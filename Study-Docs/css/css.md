# CSS방법론
> 웹에서 CSS의 영향력이 높아지게 되면서 CSS사용시 클래스 이름을 어떻게 작성할지, 어떠한 방식으로 스타일을 작성할지 등 CSS를 보다 효율적으로 작성하기 위해 정의된 일종의 규칙

사용 이유
- 원활한 유지보수
- 코드의 재사용성을 높이기 위해
- 클래스명 만으로도 무슨 내용인지 예측 가능하도록

## OOCSS
> OOCSS(Object Oriented CSS)는 CSS를 모듈(module) 방식으로 작성하여 중복을 줄이는 방식의 방법론

- 가장 많이 사용되는 방법론으로 **구조(레이아웃)와 스타일(테마,스킨)을 분리하여 작성**
- 중복되는 디자인 요소를 따로 빼내어 작성하기 때문에 **반복적으로 사용(재사용)**가능
- 컨테이너와 컨텐츠를 분리하여 **객체 지향적**인 디자인을 유도
- 새로운 테마나 레이아웃 추가가 용이한 **확장성**
- *단점*: 다중 클래스 사용으로 인해 코드의 가독성이 떨어질 수 있음, 유지보수가 어려움

```html
    <div class="btn common-skin tel">tel</div>
    <div class="btn common-skin email">email</div>
```
```css
    .btn{..} 
    .common-skin{..}
```

## BEM
> BEM(Block Element Modifier)은 블록(block), 요소(element), 수정자(modifier)로 구분하여 클래스 이름을 작성하는 방식의 방법론

- BEM은 블록(block), 요소(element), 수정자(modifier) 3가지로 구성, 각 부분을 __와 --로 구분
- **명확성** '어떠한 목적인가' 에 초점
- 스타일이 독립적으로 구성되어 다른 부분에 재사용하기 쉬움
- 엄격한 네이밍 규칙을 따르며 클래스명이 용도와 형태를 잘 표현해주어 **직관적**으로 알 수 있음
- *단점*: 클래스명이 길고 복잡해 질 수 있음, 재수정이 불편

- block
> 웹페이지의 독립적인 구성 요소를 의미
> 헤더, 메뉴, 버튼 등과 같이 재사용 가능하며 독립이 가능한 컴포넌트.
> 일반적으로 하나의 단어를 사용하되 길어질 경우엔 -를 사용한다.

```css
.header {..}
.block {..}
```

- element
> 블록 내부의 구성 요소. 해당 블록의 일부로만 의지를 가짐.
> __(더블 언더스코어)를 사용한다.

```css
.header {..}
.header__tap {..}
.header__content {..}
.header__logo__button {..}
```

- modifier
> 블록 또는 요소의 다양한 상태와 변형을 나타네는 데 사용됨.
> --(더블 대시)를 사용한다.

```css
.header--hide {..}
.header__tap--big {..}
.header__content--disabled {..}
```

## SMACSS
> SMACSS(Scalable and Modular Architecture for CSS)는 CSS를 범주화(Categorization)로 패턴화 하고자 하는 방법론

- 작성할 CSS를 비슷한 종류끼리 모아 5가지 스타일로 나누고 각 유형에 맞는 선택자와 작명법, 코딩 기법을 제시
- 클래스명을 통한 예측의 용이성, 재사용을 통한 코드의 간결화, 확장의 용이성
- 기본(base), 레이아웃(layout), 모듈(module), 상태(state), 테마(theme) 다섯가지의 범주를 제시
- *단점*: 카테고리를 나누는 기준에 따라 불분명해질 수 있음, 코드를 나누어 작성해 css사용이 번거로움

** <유의사항> **
1. 파생된 CSS셀렉터 사용금지
2. Id 셀렉터 사용금지
3. !Important 사용금지
4. 다른 개발자들이 이해할 수 있도록 class 이름을 의미있게 지어야 함


- 기본(base)
> 각 브라우저의 기본 스타일 (default.css, reset.css), 요소 element 스타일의 기본 정의 값
> Reset, Variable 등을 포함하고 !important를 쓰지 않는다.

```css
    body, form, p, table, button, fieldset, input ... {
        margin: 0;
        padding: 0;
    }
```

- 레이아웃(layout)
> 주요 요소(id)와 하위 요소(class)로 구분하고 접두사를 사용한다. *큰 틀의 레이아웃, 전체적인 페이지의 구조를 설정하고 배치*
> 주요 컴포넘트 : header, footer, aside, container, content 등
> 클래스명은 접수사 i-, layout-명시

```css
    // layout => l-

    // 주요 요소 작성
    #header {
        width: 400px;
    }
    #aside {
        width: 40px;
    }

    // 하위 요소 작성
    .l-width #header {
        width: 650px;
        padding: 10px;
    }
    .l-width #aside {
        width: 100px
    }
```

- 모듈(module)
> 재사용성이 높은 구성 요소를 정의한다.
> 페이지에서 재사용 가능한 요소 : 버튼, 배너, 아이콘, 박스 요소 등
> 각 모듈은 **독립성**을 가지게 스타일 선언 : 재사용이 가능하게 클래스 네임으로만 선택. id, 태그 선택자는 사용하지 않음.

```css
    .stick { ... }
    .stick-name { ... }
    .stick-number { ... }
```

- 상태(state)
> 요소의 상태 변화(active나 disable 등)를 표현하고 접두사 “is-“나 “s-“를 사용한다.

```css
    .is-error { ... }
    .is-hidden { ... }
    .is-disabled { ... }
```

- 테마(theme)
> 사용자가 선택 가능 하도록 스타일을 재선언하여 사용한다.
> 예시: 색상, 레이아웃, 폰트 등의 테마 관련 스타일
> Theme는 전반적인 Look and feel을 정의하며 suffix "theme-"를 붙인다.

```css
    // base.css
    .header {
        background-color: red;
    }
    // theme.css
    .header {
        background-color: orange;
    }
```

## ACSS
> ACSS(Atomic CSS)는 웹 디자인을 원자적인 부분으로 분해하는 접근 방식을 취함
> **원자**는 고유하고 불변적인 작은 스타일 단위를 의미하며, 각 원자는 단일 스타일 속성을 나타냄.

- 각 원자 클래스는 **하나의 속성과 값**을 가지며 그 **목적이 명확**해야함
- 원자 클래스는 다양한 컴포넌트와 컨텍스트에서 **재사용**될 수 있음
- 클래스 이름은 대개 스타일 규칙 속성과 값에 직접적 연관
- *단점*: html에서 많은 원자 클래스를 사용해야 할 수 있어 복잡하게 보일 수 있음, 디자인 변경 시 html/css모두 수정해야 하는 이슈 발생 가능

```css
  .m-10{ margin: 10px; }
  .pb-10{ padding-bottom: 10px; }
```
