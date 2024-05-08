# 요소의 상태
## Table of Contents
1. [Live region attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#live-region-attributes)
    1. [aria-busy](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-busy)
    2. [aria-live](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-live)
    3. [aria-relevant](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-relevant)
    4. [aria-atomic](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-atomic)
2. [Drag-and-Drop attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#drag-and-drop-attributes)
    1. [aria-dropeffect](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-dropeffect)
    2. [aria-grabbed](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-grabbed)
3. [Relationship attributes](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#relationship-attributes)
    1. [aria-activedescendant](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-activedescendant)
    2. [aria-colcount](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-colcount)
    3. [aria-colindex](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-colindex)
    4. [aria-colspan](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-colspan)
    5. [aria-controls](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-controls)
    6. [aria-describedby](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-describedby)
    7. [aria-details](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-details)
    8. [aria-flowto](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-flowto)
    9. [aria-labelledby](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-labelledby)
    10. [aria-owns](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-owns)
    11. [aria-posinset](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-posinset)
    12. [aria-rowcount](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-rowcount)
    13. [aria-rowindex](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-rowindex)
    14. [aria-rowspan](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-rowspan)
    15. [aria-roledescription](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-roledescription)
    16. [aria-setsize](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md#aria-setsize)

<br/>

___
___
___

<br/>

## Live region attributes
> 동적으로 업데이트되는 콘텐츠 설명
> ``` ※ Live Region: 화면에 표시되는 동안 업데이트되는 콘텐츠를 보조 기기 사용자에게 즉시 알리는 데 사용 ```

<br/>

### aria-busy
> 사용자 인터페이스가 **현재 작업이 진행 중**임을 나타냄 <br/>
> **동적으로 로딩 중인 상태**나 **사용자가 기다려야 하는 상황**
 
일반적으로 스크립트가 UI 요소의 상태를 업데이트하고 있는 동안 사용되며, 사용자에게 현재 작업이 진행 중임을 시각적으로 알려줌.

token | note
-- | --
```true``` | 현재 작업이 진행 중임을 남타냄
```false``` | ```[default]``` 현재 작업이 진행 중이 아님을 나타냄

```html
<div id="loading" role="status" aria-busy="true">
    로딩 중...
</div>
<!-- 
    작업 중인 상태에서는 화면에 '로딩 중...' 이라는 텍스트가 보여지며
    작업이 완료되면 aria-busy="false"로 설정하여 작업이 완료되었음을 나타낼 수 있음 
-->
```

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

<br/>

### aria-grabbed
> 드래그 앤 드롭 작업에서 **드래그되는 요소의 상태**를 나타냄
 
token | note
-- | --
```true``` | 요소가 드래그되었음을 나타냄
```false``` | 요소가 드래그되지 않았음을 나타냄
```undefined``` | 요소가 드래그 가능한 상태인지 여부를 알 수 없는 경우 사용됨

```html
<div id="draggable" draggable="true" aria-grabbed="false">
    드래그할 요소
</div>
<!-- 
    사용자가 요소를 드래그할 때 
    해당 요소의 aria-grabbed 속성을 변경하여 드래그 상태를 업데이트할 수 있음 
-->
```

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

<br/>
