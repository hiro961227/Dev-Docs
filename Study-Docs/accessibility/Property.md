# 요소의 속성
## Table of Contents
1. [Widget attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#widget-attributes)
   1. [aria-autocomplete](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-autocomplete)
   2. [aria-errormessage](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-errormessage)
   3. [aria-haspopup](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-haspopup)
   4. [aria-keyshortcuts](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-keyshortcuts)
   5. [aria-label](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-label)
   6.  [aria-level](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-level)
   7. [aria-modal](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-modal)
   8.  [aria-multiline](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-multiline)
   9.  [aria-multiselectable](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-multiselectable)
   10. [aria-orientation](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-orientation)
   11. [aria-placeholder](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-placeholder)
   12. [aria-readonly](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-readonly)
   13. [aria-required](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-required)
   14. [aria-sort](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-sort)
   15. [aria-valuemax](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuemax)
   16. [aria-valuemin](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuemin)
   17. [aria-valuenow](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuenow)
   18. [aria-valuetext](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-valuetext)
2. [Live region attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#live-region-attributes)
   1. [aria-atomic](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-atomic)
   2. [aria-live](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-live)
   3. [aria-relevant](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-relevant)
3. [Drag-and-Drop attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#drag-and-drop-attributes)
    1. [aria-dropeffect](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-dropeffect)
4. [Relationship attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#relationship-attributes)
    1. [aria-activedescendant](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-activedescendant)
    2. [aria-colcount](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-colcount)
    3. [aria-colindex](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-colindex)
    4. [aria-colspan](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-colspan)
    5. [aria-controls](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-controls)
    6. [aria-describedby](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-describedby)
    7. [aria-details](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-details)
    8. [aria-flowto](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-flowto)
    9.  [aria-labelledby](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-labelledby)
    10. [aria-owns](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-owns)
    11. [aria-posinset](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-posinset)
    12. [aria-rowcount](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-rowcount)
    13. [aria-rowindex](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-rowindex)
    14. [aria-rowspan](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-rowspan)
    15. [aria-roledescription](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-roledescription)
    16. [aria-setsize](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md#aria-setsize)


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

> **역할 사용** [combobox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#combobox) | [textbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#textbox) <br/>
> **역할 상속** [searchbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#searchbox)

<br/>

### aria-errormessage
> 요소의 **오류 메시지**를 나타냄

주로 입력 필드나 폼 요소와 같은 사용자 입력을 받는 요소에 사용됨. 해당 요소에 오류가 있을 경우, 오류 메세지를 제공하여 사용자에게 오류 상황을 알림. 해당 속성은 ***오류 메세지를 포함하는 요소의 ID***를 참조함.

```html
<div id="error-message" role="alert">이 필드는 필수입니다.</div>

<input type="text" aria-errormessage="error-message" aria-invalid="true">
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>


### aria-haspopup
> 요소가 **하위 메뉴나 팝업을 가지고 있는지**를 나타냄
 
사용자에게 인터랙션 가능한 메뉴나 팝업이 있는 요소를 식별하기 위해 사용됨 <br/>
e.g. 버튼, 링크, 드롭다운 메뉴, 메뉴 등

token | note
-- | --
```false``` | ```[default]``` 요소가 하위 메뉴나 팝업을 가지고 있지 않음
```true``` | 요소가 하위 메뉴나 팝업을 가지고 있음
```menu``` | 팝업이 메뉴 형태임을 나타냄 e.g. 드롭다운 메뉴, 컨텍스 메뉴
```listbox``` | 팝업이 목록 상자 형태임을 나타냄 e.g. 선택 목록, 아이템 목록
```tree``` | 팝업이 트리 형태임을 나타냄 e.g. 트리 메뉴, 폴더(계층적 구조)
```grid``` | 팝업이 그리드 형태임을 나타냄 e.g. 표 형태로 정렬된 데이터
```dialog``` | 팝업이 대화 상자 형태임을 나타냄

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

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-keyshortcuts
> 특정 **키보드 단축키를 사용하여 요소의 기능을 활성화**하는 데 사용됨
 
공백으로 구분된 문자열의 리스트로 구성됨. 각 문자열은 하나 이상의 키보드 단축키를 나타내며, javascript 등의 이벤트 핸들러와 함께 사용되어 사용자가 해당 단축키를 누르면 연결된 기능이 실행됨.


```html
<!-- 
    Alt + C 키를 누르면 주소록 열기 기능이 실행됨을 알림
    실제 기능은 onclick="openContacts()"에 내포되어 있음
-->
<button aria-keyshortcuts="Alt+C" onclick="openContacts()">주소록 열기</button>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능


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
> 문장이나 단어 태그 안에 ```span```, ```strong```, ```br``` 등의 요소가 들어갈 경우 ```aria-hidden``` 처리를 한 후 상위 부모에게``` 초점을 이동시킨 뒤(textindex="0")``` **aria-label로 숨김 처리한 텍스트를 작성**해 읽히도록 함 <br/>

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능


<br/>

### aria-level
>  요소의 **수준**을 나타냄

일반적으로 트리 구조를 가진 요소에서 해당 요소의 계층적 위치를 나타낼 때 사용됨. 주로 ```헤딩(제목)```요소에 사용됨. 1부터 시작(가장 높은 수준)하여 레벨이 증가함에 따라 하위 수준으로 내려감.

```html
<h1 aria-level="1">이 페이지의 제목</h1>

<h2 aria-level="2">하위 섹션 제목</h2>
```

> **역할 사용** [grid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#grid) | [heading](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#heading) | [listitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#listitem) | [row](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#row) | [tablist](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tablist) <br/>
> **역할 상속** [treegrid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treegrid) | [treeitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treeitem)

<br/>

### aria-modal
> **대화형 모달(dialog)의 역할 및 동작**을 정의 <br/>
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

> **역할 사용** [window](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#window) <br/>
> **역할 상속** [alertdialog](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#alertdialog) | [dialog](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#dialog)

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

> **역할 사용** [textbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#textbox) <br/>
> **역할 상속** [searchbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#searchbox)

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

> **역할 사용** [grid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#grid) | [listbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#listbox) | [tablist](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tablist) | [tree](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tree) <br/>
> **역할 상속** [treegrid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treegrid)


<br/>

### aria-orientation
> 요소의 **방향**을 나타냄
 
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

> **역할 사용** [scrollbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#scrollbar) | [select](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#select) | [separator](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#separator) | [slider](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#slider) | [tablist](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tablist) | [toolbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#toolbar) <br/>
> **역할 상속** [combobox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#combobox) | [listbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#listbox) | [menu](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menu) | [menubar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menubar) | [radiogroup](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#radiogroup) | [tree](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tree) | [treegrid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treegrid)


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

> **역할 사용** [textbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#textbox) <br/>
> **역할 상속** [searchbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#searchbox)

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

> **역할 사용** [checkbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#checkbox) | [combobox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#combobox) | [grid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#grid) | [gridcell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#gridcell) | [listbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#listbox) | [radiogroup](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#radiogroup) | [slider](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#slider) | [spinbutton](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#spinbutton) | [textbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#textbox) <br/>
> **역할 상속** [columnheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#columnheader) | [menuitemcheckbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitemcheckbox) | [menuitemradio](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitemradio) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader) | [searchbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#searchbox) | [treegrid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treegrid)


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

> **역할 사용** [combobox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#combobox) | [gridcell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#gridcell) | [listbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#listbox) | [radiogroup](radiogroup) | [spinbutton](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#spinbutton) | [textbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#textbox) | [tree](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tree) <br/>
> **역할 상속** [columnheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#columnheader) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader)| [searchbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#searchbox)| [treegrid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treegrid)


<br/>

### aria-sort
> 테이블의 열이나 리스트 등에서 **정렬된 상태**를 나타냄
 
주로 정렬 가능한 ```테이블의 열```에서 사용되며, 열의 정렬 방향과 *현재 정렬된 상태를 사용자에게 명확하게 전달*하는 데 사용됨

token | note
-- | --
```none``` | ```[default]``` 열이 정렬되지 않은 상태
```ascending``` | 열이 **오름차순**으로 정렬된 상태
```descending``` | 열이 **내림차순**으로 정렬된 상태
```other``` | 오름차순, 내림차순 외의 정렬 알고리즘이 적용된 상태

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

> **역할 사용** [columnheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#columnheader) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader)

<br/>


### aria-valuemax
> 슬라이더, 프로그레스 바 등과 같은 *범위를 나타내는 UI 요소*에서 가장 큰 값, 즉 **최댓값**을 나타냄
 
```html
<input type="range" min="0" max="100" value="50" aria-valuemax="100">
<!-- 슬라이더의 최댓값은 100 -->
```

> **역할 사용** [range](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#range) | [scrollbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#scrollbar) | [separator](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#separator) | [slider](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#slider) | [spinbutton](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#spinbutton) <br/>
> **역할 상속** [progressbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#progressbar)

<br/>

### aria-valuemin
> 슬라이더, 프로그레스 바 등과 같은 *범위를 나타내는 UI 요소*에서 가장 작은 값, 즉 **최솟값**을 나타냄
 
```html
<input type="range" min="0" max="100" value="50" aria-valuemin="0">
<!-- 슬라이더의 최솟값은 0 -->
```

> **역할 사용** [range](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#range) | [scrollbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#scrollbar) | [separator](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#separator) | [slider](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#slider) | [spinbutton](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#spinbutton) <br/>
> **역할 상속** [progressbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#progressbar)


<br/>

### aria-valuenow
> 슬라이더, 프로그레스 바 등과 같은 *범위를 나타내는 UI 요소*에서 **현재 위치나 상태에 해당하는 값**을 나타냄
 
해당 요소의 값은 aria-valuemin과 aria-valuemax 사이의 값을 가져야 함

```html
<input type="range" min="0" max="100" value="50" aria-valuenow="50">
<!-- 슬라이더의 현재 값은 50 -->
```

> **역할 사용** [range](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#range) | [scrollbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#scrollbar) | [separator](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#separator) | [slider](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#slider) | [spinbutton](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#spinbutton) <br/>
> **역할 상속** [progressbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#progressbar)

<br/>

### aria-valuetext
> ```aria-valuenow```속성 값을 설명하는 텍스트를 제공함
 
```aria-valuenow``` 속성이 설정된 경우에만 사용되며, 특정 값이 숫자로 표현하기 부족한 경우 응용할 수 있음. 해당 값이 숫자 값을 경우에는 무시되지만, 누락되었거나 숫자 값이 아닌 경우 사용됨. <br/>
e.g. 저, 중간, 높음 등

```html
<input type="range" min="0" max="100" value="50" aria-valuetext="50%">
<!-- 슬라이더의 현재 값은 50%로 설명됨 -->
```

> **역할 사용** [range](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#range) | [separator](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#separator) <br/>
> **역할 상속** [progressbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#progressbar) | [scrollbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#scrollbar) | [slider](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#slider) | [spinbutton](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#spinbutton)


<br/>

## Live region attributes
> 동적으로 업데이트되는 콘텐츠 설명 <br/>
> ``` ※ Live Region: 화면에 표시되는 동안 업데이트되는 콘텐츠를 보조 기기 사용자에게 즉시 알리는 데 사용 ```

<br/>


### aria-atomic
> Live Region 요소가 업데이트될 때 해당 요소의 모든 자식 요소를 포함하여 전체 콘텐츠를 **전달할지 여부**를 나타냄
 
token | note
-- | --
```true``` | Live Region 요소가 업데이트될 때 해당 요소의 **모든 자식 요소를 포함하여 전체 콘텐츠를 전달**함
```false``` | ```[default]``` Live Region 요소가 업데이트될 때 **해당 요소의 변경된 부분만을 전달**함

```html
<!-- 모든 자식 요소의 내용이 업데이트 될 때 함께 전달됨 -->
<div role="status" aria-live="assertive" aria-atomic="true">
    <div>새로운 메시지 도착</div>
    <div>메시지 내용: "안녕하세요!"</div>
</div>

<!-- 특정 부분이 업데이트 되었을 때 해당 부분만 전달됨 -->
<div role="status" aria-live="assertive">
    <div>새로운 메시지 도착: <span aria-atomic="false">"안녕하세요!"</span></div>
</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-live
> 사용자들에게 새로운 콘텐츠나 상태 변경을 실시간으로 알려주는 데 사용 <br/>
> 특정한 영역이나 엘리먼트가 업데이트되는 경우, 그 변경사항을 즉시 알려주는 역할

token | note
-- | --
```off``` | ```[default]``` 실시간 업데이트를 알리지 않아야 함(변경사항이 사용자에게 중요하지 않을 때 사용)
```assertive``` | 현재 사용자 작업을 중단하고 즉시 업데이트된 내용을 알려줌, 사용자의 주의를 끌 때 사용됨 e.g. 긴급 알림, 오류 메세지
```polite``` | 사용자 작업을 방해하지 않고, 현재 활동이 종료되면 업데이트된 내용을 알려줌 e.g. 채팅 앱 새로운 메세지

```html
<div id="status-message" aria-live="off">
  현재 상태: 대기 중
</div>
<div id="live-region" aria-live="assertive">
  경고!
</div>
<div id="live-region" aria-live="polite">
  <p>새로운 메시지가 도착했습니다!</p>
</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-relevant
> Live Region 요소의 **업데이트가 화면에 표시되는 방식**을 정의함
 
아래 세 가지 값 중 하나, 혹은 공백으로 구분해 조합하여 사용할 수 있음.

token | note
-- | --
```additions``` | **새로운 항목이 추가**될 때 변경 사항을 알림
```removals``` | **기존 항목이 제거**될 때 변경 사항을 알림
```text``` | **텍스트 내용이 변경**될 때 변경 사항을 알림

```html
<!-- 
    실시간으로 새로운 메세지를 읽어주는 채팅 창
    텍스트가 변경될 때마다 스크린 리더에게 알려줌
 -->
<div role="log" aria-live="polite" aria-relevant="additions text">
    <!-- 실시간으로 업데이트되는 메시지가 여기에 표시됩니다. -->
</div>

<!-- 채팅 메세지가 일정 시간이 지난 후 화면에서 삭제됨 -->
<div role="log" aria-live="polite" aria-relevant="additions removals text">
    <!-- 업데이트된 메시지가 여기에 표시됩니다. -->
</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

## Drag-and-Drop attributes
> Relationship attributes 속성에 속하며, 관계와 상호작용을 설명함

<br/>

### aria-dropeffect
> 요소가 **드래그 앤 드롭 작업에 응답하는 방식**을 나타내 사용자에게 요소가 어떻게 드롭될지 힌트를 제공함
 
token | note
-- | --
```copy``` | 드롭된 요소의 복사본을 만듦
```move``` | 드롭된 요소를 새 위치로 이동시킴
```link``` | 드롭된 요소와 관련된 리소스에 대한 링크를 만듦
```execute``` | 드롭된 요소를 실행함
```popup``` | 드롭된 요소에 대한 팝업을 표시함
```none``` | 드롭 효과가 없음

```html
<!-- 드래그 앤 드롭 영역에 이미지를 드롭하면 복사본이 생성됨 -->
<div id="dropzone" aria-dropeffect="copy">
    여기에 이미지를 드래그하세요.
</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능


<br/>

## Relationship attributes
> 요소 간의 관계를 설명하기 위해 사용. <br/>
> 보조 기술이 요소들 사이의 상호작용을 이해하고, 사용자에게 적절한 정보를 제공하는 데 도움이 됨.

<br/>

### aria-activedescendant
> 사용자가 다른 요소에 **포커스를 이동하면서도 특정 부모 요소의 하위 요소 중 하나가 활성화되어 있음**을 나타냄 <br/>
> 키보드를 사용하여 탐색하거나 특정 기준에 따라 요소를 선택할 때 유용함
 
부모 요소에 있는 하나의 **활성화된 자식 요소의 ID**를 가짐. 항목이 이동될 때마다 속성값이 해당 항목의 ID값으로 변경됨으로써 스크린 리더 등의 보조 기기 사용자는 현재 활성화된 항목을 인식하고, 사용자에게 즉각적인 피드백을 제공함. <br/>
e.g.
1. 드롭다운 메뉴와 같은 컨트롤에서 포커스가 메뉴 항목 사이를 이동할 때
2. 트리 컨트롤에서 선택된 노드를 표시할 때
3. 탭 패널에서 현재 활성화된 탭을 지정할 때

```html
<div id="menu" role="menu" aria-activedescendant="item1">
<!-- 
    현재 활성화된 항목의 ID인 "item1"로 설정되어 있음 
    사용자가 키보드를 사용하여 다른 항목으로 이동 > 해당 항목의 ID가 속성값으로 변경
-->
    <div id="item1" role="menuitem">항목 1</div>
    <div id="item2" role="menuitem">항목 2</div>
    <div id="item3" role="menuitem">항목 3</div>
</div>
```

> **역할 사용** [application](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#application) | [composite](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#composite) | [group](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#group) | [textbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#textbox) <br/>
> **역할 상속** [combobox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#combobox) | [grid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#grid) | [listbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#listbox) | [menu](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menu) | [menubar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menubar) | [radiogroup](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#radiogroup) | [row](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#row) | [searchbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#searchbox) | [select](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#select) | [spinbutton](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#spinbutton) | [tablist](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tablist) | [toolbar](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#toolbar) | [tree](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tree) | [treeitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treeitem)


<br/>

### aria-colcount
> **테이블의 열 수**를 나타냄. <br/>
> 정수 값을 가지며, 보조 기기 사용자에게 테이블의 구조를 전달하는 데 사용됨.

```html
<table aria-colcount="3">
    <!-- 총 3개의 열을 가지고 있음 -->
    <tr>
        <td>열 1</td>
        <td>열 2</td>
        <td>열 3</td>
    </tr>
    <tr>
        <td>내용 1-1</td>
        <td>내용 1-2</td>
        <td>내용 1-3</td>
    </tr>
    <tr>
        <td>내용 2-1</td>
        <td>내용 2-2</td>
        <td>내용 2-3</td>
    </tr>
</table>
```

> **역할 사용** [table](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#table) <br/>
> **역할 상속** [grid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#grid) | [treegrid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treegrid)


<br/>

### aria-colindex
> **특정 셀이 속한 열의 인덱스(순서)**를 나타냄 <br/>
> 열의 인덱스는 1부터 시작하며 정수 값을 가짐. 테이블의 각 셀이 어느 열에 속하는지 전달하는 데 사용됨
  
```html
<table>
    <!-- 첫 번째 행의 각 셀은 각각 1, 2, 3번째 열에 속함 -->
    <tr>
        <td aria-colindex="1">열 1</td>
        <td aria-colindex="2">열 2</td>
        <td aria-colindex="3">열 3</td>
    </tr>
    <tr>
        <td>내용 1-1</td>
        <td>내용 1-2</td>
        <td>내용 1-3</td>
    </tr>
    <tr>
        <td>내용 2-1</td>
        <td>내용 2-2</td>
        <td>내용 2-3</td>
    </tr>
</table>
```

> **역할 사용** [cell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#cell) | [row](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#row) <br/>
> **역할 상속** [columnheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#columnheader) | [gridcell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#gridcell) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader)


<br/>

### aria-colspan
> 테이블의 셀이 **가로 방향으로 확장되는 열의 수**를 나타냄 <br/>
> 정수 값을 가지며, 테이블의 셀이 여러 열에 걸쳐 있는 경우 사용됨. 해당 셀이 몇 개의 열을 차지하는지 보조 기기에게 알려줌
 
```html
<table>
    <tr>
        <td>열 1</td>
        <td colspan="2">열 2와 3</td>
        <!-- 브라우저가 테이블을 그릴 때 사용되는 colspan이 aria-colspan과 동일한 역할을 함 -->
        <td>열 4</td>
    </tr>
    <tr>
        <td>내용 1-1</td>
        <td>내용 1-2</td>
        <td>내용 1-3</td>
        <td>내용 1-4</td>
    </tr>
    <tr>
        <td>내용 2-1</td>
        <td>내용 2-2</td>
        <td>내용 2-3</td>
        <td>내용 2-4</td>
    </tr>
</table>
```

> **역할 사용** [cell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#cell) | [row](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#row) <br/>
> **역할 상속** [columnheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#columnheader) | [gridcell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#gridcell) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader)


<br/>

### aria-controls
> 사용자 인터페이스 요소 간의 관계를 명시하고 전달하는데 사용 <br/>
> 현재 요소와 연결된 **대상 요소의 ID**를 나타냄 <br/>
> 레이블, 버튼, 탭 패널같은 요소들 사이의 관계 정의 시 사용됨

* ```콘텐츠 연결```: 밀접하게 연관된 요소의 관계를 명시적으로 나타내야 할 때
* ```상호작용 요소 제어```: 다른 요소의 동작을 제어하거나 영향을 미칠 때

```html
<!-- 탭 패널 예제 -->
<ul role="tablist">
<!-- 
    탭이 관리하는 탭 패널의 ID값을 넣어주고, 
    탭을 클릭하여 패널이 expanded="true"되었을 때 
    해당 패널에 초점이 이동하도록 tabindex=0을 부여해줌
 -->
    <li role="tab" aria-selected="true" aria-controls="a1" tabindex="0" id="tab1">tab1</li>
    <li role="tab" aria-selected="false" aria-controls="b1" tabindex="-1" id="tab2">tab2</li>
</ul>
<div role="tabpanel" aria-labelledby="tab1" aria-expanded="true" tabindex="0" id="a1">
    tab1 내용
</div>

<!-- 팝업 예제 -->
<button id="button" aria-controls="popup">팝업 열기</button>
<!-- aria-controls가 div#popup의 ID값을 가지고 있음 > 해당 요소를 제어함 -->
<div id="popup" role="dialog" aria-labelledby="popupTitle" aria-hidden="true">
    <h2 id="popupTitle">팝업 제목</h2>
    <p>팝업 내용</p>
    <button onclick="closePopup()">닫기</button>
</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-describedby
> 현재 요소와 **관련된 설명을 제공하는 요소의 ID**를 나타냄
 
레이블이나 설명을 *별도의 요소에 작성*하고, 해당 요소의 ID를 ```aria-describedby``` 속성에 제공하여 **요소에 설명을 연결**할 때 사용됨

```html
<label for="username">사용자 이름:</label>
<input type="text" id="username" aria-describedby="username-desc">
<div id="username-desc">사용자 이름은 5자 이상이어야 합니다.</div>
<!-- 보조 기기 사용자가 입력 필드에 포커스를 이동할 때 해당 #username-desc의 설명을 읽어줌 -->
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능


<br/>

### aria-details
> 현재 요소와 **관련된 세부 정보가 포함된 요소의 ID**를 나타냄
 
별도의 요소에 상세 정보를 작성하고, 해당 요소의 ID를 ```aria-details``` 속성에 추가하여 **현재 요소에 연결**할 때 사용됨
 
```html
<!-- 사용자에게 추가 정보를 제공하는 버튼을 가진 경우 -->
<button aria-controls="details" aria-expanded="false" aria-details="more-info">자세히 보기</button>
<!-- 
    aria-controls="details": id#details를 컨트롤하고 있음
    aria-details="more-info": 버튼과 연결된 추가 정보가 id#more-info 요소에 있음
 -->
<div id="details" aria-labelledby="details-title" aria-hidden="true">
    <h2 id="details-title">추가 정보</h2>
    <p id="more-info">이 버튼을 누르면 자세한 정보가 표시됩니다.</p>
</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-flowto
> 현재 요소의 **포커스 이동 경로**를 나타내는 데 사용

주로 ```순차적인 탐색```이 필요한 경우나 ```대화형 위젯```에서 사용됨

```html
<label for="name">이름:</label>
<input type="text" id="name" aria-flowto="email">
<!-- 다음 포커스 이동 필드는 input#email -->

<label for="email">이메일:</label>
<input type="email" id="email" aria-flowto="message">
<!-- 다음 포커스 이동 필드는 textarea#message -->

<label for="message">메시지:</label>
<textarea id="message" aria-flowto="submit"></textarea>
<!-- 다음 포커스 이동 필드는 button#submit -->

<button type="submit" id="submit">제출</button>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-labelledby
> 현재 요소의 **레이블로 사용될 요소의 ID**를 지정 <br/>
> **해당 텍스트 영역과 현재 요소를 연결**할 때 사용됨 <br/>
> 레이블을 지정하는 대상이 레이블을 지정하는 주제로 참조. 네이티브 레이블링 매커니즘을 무시하므로 *aria-labelledby내용이 최우선*이 됨

* ```라벨을 명시적으로 제공할 필요가 있는 경우```: 라벨이 엘리먼트와 분리되어 있거나, 보이지 않을 경우 사용
* ```다른 엘리먼트에서 생성된 라벨 사용시```: <label>로 연결된 라벨 사용 대신 타 엘리먼트에서 생성된 라벨을 사용할 때
* ```다국어 지원```: 여러 언어로 라벨 제공할 때
* ```컨트롤과 연관된 라벨```: 버튼이나 입력 필드와 같은 컨트롤에 대한 설명 제공

```html
<button id="schedule-button">스케줄 조회</button>
<div id="schedule-info" aria-labelledby="schedule-button">
    이 버튼을 클릭하여 스케줄을 조회할 수 있습니다.
</div>
<!-- 
    aria-labelledby="schedule-button": 
    div#schedule-info 요소가 스케줄 조회 버튼인 button#schedule-button과 연관되어 정보를 제공함 
-->

<label id="username-label">사용자 이름:</label>
<input type="text" aria-labelledby="username-label">
<!-- 
    username-label를 사용함으로써 
    사용자 이름 입력 필드에 '사용자 이름'이라는 레이블이 있음을 나타냄 
-->
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-owns
> 현재 요소가 **직접 소유한 하나 이상의 요소의 ID**를 나타냄
 
주로 ```팝업```이나 ```대화 상자```같은 컨테이너 요소가 그 안에 있는 요소들을 소유할 때 사용됨

```html
<div id="popup" role="dialog" aria-labelledby="popup-title" aria-owns="popup-content">
    <h2 id="popup-title">알림</h2>
    <div id="popup-content">이 내용은 팝업에 속합니다.</div>
</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-posinset
> 현재 요소가 속한 **컬렉션에서의 위치**를 나타냄
 
주로 ```목록```이나 ```그리드```같은 요소에서 사용되며, 현재 요소가 해당 컬렉션에서 *몇 번째에 위치*하는지 명시적으로 지정하여, 보조 기기 사용자에게 해당 요소의 순서를 알려줌 

```html
<table role="grid">
    <tr>
        <td role="gridcell" aria-posinset="1">셀 1</td>
        <td role="gridcell" aria-posinset="2">셀 2</td>
        <td role="gridcell" aria-posinset="3">셀 3</td>
    </tr>
</table>
```

> **역할 사용** [article](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#article) | [listitem](listitem) | [menuitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitem) | [option](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#option) | [radio](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#radio) | [tab](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tab) <br/>
> **역할 상속** [menuitemcheckbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitemcheckbox) | [menuitemradio](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitemradio) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader) | [treeitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treeitem)

<br/>

### aria-rowcount
> 그리드나 테이블과 같은 요소에서 **전체 행의 수**를 나타냄 
 
정수 값을 가지며, 컬렉션 내의 전체 행의 수를 나타냄. 주로 ```그리드```나 ```테이블```같은 요소에서 사용되며, 현재 **표시되는 행의 수가 전체 행의 수와 다를 때** 사용됨

```html
<table role="grid" aria-rowcount="5">
    <!-- 그리드가 총 5개의 행을 가지고 있음 -->
    <tr>
        <td role="gridcell">셀 1</td>
        <td role="gridcell">셀 2</td>
        <td role="gridcell">셀 3</td>
    </tr>
    <!-- 나머지 행들 -->
</table>
```

> **역할 사용** [table](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#table) <br/>
> **역할 상속** [grid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#grid) | [treegrid](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treegrid)


<br/>

### aria-rowindex
> 그리드나 테이블과 같은 요소에서 **현재 행의 인덱스**를 나타냄

정수 값을 가지며, 컬렉션 내의 현재 행의 수를 나타냄. 주로 ```그리드```나 ```테이블```같은 요소에서 사용되며, 현재 **특정 행의 위치를 지정**힐 때 사용됨

```html
<table role="grid">
    <tr role="row" aria-rowindex="1">
        <!-- 첫번째 행 -->
        <td role="gridcell">셀 1</td>
        <td role="gridcell">셀 2</td>
        <td role="gridcell">셀 3</td>
    </tr>
    <tr role="row" aria-rowindex="2">
        <!-- 두번째 행 -->
        <td role="gridcell">셀 4</td>
        <td role="gridcell">셀 5</td>
        <td role="gridcell">셀 6</td>
    </tr>
    <!-- 나머지 행들 -->
</table>
```

> **역할 사용** [cell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#cell) | [row](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#row) <br/>
> **역할 상속** [columnheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#columnheader) | [gridcell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#gridcell) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader)


<br/>

### aria-rowspan
> 테이블의 셀이 **세로 방향으로 확장되는 행의 수**를 나타냄 <br/>
> 정수 값을 가지며, 특정 셀이 여러 행에 걸쳐 있는 경우 사용됨. 해당 셀이 몇 개의 행을 차지하는지 보조 기기에게 알려줌
 
```html
<table>
    <tr>
        <td>셀 1</td>
        <td rowspan="2">셀 2와 3</td>
        <!-- 브라우저가 테이블을 그릴 때 사용되는 rowspan이 aria-rowspan과 동일한 역할을 함 -->
        <td>셀 4</td>
    </tr>
    <tr>
        <td>셀 5</td>
        <td>셀 6</td>
    </tr>
</table>
```

> **역할 사용** [cell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#cell) <br/>
> **역할 상속** [columnheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#columnheader) | [gridcell](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#gridcell) | [rowheader](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#rowheader)


<br/>

### aria-roledescription
> 요소의 역할(role)을 설명하는 **추가 정보**를 제공, **정해진 요소의 역할을 더 명확하게 만드는 데 사용**

* 역할 설명에 대한 속성, 장문의 설명이 아닌 **요소의 역할을 명확하게 세분화**하기 위해 사용. 요소의 의미를 무시하고 덮어씌움
* aria나 네이티브 html에서 정의된 요소 유형에 해당되어야 함
* 되도록 **사용자 상호작용이 없는 요소**에 사용하는 것이 바람직함
    * Android에서는 제대로 지원하지 않음. 의도와 다르게 읽힐 수 있음을 주의해야 함
* **컴포넌트에 대한 지역화** 필요
    * 접속 사용자의 기기, 국가별 언어 반드시 고려 필요. 언어별로 텍스트를 다르게 준다면 해결됨

```html
<!--
    배너로 커스텀한 a태그, aria-roledescription="Banner link" 부가 설명 추가
-->
<a href="...." aria-roledescription="Banner link"> 가을 난방 30% 할인 </a>

<!--
    버튼으로 커스텀한 div를 role="button" 지정
    aria-roledescription="커스텀 버튼" 부가 설명 추가 
-->
<div role="button" aria-roledescription="커스텀 버튼">클릭하세요</div>
```

> **역할 사용** 기본 마크업의 모든 요소에서 사용 가능

<br/>

### aria-setsize
> **현재 요소가 속한 그룹이나 집합의 전체 크기(총 요소 수)**를 나타냄

주로 ```리스트```나 ```그리드```같은 요소에서 사용되며, 현재 요소가 속한 집합의 전체 크기를 지정할 때 사용됨. 정수 값을 가지며 현재 요소가 속한 *집합의 전체 요소 수*를 나타냄.

```html
<table role="grid">
    <tr>
        <td role="gridcell" aria-setsize="3">셀 1</td>
        <td role="gridcell" aria-setsize="3">셀 2</td>
        <td role="gridcell" aria-setsize="3">셀 3</td>
        <!-- 해당 행이 가지고 있는 셀의 수가 3 -->
    </tr>
    <tr>
        <td role="gridcell" aria-setsize="4">셀 4</td>
        <td role="gridcell" aria-setsize="4">셀 5</td>
        <td role="gridcell" aria-setsize="4">셀 6</td>
        <td role="gridcell" aria-setsize="4">셀 7</td>
        <!-- 해당 행이 가지고 있는 셀의 수가 4 -->
    </tr>
</table>

```

> **역할 사용** [article](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#article) | [listitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#listitem) | [menuitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitem) | [option](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#option) | [radio](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#radio) | [tab](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#tab) <br/>
> **역할 상속** [menuitemcheckbox](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitemcheckbox) | [menuitemradio](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#menuitemradio) | [treeitem](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md#treeitem)

<br/>
