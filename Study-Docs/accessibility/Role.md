# table


## Abstract(추상적)
> 일반적인 역할 개념을 정의할 목적으로 WAI-ARIA 역할 모델을 지원하는 데 사용

### command
> 작업을 수행하지만 입력 데이터를 수신하지 않는 위젯 형태
> 사용자가 실행할 수 있는 명령(커맨드)을 나타내는 역할을 지정
> 사용자 인터페이스의 커맨드 버튼 또는 링크와 관련하여 사용 **사용자에게 어떤 동작을 실행할 수 있다는 시각적 힌트를 제공**

e.g. 커맨드 버튼이나 링크를 사용하여 ```저장```, ```전송```, ```추가```와 같은 동작을 수행

```html
<button role="command" onclick="saveData()">저장</button>
// 버튼은 사용자가 클릭하여 데이터를 저장할 수 있는 명령을 나타냄
```

<br/>

### composite
> 탐색 가능한 하위 항목 또는 소유된 하위 항목을 포함할 수 있는 위젯
> 사용자 정의 위젯이나 복합 컴포넌트를 보다 명확하게 설명 가능
> 복합적인 구조를 스크린 리더와 같은 보조 기술에게 전달할 수 있음, 이를 통해 사용자가 해당 위젯의 구성 요소와 기능을 이해하고 조작할 수 있음

e.g. 사용자 정의 콤보박스, 다중 선택 목록 

```html
<div role="composite" aria-labelledby="composite-label"> // 복합 위젯을 나타냅니다. 이 위젯은 다른 역할이 결합된 구조를 가지고 있으며, 라벨에 의해 식별됨
    <label id="composite-label">컴포지트 위젯</label> // 컴포지트 위젯에 대한 라벨
    <div role="option" aria-selected="false">옵션 1</div> // 위젯 내의 각각의 옵션
    <div role="option" aria-selected="true">옵션 2</div>
    <div role="option" aria-selected="false">옵션 3</div>
</div>

```

<br/>

### input
> 사용자에게 데이터를 입력할 수 있는 입력 필드를 나타내는 WAI-ARIA 속성 ```<input>엘리먼트와 유사한 역할```
> 보조 기술을 사용하는 사용자에게 필드의 의미를 전달하고, 해당 필드가 입력 가능한 역할임을 알려줌
> 커스텀 위젯이나 특정 사용자 인터페이스 요소에서 사용,  텍스트나 데이터를 입력할 수 있는 역할을 정의됨

```html
<div role="input" aria-label="이름을 입력하세요"> //사용자에게 이름을 입력할 수 있는 역할을 나타내는 엘리먼트
    <input type="text" id="name-input" placeholder="이름을 입력하세요"> //실제 텍스트 입력 필드
</div>
```

<br/>

### landmark
> 웹 페이지의 중요한 영역을 나타내는 데 사용, 웹 페이지의 다양한 섹션을 식별하고 해당 섹션의 역할을 설명함
> 작성자가 지정한 특정 목적과 관련이 있고 사용자가 해당 섹션으로 쉽게 이동하고 페이지 요약에 나열할 수 있을 만큼 충분히 중요한 콘텐츠가 포함된 인식 가능한 섹션
> 이러한 페이지 요약은 사용자 에이전트나 보조 기술에 의해 동적으로 생성될 수 있음

e.g. 페이지의 주요 내용, 검색 기능, 메인 네비게이션

role="landmark" | note.
-- | --
```banner``` | 주요 네비게이션 등이 포함된 웹 페이지 상단 부분 e.g. 로고, 사이트 이름
```navigation``` | 사이트 내에서의 주요 네비게이션 e.g. 사이트 메뉴, 사이트 내 링크 
```main``` | 페이지의 주요 콘텐츠. 주로 한 페이지 내에서 중요한 콘텐츠가 들어가는 영역
```complementary``` | 주요 콘텐츠와 관련된 보조 콘텐츠 e.g. 사이드바나 광고, 연관 링크
```contentinfo``` | 페이지의 하단에 위치하는 정보 영역 e.g. 저작권 정보, 연락처, 사이트 링크
```form``` | 폼 요소를 포함하는 영역


```html
<header role="banner">
    <!-- 로고, 사이트 이름, 주요 네비게이션 등 -->
</header>

<nav role="navigation">
    <!-- 메인 네비게이션 -->
</nav>

<main role="main">
    <!-- 페이지의 주요 콘텐츠 -->
</main>

<aside role="complementary">
    <!-- 사이드바, 광고, 연관 링크 등 -->
</aside>

<footer role="contentinfo">
    <!-- 저작권 정보, 연락처, 사이트 링크 등 -->
</footer>
```

<br/>

### range
> 사용자가 범위 내의 값을 선택할 수 있는 조절기(슬라이더)와 같은 역할을 나타냄
> 주로 범위 입력 요소에 사용되며, 사용자가 값을 선택하고 조절할 수 있는 UI 컨트롤

e.g.  사용자가 값의 범위를 선택하고 조절하는 데 사용할 수 있는 슬라이더, 스핀박스

```html
<div role="range" aria-valuemin="0" aria-valuemax="100" aria-valuenow="50" aria-valuetext="50">
    <input type="range" min="0" max="100" value="50">
</div>
```

<br/>

### section
> 웹 페이지 내에서 독립적인 섹션을 나타내는 데 사용
> 일반적으로 콘텐츠를 논리적으로 그룹화하는 데 사용되며, 이 그룹은 주로 제목(<h1> ~ <h6>)과 함께 사용됨
>  논리적으로 관련된 콘텐츠를 그룹화하고 이러한 섹션을 스크린 리더 등의 보조 기술을 사용하는 사용자에게 명시적으로 전달하는 데 사용

```html
<div role="section" aria-labelledby="section-heading">
//aria-labelledby: 섹션의 제목을 식별하는 데 사용됩니다. 여기서는 제목의 ID를 참조하고 있습니다.
    <h2 id="section-heading">공지사항</h2> 
    <p>이번 주에는 새로운 기능이 추가되었습니다!</p>
    <p>새로운 기능을 확인해보세요.</p>
</div>

<div role="section" aria-labelledby="section-heading2">
    <h2 id="section-heading2">이벤트</h2>
    <p>이번 주에는 다양한 이벤트가 준비되어 있습니다.</p>
    <p>참가하고 즐거운 시간을 보내세요.</p>
</div>
```

<br/>

### select
> 사용자가 선택할 수 있는 옵션 목록을 나타내는 WAI-ARIA 속성

e.g. ```드롭다운 메뉴```, ```콤보박스```

```html
<div role="select" aria-labelledby="select-label">
    <span id="select-label">선택하세요:</span>
    <button aria-haspopup="true" aria-expanded="false" aria-controls="select-options">
        선택된 옵션
    </button>
    <ul id="select-options" role="listbox" aria-hidden="true">
        <li role="option">옵션 1</li>
        <li role="option">옵션 2</li>
        <li role="option">옵션 3</li>
    </ul>
</div>
```

<br/>

### widget
> 사용자와 상호 작용할 수 있는 인터랙티브한 UI 요소를 나타내는 데 사용. 사용자와의 인터랙션에 중점을 둠
> > 사용자가 특정 작업을 수행하거나 정보를 제공할 때 사용

e.g.  버튼, 입력 필드, 체크박스, 라디오 버튼 등과 같은 다양한 UI 컨트롤

```html
<div role="widget" aria-label="검색 위젯">
    <input type="text" aria-label="검색어 입력" placeholder="검색어를 입력하세요">
    <button aria-label="검색하기">검색</button>
</div>
```

<br/>

### window
> 웹 페이지나 어플리케이션 내에서 독립적인 윈도우 영역 나타냄
> 스크린 리더와 같은 보조 기술을 사용하는 사용자에게 해당 영역이 모달 다이얼로그나 팝업과 같은 윈도우로 인식될 수 있음
> 현재 상황을 명확히 전달하고, 이 영역이 모달이나 팝업인지 인식하게 해줌

e.g. 모달 다이얼로그, 팝업, 알림, 그리고 다른 윈도우 기반의 UI 요소
```html
<div role="window" aria-labelledby="dialog-title" aria-modal="true">
    <div role="dialog" aria-labelledby="dialog-title" aria-describedby="dialog-description">
        <h2 id="dialog-title">알림</h2>
        <p id="dialog-description">메시지를 확인하시겠습니까?</p>
        <button onclick="closeDialog()">닫기</button>
    </div>
</div>
```



<br/>


***


## Widget (위젯)
> 독립형 사용자 인터페이스 위젯 또는 더 큰 복합 위젯의 일부로 작동

### button
> 클릭하거나 누를 때 사용자가 트리거하는 작업을 허용하는 입력

<br/>

### checkbox
> true, false 또는 혼합의 세 가지 가능한 값이 있는 확인 가능한 입력

<br/>

### gridcell
> 그리드 또는 트리 그리드의 셀

<br/>

### link
> 사용자 에이전트가 해당 리소스를 탐색하게 만드는 내부 또는 외부 리소스에 대한 대화형 참조

<br/>

### menuitem

<br/>

### menuitemcheckbox

<br/>

### menuitemradio

<br/>

### option

<br/>

### progressbar

<br/>

### radio

<br/>

### scrollbar

<br/>

### searchbox

<br/>

### separator 

<br/>

### slider

<br/>

### spinbutton

<br/>

### switch

<br/>

### tab

<br/>

### tabpanel

<br/>

### textbox

<br/>

### treeitem

<br/>

> 복합 사용자 인터페이스 위젯, 일반적으로 포함된 다른 위젯을 관리하는 컨테이너 역할

### combobox
> 사용자가 입력 값을 설정하는 데 도움이 되도록 동적으로 팝업할 수 있는 목록 상자 또는 그리드와 같은 다른 요소를 제어하는 입력

<br/>

### grid
> 방향 화살표 키와 같은 2차원 탐색 방법을 사용하여 그리드의 일부 또는 전체 셀에 초점을 맞출 수 있는, 하나 이상의 셀이 있는 하나 이상의 행 컬렉션을 포함하는 복합 위젯

<br/>

### listbox
> 선택 목록에서 하나 이상의 항목을 선택할 수 있게 해주는 위젯

<br/>

### menu

<br/>

### menubar

<br/>

### radiogroup

<br/>

### tablist

<br/>

### tree

<br/>

### treegrid


***



## Document Structure (문서 구조)
> 페이지의 콘텐츠를 구성하는 구조를 설명

### application
> 하나 이상의 포커스 가능 요소를 포함하는 구조 (e.g. 키보드, 제스처 이벤트)

<br/>

### article
> 문서, 페이지, 사이트 독립적인 부분 구성하는 구성 요소 페이지 섹션

<br/>

### blockquote
> 다른 출처에서 인용한 콘텐츠 섹션

<br/>

### caption
> 그림, 표, 그리드 또는 트리 그리드의 이름을 지정하고 설명할 수도 있는 표시 콘텐츠

<br/>

### cell
> 테이블 형식 컨테이너의 셀

<br/>

### columnheader
> 열의 헤더 정보가 포함된 셀

<br/>

### definition
> 용어 또는 개념의 정의

<br/>

### deletion
> 삭제에는 삭제된 것으로 표시된 콘텐츠 또는 삭제가 제안된 콘텐츠가 포함

<br/>

### document
> 보조 기술 사용자가 읽기 모드에서 탐색할 수 있는 콘텐츠가 포함된 요소

<br/>

### emphasis
> 하나 이상의 강조 문자

<br/>

### feed
> 스크롤하면 목록 끝에서 기사가 추가되거나 제거될 수 있는 스크롤 가능한 기사 목록

<br/>

### figure
> 일반적으로 그래픽 문서, 이미지, 코드 조각 또는 예제 텍스트를 포함하는 인식 가능한 콘텐츠 섹션

<br/>

### generic
> 자체적으로 의미론적 의미가 없는 이름 없는 컨테이너 요소

<br/>

### group
> 보조 기술에 의해 페이지 요약이나 목차에 포함되지 않는 사용자 인터페이스 개체 집합

<br/>

### heading
> 페이지 섹션의 제목

<br/>

### img
> 이미지를 형성하는 요소 컬렉션을 위한 컨테이너

<br/>

### insertion
> 추가됨으로 표시된 콘텐츠 또는 추가가 제안되는 콘텐츠가 포함

<br/>

### list
> 목록 항목 요소를 포함하는 섹션

<br/>

### listitem
> 목록이나 디렉터리의 단일 항목

<br/>

### math
> 수학적 표현을 나타내는 콘텐츠

<br/>

### meter
> 스칼라 측정을 나타내는 요소

<br/>

### none

<br/>

### note

<br/>

### paragraph

<br/>

### presentation

<br/>

### row

<br/>

### rowgroup

<br/>

### rowheader

<br/>

### separator 

<br/>

### strong

<br/>

### subscript

<br/>

### superscript

<br/>

### table

<br/>

### term

<br/>

### time

<br/>

### toolbar

<br/>

### tooltip


***


## Landmark (랜드마크)
> 탐색 랜드마크로 사용되는 페이지 영역, 기본 유형에서 상속
> 모두 역할 속성 [ROLE-ATTRIBUTE]에서 가져옴, WAI-ARIA 역할 모델의 일부로 명확하게 만들기 위해 포함

### banner
> 주로 사이트 중심 콘텐츠를 포함

<br/>

### complementary
> DOM 계층 구조의 유사한 수준에서 기본 콘텐츠를 보완하도록 설계되었지만 기본 콘텐츠와 분리되어도 의미를 유지

<br/>

### contentinfo
> 상위 문서에 대한 정보가 포함된 랜드마크 영역

<br/>

### form
> 전체적으로 결합하여 양식을 생성하는 항목 및 객체의 컬렉션을 포함하는 랜드마크 영역

<br/>

### main
> 문서의 주요 내용을 포함하는 랜드마크

<br/>

### navigation

<br/>

### region

<br/>

### search


***



## Live Region (라이브 지역)
> 라이브 영역 속성에 의해 수정될 수 있음

### alert
> 중요도가 높고 시간에 민감한 정보가 포함된 라이브 영역
> 1. 실시간으로 사용자에게 알려야 할 중요한 정보가 있는 경우
> 2. 사용자의 주의를 요하는 긴급 상황

```경고``` : 사용자에게 즉시 중요할 수 있는 메세지를 전달
e.g. 폼 제출 후 오류가 발생했거나, 중요한 경고 메시지를 표시해야 할 때
     온라인 상점에서 장바구니에 제품을 추가할 때 장바구니에 추가되었음을 알릴 때

```html
<div role="alert">
    잘못된 이메일 형식입니다. 올바른 형식으로 입력해주세요.
</div>
```

<br/>

### log
> 새로운 정보가 의미 있는 순서대로 추가되고, 오래된 정보는 사라질 수 있는 일종의 라이브 영역

<br/>

### marquee
> 필수적이지 않은 정보가 자주 변경되는 라이브 영역 유형

<br/>

### status

<br/>

### timer


***



## Window (창)
> 브라우저 또는 애플리케이션 내에서 창 역할

### alertdialog
> 초기 초점이 대화 상자 내의 요소로 이동, 경고 메세지가 포함된 대화상자 유형

<br/>

### dialog
> 대화 상자는 웹 애플리케이션 기본 창의 하위 창
> html 페이지의 경우, 기본 애플리케이션 창 = 전체 웹문서(body요소)

