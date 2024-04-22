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
