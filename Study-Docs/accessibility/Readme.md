
# 웹 접근성(Web Accessibility)
> 장애인, 고령자 등 ***모든 사람들***이 웹 사이트에서 제공하는 정보를 **동등하게 접근하고 이용**할 수 있도록 보장

<br/>

## <W3C 웹 접근성 이니셔티브(WAI) 지침>
> 여러 요소들에서 접근성을 위한 대체 텍스트를 어떻게 사용할지 정의함
***

## [웹 콘텐츠 접근성 지침(WCAG)2.2](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md)
> 장애가 있는 사람들이 웹 콘텐츠에 더 쉽게 접근할 수 있도록 지원하는 방법에 관한 국제 표준 <br/>
> 웹 콘텐츠에 대해 설명하고, 개발자, 저작 도구, 접근성 검사 도구에 주로 적용됨 <br/>
> 2.2 표준에는 인식의 용이성, 운용의 용이성, 이해의 용이성, 견고함 네 가지 지침을 가지고 있음 <br/>

<br/>

## 웹 저작 도구 접근성 지침(ATAG)
> 저작도구의 접근성을 보장하여 장애가 있는 사용자가 웹 콘텐츠를 생산할 수 있도록 함 <br/>
> 저자가 더 접근성 좋은 웹 콘텐츠를 생산하도록 도움 <br/>
> ※ ```저작도구```: 저자(웹 개발자, 디자이너, 작가 등)가 웹 콘텐츠를 생산하는 데 사용하는 서비스나 소프트웨어를 가리킴 e.g. html에디터, 콘텐츠 관리 시스템(CMS), 블로그나 소셜 네트워킹 사이트

<br/>

## 사용자 에이전트 접근성 지침(UAAG)
> UAAG를 따르는 사용자 에이전트는 자체 사용자 인터페이스와 보조 기술을 비롯한 다른 **기술과의 통신을 통해 접근성을 향상시킴** <br/>
> UAAG는 주로 웹 브라우저, 확장, 미디어 플레이어, 리더 및 웹 콘텐츠를 렌더링하는 *응용 프로그램의 개발자*를 위한 것 <br/>
> ※ ```사용자 에이전트```: 브라우저, 브라우저 확장프로그램, 미디어 플레이어, 리더기와 같은 웹 콘텐츠를 제공하는 어플리케이션을 포함함

<br/>


# WAI-ARIA
> Web Accessibility Initiative – Accessible Rich Internet Applications <br/>
> 웹 접근성을 담당하는 조직 - 리치 인터넷을 위한 W3C 접근성 명세 <br/><br/>
> 웹 콘텐츠와 애플리케이션의 접근성과 상호 운용성을 향상시키기 위한 프레임워크를 제공하는 기술 사양 <br/>
> W3C 에서 정의한 기술로 웹 접근성을 위해 지원되는 여러 가지 특성들을 의미 <br/>
> 역할(Role), 속성(Property), 상태(State) 정보를 추가할 수 있음

<br/>

## [역할 - Role](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Role.md)
> 컴포넌트, html요소 내 ```역할``` 정의, 보조 기술에게 정보를 제공함 <br/>
> * **반드시 올바른 역할**을 지정해야 하며 html요소가 이미 적절한 역할을 가지고 있는 경우, 추가 정의할 필요가 없음.

<br/>

## [속성 - Property](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Property.md)
> 요소의 ```특징```이나 ```상황```같은 ```정적인 정보```를 나타냄. ***요소의 상태***나 ***상호 작용에 따라 자주 변하지 않는 정보***를 의미함. <br/>
> 해당 요소의 ```특성```이나 상황 정리. 보조 기술이 요소를 이해하고 조작할 수 있도록 도움. <br/>
> 보통 단일값으로 정의됨

<br/>

## [상태 - State](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/State.md)
> ```컴포넌트 상태 정보```를 정의. <br/>
> 요소의 ```동적인 상태```나 ```상호 작용```에 관련된 정보를 나타냄. ***사용자의 상호 작용에 따라 변할 수 있는 정보***를 의미함. <br/>
> 주로 ```요소의 상태```를 설명하고, 보조 기술이 요소의 **변화를 실시간으로 인식**할 수 있도록 도움. <br/>
> 보통 여러 값을 가질 수 있음 <br/>
> 자바스크립트를 사용해 상황에 맞게 변경할 수 있음 

<br/>

<br/>

## accessibilityLabel
> 웹 개발과 모바일 애플리케이션 개발에서 사용자 인터페이스 요소에 대한 접근성을 높이기 위해 사용되는 속성

주로 스크린 리더와 같은 보조 기술이 사용자에게 요소의 목적이나 기능을 설명할 수 있도록 돕는 데 사용됨. <br/>
웹에서 해당 비슷하게 수행되는 속성들로는 ```aria-label``` ```aria-labelledby``` ```aria-describedby``` 등이 있음 <br/><br/>

```accessibilityLabel```는
- 스크린 리더를 사용하는 사용자에게 명확하고 유용한 정보를 제공해 UI요소의 용도를 이해하기 쉽도록 **사용자 경험을 개선** 시킴
- 웹 콘텐츠 접근성 지침(WCAG)과 같은 **접근성 표준을 준수**하는 데 도움
- 다양한 능력을 가진 사용자들이 웹 애플리케이션이나 모바일 앱을 더 쉽게 사용할 수 있도록 **포용성을 강화**함

<br/>


***

> [Role 참고 사이트](https://www.w3.org/TR/wai-aria/#roles_categorization) <br/>
> [Property, State 참고 사이트](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes) <br/>
> [wai-aria 1.1 참고](https://www.digitala11y.com/wai-aria-1-1-cheat-sheet/) <br/>
> [W3C접근성 기준 개요](https://www.w3.org/WAI/standards-guidelines/ko)
