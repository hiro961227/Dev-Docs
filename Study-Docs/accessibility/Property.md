# 요소의 속성
## Table of Contents
1. [Widget attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#widget-attributes)
   1. [aria-autocomplete](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-autocomplete)
   2. [aria-checked](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-checked)
   3. [aria-disabled](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-disabled)
   4. [aria-errormessage](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-errormessage)
   5. [aria-expanded](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-expanded)
   6. [aria-haspopup](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-haspopup)
   7. [aria-hidden](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-hidden)
   8. [aria-invalid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-invalid)
   9. [aria-label](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-label)
   10. [aria-level](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-level)
   11. [aria-modal](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-modal)
   12. [aria-multiline](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-multiline)
   13. [aria-multiselectable](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-multiselectable)
   14. [aria-orientation](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-orientation)
   15. [aria-placeholder](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-placeholder)
   16. [aria-pressed](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-pressed)
   17. [aria-readonly](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-readonly)
   18. [aria-required](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-required)
   19. [aria-selected](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-selected)
   20. [aria-sort](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-sort)
   21. [aria-valuemax](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuemax)
   22. [aria-valuemin](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuemin)
   23. [aria-valuenow](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuenow)
   24. [aria-valuetext](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuetext)


<br/>

___
___
___

<br/>

## Widget attributes
> 사용자 인터페이스 위젯의 속성 설명

<br/>

### aria-autocomplete
> 입력 필드(주로 텍스트 입력 필드)에서 **자동 완성 기능**의 동작을 정의
 
token | note
-- | --
```none``` | 자동 완성 기능을 사용하지 않음
```inline``` | 자동 완성된 내용이 인라인으로 표시. 사용자가 입력하는 동안 **자동 완성된 내용이 동적**으로 표시.
```list``` | 자동 완성된 내용이 연관된 리스트로 표시. 사용자가 필드에 입력할 때마다 연관된 리스트에서 해당 항목이 제시됨.
```both``` | 입력 필드 내에서 자동 완성된 내용이 인라인으로 표시되는 동시에, 연관 리스트에서도 표시됨.

```html
<!-- aria-autocomplete="none" -->
<input type="text" aria-autocomplete="none">
<!-- aria-autocomplete="inline" -->
<input type="text" aria-autocomplete="inline">
<!-- aria-autocomplete="list" -->
<input type="text" aria-autocomplete="list" aria-owns="suggestions">
<ul id="suggestions">
    <li>추천 항목 1</li>
    <li>추천 항목 2</li>
</ul>
<!-- aria-autocomplete="both" -->
<input type="text" aria-autocomplete="both" aria-owns="suggestions">
<ul id="suggestions">
    <li>추천 항목 1</li>
    <li>추천 항목 2</li>
</ul>
```

<br/>

### aria-checked
> 체크 상태를 나타내는 데 사용 <br/>
> 주로 시각적으로 체크 상태가 나타나지 않는 경우에 사용되며, 체크 박스나 라디오 버튼과 같은 UI 요소에서 활용됨
 
token | note
-- | --
```true``` | 요소가 체크된 상태
```false``` | 요소가 체크되지 않은 상태
```mixed``` | 체크 박스가 부분적으로 체크된 상태. 주로 체크 박스 그룹에서 일부만 선택되었을 경우 사용됨.

```html
<!-- 체크 박스의 경우 -->
<input type="checkbox" aria-checked="true">

<!-- 라디오 버튼의 경우 -->
<input type="radio" name="group1" aria-checked="false">
<input type="radio" name="group1" aria-checked="true">
<input type="radio" name="group1" aria-checked="false">
```

<br/>

### aria-disabled
> 요소의 **비활성화 여부**를 나타냄
 
일반적으로 ```disabled```속성을 사용하여 요소를 비활성화할 수 있지만, 모든 요소에 적용되지 않으므로 ```div```나 ```span```같은 요소 등 시각적으로 보여주어야 하는 요소에 ```aria-disabled``` 속성을 사용하여 사용자에게 해당 요소가 비활성화 되었음을 전달할 수 있음.

token | note
-- | --
```true``` | 요소가 비활성화 되었음을 나타냄
```false``` | ```[default]``` 요소가 활성화 되었음을 나타냄

```html
<button aria-disabled="true">클릭할 수 없는 버튼</button>
```

<br/>

### aria-errormessage
> 요소의 **오류 메시지**를 나타냄

주로 입력 필드나 폼 요소와 같은 사용자 입력을 받는 요소에 사용됨. 해당 요소에 오류가 있을 경우, 오류 메세지를 제공하여 사용자에게 오류 상황을 알림. 해당 속성은 ***오류 메세지를 포함하는 요소의 ID***를 참조함.

```html
<div id="error-message" role="alert">이 필드는 필수입니다.</div>

<input type="text" aria-errormessage="error-message" aria-invalid="true">
```

<br/>

### aria-expanded
> 요소의 **확장 상태**를 나타냄
 
주로 접근성을 향상시키기 위해 사용되며, 요소가 펼쳐진 상태인지 아닌지를 전달함. <br/>
e.g. 아코디언 메뉴, 툴팁, 드롭다운 메뉴 등

token | note
-- | --
```true``` | 요소가 펼쳐진 상태
```false``` | 요소가 축소된 상태
```undefined``` | 요소가 확장 가능한데도 확장 상태를 나타내는 데 적절한 정보를 제공할 수 없는 경우

```html
<button aria-expanded="false" aria-controls="content">펼치기</button>
<div id="content" hidden>
    내용
</div>
```

<br/>

### aria-haspopup
> 요소가 **하위 메뉴나 팝업을 가지고 있는지**를 나타냄
 
사용자에게 인터랙션 가능한 메뉴나 팝업이 있는 요소를 식별하기 위해 사용됨 <br/>
e.g. 버튼, 링크, 드롭다운 메뉴, 메뉴 등

token | note
-- | --
```true``` | 요소가 하위 메뉴나 팝업을 가지고 있음
```false``` | 요소가 하위 메뉴나 팝업을 가지고 있지 않음

```html
<button aria-haspopup="true" aria-controls="dropdown-menu">메뉴 열기</button>
<!-- 
    * aria-haspopup="true": 버튼이 하위 메뉴를 가지고 있음
    * aria-controls="dropdown-menu": 해당 버튼이 제어하는 메뉴의 ID 명시
 -->
<div id="dropdown-menu" hidden>
    <ul>
        <li><a href="#">메뉴 항목 1</a></li>
        <li><a href="#">메뉴 항목 2</a></li>
        <li><a href="#">메뉴 항목 3</a></li>
    </ul>
</div>
```

<br/>

### aria-hidden
> 요소의 **가시성**을 나타냄
 
스크린 리더를 포함한 보조 기술을 사용하는 사용자를 위해 *화면에 표시되지 않아야 하는 요소를 식별*하기 위해 사용. CSS의 ```display``` 속성이나 ```visibility``` 속성을 사용하여 화면에서 요소를 숨길 때와 같이 **시각적으로는 보이지 않지만 보조 기술을 통해 접근할 수 있는 요소**에 사용

token | note
-- | --
```true``` | 요소가 화면에서 숨겨져 있음. 이 경우, 요소와 해당 자식 요소는 시각적으로 화면에 나타나지 않지만, *접근성 트리에는 남아 있음*.
```false``` | ```[default]``` 요소가 화면에 표시되어 있음

```html
<div aria-hidden="true">
    이 영역은 스크린 리더에 의해 읽히지 않습니다.
</div>
```

<br/>

### aria-invalid
> 입력 **필드의 유효성**을 나타내는 데 사용 <br/>

주로 사용자 입력이 필요한 *폼 요소*에 적용되며, **입력이 올바르지 않을 때 해당 요소에 추가**되어 사용자가 잘못된 입력을 수정할 수 있도록 도와줌.
 
token | note
-- | --
```true``` | 입력 필드에 오류가 있음
```false``` | ```[default]``` 입력 필드에 오류가 없음

```html
<label for="email">이메일:</label>
<input type="email" id="email" aria-invalid="true" aria-describedby="email-error">
<div id="email-error">올바른 이메일 주소를 입력하세요.</div>
<!-- 
    aria-describedby 속성 사용하여 오류 메세지가 있는 요소의 ID값 참조하여, 메세지가 입력필드와 연결되어 사용자에게 정확한 오류 알려줌.
-->
```

<br/>

### aria-label
> html 요소에 접근 가능한 **설명용 텍스트**를 넣을 수 있음

* 이미지를 사용해 시각적인 표현을 할 경우 대체 텍스트 역할

```html
<div role="text" class="text-area" tabindex="0" aria-label="필요한 금액: 100원">
  <p aria-hidden="true"><strong>필요한 금액</strong></p>
  <p aria-hidden="true"><strong class="txt-blue">100</strong>원</p>
</div>
```
> 문장이나 단어 태그 안에 span, strong, br 등의 요소가 들어갈 경우 aria-hidden 처리를 한 후 상위 부모에게 초점을 이동시킨 뒤(textindex="0") aria-label로 숨김 처리한 텍스트를 작성해 읽히도록 함


<br/>

### aria-level
>  요소의 **수준(레벨)**을 나타냄

일반적으로 트리 구조를 가진 요소에서 해당 요소의 계층적 위치를 나타낼 때 사용됨. 주로 ```헤딩(제목)```요소에 사용됨. 1부터 시작(가장 높은 수준)하여 레벨이 증가함에 따라 하위 수준으로 내려감.

```html
<h1 aria-level="1">이 페이지의 제목</h1>

<h2 aria-level="2">하위 섹션 제목</h2>
```

<br/>

### aria-modal
> **대화형 모달(dialog)의 역할 및 동작**을 정의
> ```※ 모달: 사용자가 반드시 응답해야 하는 정보를 표시하고, 닫힐 때까지 기본 콘텐츠에 대한 접근을 제한함```
 
token | note
-- | --
```true``` | 모달이 열려 있고, 모달 내부에 포커스가 있을 때 모달 외부의 콘텐츠에 대한 접근을 제한함
```false``` | 모달이 열려 있지 않음

```html
<div id="modal" role="dialog" aria-modal="true">
    <p>모달 내용</p>
    <button id="close-button">닫기</button>
</div>
```

<br/>

### aria-multiline
> 입력 필드나 텍스트 영역이 **여러 줄의 텍스트를 입력할 수 있는지** 여부를 나타냄
 
입력 필드나 텍스트 영역에 사용되며, 사용자가 여러 줄의 텍스트를 입력할 수 있는지를 명시적으로 나타내는 데 사용됨.

token | note
-- | --
```true``` | 입력 필드나 텍스트 영역이 *여러 줄*의 텍스트를 입력할 수 있음
```false``` |  필드나 텍스트 영역이 *단일 줄*의 텍스트만을 입력할 수 있음

```html
<!-- 여러 줄의 텍스트 입력 가능 -->
<textarea aria-multiline="true"></textarea>
<!-- 단일 줄의 텍스트 입력 가능 -->
<input type="text" aria-multiline="false">
```

<br/>

### aria-multiselectable
> 여러 개의 항목을 **동시에 선택**할 수 있는 요소
 
주로 ```리스트```나 ```트리```와 같은 **다중 선택**이 가능한 요소에서 사용됨

token | note
-- | --
```true``` | 여러 항목을 동시에 선택할 수 있는 요소
```false``` | ```[default]``` 한 번에 하나의 항목만 선택할 수 있는 요소 

```html
<!-- 다중 선택 가능 -->
<ul aria-multiselectable="true">
    <li>항목 1</li>
    <li>항목 2</li>
    <li>항목 3</li>
</ul>
<!-- 다중 선택 불가능 -->
<ul>
    <li>항목 1</li>
    <li>항목 2</li>
    <li>항목 3</li>
</ul>
```

<br/>

### aria-orientation
> 요소의 **방향(orientation)**을 나타냄
 
주로 ```슬라이더```, ```스크롤바``` 등과 같이 **방향이 중요한 UI 요소**에서 사용됨

token | note
-- | --
```horizontal``` | 요소가 가로 방향으로 나타남
```vertical``` | 요소가 세로 방향으로 나타남

```html
<!-- 가로 방향으로 움직이는 슬라이더 -->
<input type="range" min="0" max="100" value="50" aria-orientation="horizontal">
<!-- 세로 방향으로 움직이는 슬라이더 -->
<div role="scrollbar" aria-orientation="vertical">
    <!-- 스크롤되는 콘텐츠 -->
</div>
```

<br/>

### aria-placeholder
> 입력 필드의 **플레이스홀더(placeholder) 텍스트** <br/>
> ```※ 플레이스홀더: 사용자가 입력해야 할 내용을 나타내는 짧은 설명```
 
html5의 ```placeholder```속성과 유사하지만 보조기기 사용자에게 플레이스홀더 텍스트를 전달하기 위해 ```aria-placeholder```속성이 사용됨 

```html
<!-- placeholder or aria-placeholder 둘 중 하나만 사용(의미 중복) -->
<input type="text" placeholder="검색어를 입력하세요"> <!-- 일반적으로 권장됨 -->
<input type="text" aria-placeholder="검색어를 입력하세요">
```

<br/>

### aria-pressed
> 토글(toggle) 버튼의 **눌림 상태**를 나타냄
 
token | note
-- | --
```true``` | 토글 버튼이 눌려진 상태
```false``` | 토글 버튼이 눌려지지 않은 상태
```undefined``` | 토글 버튼이 눌릴 수 있으나 현재의 눌림 상태를 알 수 없는 경우

```html
<button aria-pressed="false" onclick="toggleButton(this)">누르기</button>

<!-- javascript로 토글 버튼 클릭되었을 때 상태 변경 -->
function toggleButton(button) {
    if (button.getAttribute('aria-pressed') === 'true') {
        button.setAttribute('aria-pressed', 'false');
    } else {
        button.setAttribute('aria-pressed', 'true');
    }
}
```

<br/>

### aria-readonly
> 사용자가 **요소의 값을 편집할 수 있는지** 여부를 나타냄

주로 편집이 가능한 요소인데도 *사용자에게 읽기 전용으로 제공되어야 하는 경우* 사용됨.

token | note
-- | --
```true``` | 요소의 값이 읽기 전용임을 나타냄. 사용자는 해당 요소 값을 편집할 수 없음.
```false``` | ```[default]``` 요소의 값이 편집 가능함을 나타냄. 사용자는 해당 요소의 값을 편집할 수 있음.

```html
<!-- 읽기 전용 -->
<input type="text" value="읽기 전용 값" aria-readonly="true">
<input type="text" value="읽기 전용 값" readonly> <!-- 권장(중복 사용x) -->

<!-- 편집 가능: 입력 필드는 기본 편집 가능하기에 aria-readonly 설정하지 않아도 됨 -->
<input type="text" value="편집 가능한 값">
```

<br/>

### aria-required
> 사용자가 반드시 입력해야 하는 필수 입력 필드를 나타냄
 
주로 ```폼 요소```에서 사용되며, 사용자가 *필수적으로 값을 입력해야 하는 경우*에 시각적으로나 보조 기기를 통해 명시적으로 전달됨

token | note
-- | --
```true``` | 입력 필드가 필수 입력 필드임을 나타냄
```false``` | ```[default]``` 입력 필드가 선택적인 필드임을 나타냄

```html
<!-- 필수 입력 필드일 경우 -->
<label for="username">사용자 이름:</label>
<input type="text" id="username" aria-required="true">

<!-- 선택 입력 필드일 경우 -->
<label for="email">이메일:</label>
<input type="email" id="email" aria-required="false"> <!-- aria-required 생략 가능 -->
```

<br/>

### aria-selected
>  사용자가 **선택한 요소**를 나타냄
 
주로 *다중 선택이 가능한 요소*에서 사용되며, 사용자가 특정 항목을 선택했는지 여부를 명시적으로 나타내는 데 사용됨

token | note
-- | --
```true``` | 요소가 선택된 상태임을 나타냄
```false``` | 요소가 선택되지 않은 상태임을 나타냄
```undefined``` | 요소가 선택 가능하거나 현재의 선택 상태를 알 수 없는 경우에 사용

```html
<!-- 선택 가능한 항목들이 있는 리스트에서 특정 항목(항목2)을 선택한 경우 -->
<ul>
    <li aria-selected="true">항목 1</li>
    <li aria-selected="false">항목 2</li>
    <li aria-selected="false">항목 3</li>
</ul>
<!-- 다중 선택이 가능한 경우 여러 항목(항목1,3,4)이 선택 되어있을 수 있음 -->
<ul>
    <li aria-selected="true">항목 1</li>
    <li aria-selected="false">항목 2</li>
    <li aria-selected="true">항목 3</li>
    <li aria-selected="true">항목 4</li>
</ul>

```

<br/>

### aria-sort
> 테이블의 열이나 리스트 등에서 **정렬된 상태**를 나타냄
 
주로 정렬 가능한 ```테이블의 열```에서 사용되며, 열의 정렬 방향과 *현재 정렬된 상태를 사용자에게 명확하게 전달*하는 데 사용됨

token | note
-- | --
```none``` | 열이 정렬되지 않은 상태
```ascending``` | 열이 **오름차순**으로 정렬된 상태
```descending``` | 열이 **내림차순**으로 정렬된 상태

```html
<table>
    <thead>
        <tr>
            <th id="name" aria-sort="ascending">이름</th>
            <th id="age" aria-sort="none">나이</th>
            <th id="city" aria-sort="none">도시</th>
            <!--  
                "이름" 열은 오름차순으로 정렬되었으며, 
                "나이"와 "도시" 열은 정렬되지 않은 상태 
            -->
        </tr>
    </thead>
    <tbody>
        <!-- 테이블 내용 -->
    </tbody>
</table>
```

<br/>

### aria-valuemax
> 슬라이더, 프로그레스 바 등과 같은 *범위를 나타내는 UI 요소*에서 가장 큰 값, 즉 **최댓값**을 나타냄
 
```html
<input type="range" min="0" max="100" value="50" aria-valuemax="100">
<!-- 슬라이더의 최댓값은 100 -->
```

<br/>

### aria-valuemin
> 슬라이더, 프로그레스 바 등과 같은 *범위를 나타내는 UI 요소*에서 가장 작은 값, 즉 **최솟값**을 나타냄
 
```html
<input type="range" min="0" max="100" value="50" aria-valuemin="0">
<!-- 슬라이더의 최솟값은 0 -->
```

<br/>

### aria-valuenow
> 슬라이더, 프로그레스 바 등과 같은 *범위를 나타내는 UI 요소*에서 **현재 위치나 상태에 해당하는 값**을 나타냄
 
해당 요소의 값은 aria-valuemin과 aria-valuemax 사이의 값을 가져야 함

```html
<input type="range" min="0" max="100" value="50" aria-valuenow="50">
<!-- 슬라이더의 현재 값은 50 -->
```

<br/>

### aria-valuetext
> ```aria-valuenow```속성 값을 설명하는 텍스트를 제공함
 
```aria-valuenow``` 속성이 설정된 경우에만 사용되며, 특정 값이 숫자로 표현하기 부족한 경우 응용할 수 있음. 해당 값이 숫자 값을 경우에는 무시되지만, 누락되었거나 숫자 값이 아닌 경우 사용됨. <br/>
e.g. 저, 중간, 높음 등

```html
<input type="range" min="0" max="100" value="50" aria-valuetext="50%">
<!-- 슬라이더의 현재 값은 50%로 설명됨 -->
```

<br/>
