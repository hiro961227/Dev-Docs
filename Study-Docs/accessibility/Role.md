# table


## Abstract(추상적)
> 일반적인 역할 개념을 정의할 목적으로 WAI-ARIA 역할 모델을 지원하는 데 사용

### command
> 작업을 수행하지만 입력 데이터를 수신하지 않는 위젯 형태

<br/>

### composite
> 탐색 가능한 하위 항목 또는 소유된 하위 항목을 포함할 수 있는 위젯

<br/>

### input
> 사용자 입력을 허용하는 일반적인 유형의 위젯

<br/>

### landmark
> 작성자가 지정한 특정 목적과 관련이 있고 사용자가 해당 섹션으로 쉽게 이동하고 페이지 요약에 나열할 수 있을 만큼 충분히 중요한 콘텐츠가 포함된 인식 가능한 섹션
> 이러한 페이지 요약은 사용자 에이전트나 보조 기술에 의해 동적으로 생성될 수 있음

<br/>

### range

<br/>

### roletype

<br/>

### section

<br/>

### sectionhead

<br/>

### select

<br/>

### structure

<br/>

### widget

<br/>

### window


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

