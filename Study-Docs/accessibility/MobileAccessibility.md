# 모바일 애플리케이션 콘텐츠 접근성 지침 2.0

## Table of Contents
1. [인식의 용이성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#인식의-용이성)
     1. [자막, 수화 등의 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#자막-수화-등의-제공)
     2. [대체 텍스트](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#대체-텍스트)
     3. [색에 무관한 인식](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#색에-무관한-인식)
     4. [명도 대비](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#명도-대비)
     5. [명확한 지시 사항](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#명확한-지시-사항)
     6. [알림 기능](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#알림-기능)
2. [운용의 용이성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#운용의-용이성)
     1. [초점](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#초점)
     2. [누르기 동작 지원](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#누르기-동작-지원)
     3. [응답 시간 조절](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#응답-시간-조절)
     4. [정지 기능 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#정지-기능-제공)
     5. [컨트롤의 크기와 간격](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#컨트롤의-크기와-간격)
3. [이해의 용이성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#이해의-용이성)
     1. [입력 도움](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#입력-도움)
     2. [사용자 인터페이스의 일관성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#사용자-인터페이스의-일관성)
     3. [깜박거림의 사용 제한](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#깜박거림의-사용-제한)
     4. [자동재생 금지](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#자동재생-금지)
     5. [예측가능성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#예측가능성)
4. [견고성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#견고성)
     1. [폰트 관련 기능의 활용](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#폰트-관련-기능의-활용)
     2. [보조 기술과의 호환성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/MobileAccessibility.md#보조-기술과의-호환성)

***

## 인식의 용이성
> 사용자가 장애 유무 등에 관계 없이 애플리케이션의 모든 콘텐츠를 동등하게 인식할 수 있도록 제공하는 것을 의미함

### 자막, 수화 등의 제공
> 영상이나 음성 콘텐츠에는 동등한 내용의 자막, 원고 또는 수화가 제공되어야 한다.
   1. 텍스트 아닌 콘텐츠에 대한 대체 텍스트는 그 의미나 기능을 동등한 수준으로 짧고 명확하게 제공해야 함

<br/>

### 대체 텍스트
> 텍스트 아닌 콘텐츠는 대체 가능한 텍스트와 함께 제공되어야 한다.
    1. 영상이나 음성 콘텐츠 내 제공되는 모든 음성정보는 동등한 내용의 자막, 원고, 수화 중 적어도 하나 이상을 제공해야 함
    2. 영상이나 음성 콘텐츠에서 화면에 문자 정보가 의미를 가지고 있는 경우 이를 설명하는 별도의 음석 콘텐츠나 원고를 제공해야 함
    3. 자막, 원고 또는 수화는 재생되고 있는 영상이나 음성 콘텐츠와 동기화하여 제공. <br/>
      단, 신시간으로 제공되는 영상이나 음성 콘텐츠의 경우는 실시간 자막 또는 수화로 제공할 수 있음.
    4. 음성이나 문자정보 없이 제공되는 영상이나 음성 콘텐츠는 이를 설명하는 화면 해설을 제공하는 것이 바람직함

<br/>

### 색에 무관한 인식
> 화면에 표시되는 모든 정보는 색에 관계없이 인식될 수 있어야 한다.
   1. 콘텐츠에서 제공하는 모든 정보는 특정한 색을 구별할 수 없는 사용자, 흑백 디스플레이 사용자, 흑백 디스플레이 사용자, 흑백 인쇄물을 보는 사용자 및 고대비 모드 사용자가 인식할 수 있도록 제공해야 함

<br/>

### 명도 대비
> 화면에 표시되는 모든 사용자 인터페이스 컴포넌트와 텍스트는 전경색과 배경색이 구분될 수 있도록 제공되어야 한다.
   1. 화면에 표시되는 모든 사용자 인터페이스 컴포넌트와 텍스트는 전경색과 배경색이 구분될 수 있도록 명도 대비를 3:1 이상으로 제공해야 함

<br/>

### 명확한 지시 사항
> 지시 사항은 모양, 크기, 위치, 방향, 색, 소리 등에 관계없이 인식될 수 있어야 한다.
   1. 화면에 표시되는 특정 사용자 인터페이스 컴포넌트를 가리키거나 지시 사항을 전달하는 콘텐츠의 경우 가리키고자 하는 사용자 인터페이스 컴포넌트의 실제 명칭이나 그 사용자 인터페이스 컴포넌트가 포함하고 있는 대체 텍스트를 사용해 지칭하거나, 하나의 감각에 의존하지 않고 여러 감각을 이용하는 정보를 함께 제공해야 함
   2. 음성이나 음향을 사용해 지시 사항을 전달하는 경우 사용자가 소리를 들을 수 없더라도 지시 사항을 인식할 수 있어야 함

<br/>

### 알림 기능
> 알림 정보는 화면 표시, 소리, 진동 등 다양한 방법으로 제공되어야 한다.
   1. 중요한 알림 정보는 시각, 청각, 촉각 등 다양한 감각으로 인식될 수 있어야 함
   2. 알림 정보는 사용자가 자신에게 적합한 방법을 선택할 수 있도록 제공하는 것이 바람직함


<br/><br/>


## 운용의 용이성
> 사용자가 장애 유무 등에 관계없이 애플리케이션에서 제공하는 모든 기능들을 운용할 수 있게 제공하는 것을 의미함

### 초점
> 의미나 기능을 갖는 모든 사용자 인터페이스 컴포넌트에는 초점(focus)이 적용되고, 초점은 논리적인 순서로 이동되어야 한다. 
   1. 초점은 사용자가 예측할 수 있도록 논리적인 순서로 이동해야 함
   2. 초점은 화면에서 보이지 않거나 논리적으로 의미를 갖지 않는 사용자 인터페이스 컴포넌트로 이동하지 않도록 해야 함
   3. 표시되는 초점의 영역은 콘텐츠의 위치와 크기가 맞고록 제공해야 함

<br/>

### 누르기 동작 지원
> 터치(touch) 기반 모바일 기기의 모든 컨트롤은 누르기 동작으로 제어할 수 있어야 한다. 
   1. 두 개 이상의 손가락을 동시에 이용해야 하는 다중 누르기(multi-touch)동작, 팬(pan), 끌기와 놓기(drag and drop) 등의 복잡한 누르기 동작은 단순한 누르기 동작을 함께 제공해야 함

<br/>

### 응답 시간 조절
> 시간 제한이 있는 콘텐츠는 응답 시간을 조절할 수 있어야 한다. 
   1. 시간 제한이 있는 경우, 제한 시간 연장 또는 이를 제어할 수 있는 수단을 함께 제공해야 함
   2. 불가피한 사유로 시간 연장 기능을 제공할 수 없는 경우, 사용자에게 시간 제한이 있다는 것을 미리 알려주고 종료되었을 경우에도 이를 알려야 함 <br/>
      * 불가피한 경우: 보안, 게임 등

<br/>

### 정지 기능 제공
> 자동으로 변경되는 콘텐츠는 움직임을 제어할 수 있어야 한다. 
    1.  자동으로 변경되는 콘텐츠에는 앞으로 이동, 뒤로 이동, 일시 정지, 정지와 같이 이를 제어할 수 있는 수단을 제공해야 함

<br/>

### 컨트롤의 크기와 간격
> 컨트롤은 충분한 크기와 간격으로 제공되어야 한다. 
    1.  컨트롤 간에 외곽선을 표시하지 않는 경우 컨트롤 간의 중심 간 간격을 충분히 제공해야 함 <br/>
        * 기본 사용자 인터페이스 컴포넌트와 같이 운영체제에게 기본적으로 제공하는 컨트롤의 경우 예외로 함
    2. 모바일 기기의 화면 크기에 관계없이 컨트롤의 가로와 세로 크기는 각각 9mm 이상으로 제공하는 것이 바람직함 


<br/><br/>


## 이해의 용이성
> 사용자가 장애 유무 등에 관계없이 애플리케이션에서 제공되는 콘텐츠를 이해할 수 있도록 제공하는 것을 의미함

### 입력 도움
> 입력 서식 이용 시, 입력 오류를 방지하거나 정정할 수 있는 방법을 제공해야 한다.
    1.  입력 서식에는 용도와 목적을 알 수 있는 대체 정보를 제공해야 함
    2.  별도의 입력 방식이 있는 입력 서식에는 입력 오류를 방지하기 위해 입력내용에 대한 설명 정보를 제공해야 함
    3.  사용자 입력 값에 오류가 있는 경우 오류 내용을 이해하고 이를 정정할 수 있도록 해당 오류 내용을 알릴 수 있는 방법을 제공해야 함
    4.  입력 서식의 오류 내용을 수정하기 용이하도록 오류가 ㅂ라생된 지점으로 초점을 이동시키는 것이 바람직함

<br/>

### 사용자 인터페이스의 일관성
> 사용자 인터페이스 컴포넌트들은 일관성 있게 배치되어야 한다.
    1.  화면에 표시되는 콘텐츠들의 배치는 일관성 있게 제공되어야 함
    2.  애플리케이션 내의 유사한 기능을 가지고 있는 컨트롤은 동일하게 제공되어야 함

<br/>

### 깜박거림의 사용 제한
> 깜빡이거나 번쩍이는 콘텐츠를 제공하지 않아야 한다.
    1.  화면상에서 깜빡임의 효과를 제공해야 하는 콘텐츠는 초당 3~50회의 주기는 피해 제공하는 것이 바람직함
    2.  불가피하게 사용할 경우, 깜빡임을 제공하는 콘텐츠는 사전에 알리고 회피할 수 있는 법을 제공해야 함

<br/>

### 자동재생 금지
> 자동으로 재생되는 배경음을 사용하지 않아야 한다.
    1.  자동으로 재생되는 배경음은 제공하지 않아야 함. 단, 3초 미만의 배경음은 예외로 인정
    2.  배경음을 사용할 경우, 사용자가 손쉽게 멈춤, 일시 정지, 음량조절 등과 같이 이를 제어할 수 있는 수단을 제공해야 함

<br/>

### 예측가능성
> 사용자가 의도하지 않는 화면 전환이나 이벤트 등이 실행되는 경우 사용자가 이해할 수 있는 방법으로 제공되어야 한다.
    1.  화면이 전환되거나 팝업과 같은 이벤트가 실행되는 경우 이를 예측할 수 있는 방법을 제공해야 함
    2.  다른 애플리케이션으로 연결 및 전환되는 경우 이를 예측할 수 있는 방법을 제공해야 함


<br/><br/>


## 견고성
> 사용자가 기술에 관계없이 애플리케이션에서 제공하는 콘텐츠를 이용할 수 있도록 제공하는 것을 의미함

### 폰트 관련 기능의 활용
> 텍스트 콘텐츠는 운영체제에서 제공하는 폰트 관련 기능을 활용할 수 있는 방법을 제공해야 한다.
    1.  텍스트 콘텐츠는 폰트 크기의 조절이 가능하도록 제공되어야 함 <br/>
        * 폰트 크기 조절 시 화면 레이아웃이 유지될 수 있는 범위 내에서 적용
    2.  폰트 관련 기능을 활용할 수 있도록 범용폰트를 활용하는 것이 바람직함

<br/>

### 보조 기술과의 호환성
> 사용자 인터페이스 컴포넌트는 보조 기술을 이용하여 사용할 수 있도록 해야 한다.
    1.  운영체제에서 제공하는 기본 사용자 인터페이스 컴포넌트를 최대한 이용하는 것이 바람직함
    2.  부득이하게 기본 사용자가 인터페이스 컴포넌트를 사용할 수 없을 시, 운영체제에서 제공하는 보조 기술을 사용할 수 있도록 해야 함
    3.  기본 컴포넌트를 원래의 기능과 다른 기능으로 제공할 경우 사용자가 컨트롤의 기능을 이해할 수 있도록 그 기능에 대한 정보를 제공해야 함
