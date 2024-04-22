# 요소의 속성

## aria-live
>  사용자들에게 새로운 콘텐츠나 상태 변경을 실시간으로 알려주는 데 사용
> 특정한 영역이나 엘리먼트가 업데이트되는 경우, 그 변경사항을 즉시 알려주는 역할

token | note
-- | --
```off(default)``` | 실시간 업데이트를 알리지 않아야 함(변경사항이 사용자에게 중요하지 않을 때 사용)
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

## aria-roleDescription
> 요소의 역할(role)을 커스터마이징 하여 전달함, **정해진 요소의 역할을 더 명확하게 만드는 데 사용**

* 역할 설명에 대한 속성, 장문의 설명이 아닌 **요소의 역할을 명확하게 세분화**하기 위해 사용. 요소의 의미를 무시하고 덮어씌움
* aria나 네이티브 html에서 정의된 요소 유형에 해당되어야 함
* 되도록 **사용자 상호작용이 없는 요소**에 사용하는 것이 바람직함
    * Android에서는 제대로 지원하지 않음. 의도와 다르게 읽힐 수 있음을 주의해야 함
* **컴포넌트에 대한 지역화** 필요
    * 접속 사용자의 기기, 국가별 언어 반드시 고려 필요. 언어별로 텍스트를 다르게 준다면 해결됨

```html
<a href="...." aria-roledescription="Banner link"> 가을 난방 30% 할인 </a>
```

## aria-controls
> 사용자 인터페이스 요소 간의 관계를 명시하고 전달하는데 사용.
> 일반적으로 대화형 컴포넌트, 위젯에서 사용됨. 버튼 클릭시 관련 패널이 열리는 경우 사용 가능.

* 콘텐츠 연결: 밀접하게 연관된 요소의 관계를 명시적으로 나타내야 할 때
* 상호작용 요소 제어: 다른 요소의 동작을 제어하거나 영향을 미칠 때

```html
<ul role="tablist">
    <li role="tab" aria-selected="true" aria-controls="a1" tabindex="0" id="tab1">tab1</li>
    <li role="tab" aria-selected="false" aria-controls="b1" tabindex="-1" id="tab2">tab2</li>
</ul>
<div role="tabpanel" aria-labelledby="tab1" aria-expanded="true" tabindex="0" id="a1">
    tab1 내용
</div>
```
> 탭이 관리하는 탭 패널의 ID값을 넣어주고, 탭을 클릭하여 패널이 expanded되었을 때 초점이 이동하도록 tabindex=0을 부여해줌

## aria-lable
> html 요소에 접근 가능한 **설명용 텍스트**를 넣을 수 있음

* 이미지를 사용해 시각적인 표현을 할 경우 대체 텍스트 역할

## aria-labelledby
> 요소의 레이블로서 DOM에 있는 다른 요소의 ID를 지정 가능함. **해당 텍스트 영역과 현재 요소를 연결**할 때 사용됨
> 레이블을 지정하는 대상이 레이블을 지정하는 주제로 참조. 네이티브 레이블링 매커니즘을 무시하므로 aria-labelledby내용이 최우선이 됨

* 라벨을 명시적으로 제공할 필요가 있는 경우: 라벨이 엘리먼트와 분리되어 있거나, 보이지 않을 경우 사용
* 다른 엘리먼트에서 생성된 라벨 사용시: <label>로 연결된 라벨 사용 대신 타 엘리먼트에서 생성된 라벨을 사용할 때
* 다국어 지원: 여러 언어로 라벨 제공할 때
* 컨트롤과 연관된 라벨: 버튼이나 입력 필드와 같은 컨트롤에 대한 설명 제공

```html
<button id="schedule-button">스케줄 조회</button>
<div id="schedule-info" aria-labelledby="schedule-button">
    이 버튼을 클릭하여 스케줄을 조회할 수 있습니다.
</div>
```
>  ```div#schedule-info``` 엘리먼트는 스케줄 조회 버튼과 연관된 정보를 제공함. 
