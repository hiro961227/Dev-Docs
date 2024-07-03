# Gulp + Nunjucks를 이용해 컴포넌트 제작하기

html을 작성할 때 공통 요소를 탬플릿으로 생성해, 보다 더 관리하기 쉽도록 컴포넌트를 작업해 보는 것을 목표로 해당 사이트([UXKM의 gulp](https://uxkm.io/buildSystem/gulp/01-gulp_start/01-intro#gsc.tab=0))를 참고로 하여 작업하였다.  <br/>
gulp와 nunjucks 모두 처음 접해보는 언어로 가이드를 보며 소스 코드를 파악하고 응용하며 작업하는 데 있어 난항을 겪거나 기억하고자 하는 부분들을 정리해보자 한다. <br/><br/>

***

## if의 중첩이 가능하다(!)

gulp에서 if문을 사용할 때 또한 ```&& === and```, ```|| === or```, ```! === not``` 처럼 문자 기술을 하면 삼항연산자 사용이 가능하다. 버튼 컴포넌트를 제작할 때 버튼의 텍스트가 두 줄이 될 경우와 아이콘을 함께 사용할 경우를 염두하여 식을 작성하고 싶어 해당 형식을 사용했다. indent를 고려하여 if문 앞에 - 기호를 붙이고, 아이콘을 포함한 i태그 역시 간격 조정이 필요하다. 중첩 형식 또한 일반 javascript처럼 응용하면 적용이 가능하다.

```gulp
<button type="button">
    {% if btnAriaHidden -%}
        <span aria-hidden="true">
            <em>{{ btnTitle }}</em> <br>
            <em>{{ btnTitle2 }}</em>
        </span>
        {%- if btnIconTxt %}
        <i class="{{ btnIconTxt }}" aria-hidden="true"></i>
        {%- endif %}
        ...
    {% endif %}
</button>
```

위와 같은 gulp문을 작성하면 아래처럼 html이 빌드된다.

```html
<!-- btnAriaHidden가 true고 btnIconTxt가 false일때 -->
<button type="button"> 
    <span aria-hidden="true">
        <em>버튼의 텍스트가</em> <br>
        <em>두 줄 일 경우</em>
    </span>
</button>

<!-- btnAriaHidden가 true고 btnIconTxt가 true일때 -->
<button type="button"> 
    <span aria-hidden="true">
        <em>버튼의 텍스트가 두 줄 이고</em> <br>
        <em>아이콘을 포함하고 있을 경우</em>
    </span>
    <i class="icon_link" aria-hidden="true"></i>
</button>
```

<br/>

## {%- -%} 구문

주로 템플릿 엔진에서 사용되며, 특정한 지시어와 루프, 조건문 등 제어 구조의 공백을 제어하는 데 사용된다. nunjucks의 경우 의도대로 들여쓰기가 되지 않는 단점이 있지만 - 기호로 공백의 조정이 가능하다. <br/>
{%- 의 구문으로 공백 조정이 어떻게 빌드되는지, gulpfile.bable.js에 추가해둔 filter태그가 어떻게 상호작용되는지 아래 예제로 확인하고자 한다.<br/>

json파일에 gnb_data라는 데이터 태그가 존재하는 가정 하 아래 태그가 어떻게 빌드되는지 확인한다. <br/><br/>

** filter 태그가 없는 경우 **<br/>
```예제1```
```gulp
    <ul>
    {% for item in gnb_data %}
    <li>{{loop.index}}. {{item.name}}</li>
    {% endfor %}
    </ul>
```

```html
    <ul>
    
    <li>1. home</li>
    
    <li>2. intro</li>
    
    <li>3. history</li>
    
    </ul>
```

```예제2```
```gulp
    <ul>
    {% for item in gnb_data %}
        <li>{{loop.index}}. {{item.name}}</li>
    {% endfor %}
    </ul>

    <!-- or -->
        
    <ul>
        {% for item in gnb_data %}
        <li>{{loop.index}}. {{item.name}}</li>
        {% endfor %}
    </ul>
```

```html
    <ul>
    
        <li>1. home</li>
    
        <li>2. intro</li>
    
        <li>3. history</li>
    
    </ul>
```

```예제3```
```gulp
    <ul>
    {%- for item in gnb_data %}
    <li>{{loop.index}}. {{item.name}}</li>
    {%- endfor %}
    </ul>
```

```html
    <ul>
    <li>1. home</li>
    <li>2. intro</li>
    <li>3. history</li>
    </ul>
```

```예제4```
```gulp
    <ul>
    {%- for item in gnb_data %}
        <li>{{loop.index}}. {{item.name}}</li>
    {%- endfor %}
    </ul>
```

```html
    <ul>
        <li>1. home</li>
        <li>2. intro</li>
        <li>3. history</li>
    </ul>
```

```예제5```
```gulp
    <ul>
    {%- for item in gnb_data %}
        <li>{{loop.index}}. {{item.name}}</li>
    {% endfor %}
    </ul>
```

```html
    <ul>
    
        <li>1. home</li>
        <li>2. intro</li>
        <li>3. history</li>
    </ul>
```

```예제6```
```gulp
    <ul>
    {% for item in gnb_data -%}
        <li>{{loop.index}}. {{item.name}}</li>
    {% endfor %}
    </ul>
```

```html
    <ul>
    <li>1. home</li>
    <li>2. intro</li>
    <li>3. history</li>
    
    </ul>
```

```예제7```
```gulp
    <ul>
    {% for item in gnb_data %}
        <li>{{loop.index}}. {{item.name}}</li>
    {% endfor -%}
    </ul>
```

```html
    <ul>
    
        <li>1. home</li>
    
        <li>2. intro</li>
    
        <li>3. history</li>
    </ul>
```

```예제8```
```gulp
    <ul>
    {%- for item in gnb_data -%}
        <li>{{loop.index}}. {{item.name}}</li>
    {% endfor %}
    </ul>
```

```html
    <ul><li>1. home</li>
    <li>2. intro</li>
    <li>3. history</li>
    
    </ul>
```

```예제9```
```gulp
    <ul>
    {% for item in gnb_data %}
        <li>{{loop.index}}. {{item.name}}</li>
    {%- endfor -%}
    </ul>
```

```html
    <ul>
    
        <li>1. home</li>
        <li>2. intro</li>
        <li>3. history</li></ul>
```

```예제10```
```gulp
    <ul>
    {%- for item in gnb_data -%}
        <li>{{loop.index}}. {{item.name}}</li>
    {%- endfor -%}
    </ul>
```

```html
    <ul><li>1. home</li><li>2. intro</li><li>3. history</li></ul>
```
