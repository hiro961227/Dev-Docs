# 웹 접근성
## Table of Contents
1. [인식의 용이성(perceivable)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#인식의-용이성)
   1. [적절한 대체 텍스트 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#적절한-대체-텍스트-제공)
   2. [색에 무관한 콘텐츠 인식](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#색에-무관한-콘텐츠-인식)
   3. [명확한 지시 사항 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#명확한-지시-사항-제공)
   4. [텍스트 콘텐츠의 명도 대비](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#텍스트-콘텐츠의-명도-대비)
   5. [배경음 사용 금지](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#배경음-사용-금지)
   6. [콘텐츠 간의 구분](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#콘텐츠-간의-구분)
2. [운용의 용이성(operable)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#운용의-용이성)
   1. [키보드 사용 보장](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#키보드-사용-보장)
   2. [초점 이동](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#초점-이동)
   3. [조작 가능](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#조작-가능)
   4. [응답 시간 조절](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#응답-시간-조절)
   5. [정지 기능 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#정지-기능-제공)
   6. [깜빡임과 번쩍임 사용 제한](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#깜빡임과-번쩍임-사용-제한)
   7. [반복 영역 건너뛰기](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#반복-영역-건너뛰기)
   8. [제목 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#제목-제공)
   9. [적절한 링크 텍스트](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#적절한-링크-텍스트)
3. [이해의 용이성(understandable)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#이해의-용이성)
   1. [기본 언어 표시](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#기본-언어-표시)
   2. [사용자 요구에 따른 실행](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#사용자-요구에-따른-실행)
   3. [콘텐츠의 선형 구조](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#콘텐츠의-선형-구조)
   4. [표의 구성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#표의-구성)
   5. [레이블 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#레이블-제공)
   6. [오류 정정](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#오류-정정)
4. [견고성(robust)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#견고성)
   1. [마크업 오류 방지](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#마크업-오류-방지)
   2. [웹 애플리케이션 자체 접근성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#웹-애플리케이션-자체-접근성)

<br/>

***
***
***

<br/>

### 인식의 용이성
> 모든 콘텐츠는 사용자가 인식할 수 있어야 한다

<br/>

#### 적절한 대체 텍스트 제공
> 텍스트가 아닌 콘텐츠는 그 의미나 용도를 인식할 수 있도록 **대체 텍스트**를 제공해야 한다.

1) ```img```태그 내 대체 텍스트 ```alt``` 제공

```html
<img src="testImg.jpg" alt="이미지 내부의 텍스트 기재" />
```

2) *IR 기법*으로 숨김 처리를 사용해 대체 텍스트 제공

```html
<a href="#" class="menu">
   <span class="blind">메뉴</span>
</a>
```

3) 의미 없는 이미지(꾸밈 목적 등)에는 대체 텍스트 미제공

```html
<img src="backgroundImg.jpg" alt="" />
```

4) 이모티콘 이미지
```html
<img src="emoticon.png" alt="브라운 캐릭터가 느낌표를 띄우고 있는 이모티콘" />>
```

5) QR코드 이미지
```html
<img src="qr_code.png" alt="QR코드, 네이버 바로가기 https://www.naver.com" />
```

6) 썸내일 이미지
> 이미지에 해당하는 텍스트까지 a태그로 묶어 중복 제공되지 않도록 함
```html
<a herf="#">
   <img src="thumb01.jpg" alt="" />
   <span>썸내일 텍스트</span>
</a>
```

7) 캡차 이미지
```html
<img src="text.jpg" alt="보안문자" />
<button>음성으로 듣기</button>
```

8) 버튼 기능의 특수 문자에 의미를 이해할 수 있는 대체 텍스트 제공
```html
<button aria-pressed="true" title="상세보기 열림 버튼">상세보기</button>
<input type="image" src="next.png" alt="메뉴 더보기" />

<!-- 각기 다른 기능에 적용된 동일한 이미지의 버튼에 대한 대체 텍스트도 정확하게 제공 -->
<img src="next.png" alt="메뉴 더보기" />
<img src="next.png" alt="다음 페이지" />
```

<br/>

#### 자막제공
> 멀티미디어 콘텐츠에는 콘텐츠와 동등한 내용의 ```자막```, ```대본``` 또는 ```수화``` 제공을 해야 함 <br/>
> 주의할 점: **자동 소리 재생 기능 금지**

1) 영상, 이미지 정보를 제공할 경우 시각 정보나 음성 정보에 대해 요약하지 않고 **빠짐없이 전달**해야 함
2) 음성이 나오지 않는 멀티미디어의 경우, **원고** 등의 **대체 콘텐츠를 제공**해야 함
3) 영상의 자막을 시청하거나 음성을 듣기 어려운 경우, *시각*을 통해 내용을 이해할 수 있도록 해야 함 (**수화**를 제공할 경우 충분한 해상도 제공 필요)

<br/>

#### 색에 무관한 콘텐츠 인식
> 특정 색을 구분할 수 없거나, 흑백 디스플레이 사용자와 같이 색상만으로 콘텐츠를 구분할 수 없는 경우가 있기에 콘텐츠는 **색에 관계없이 인식**될 수 있어야 함. *두 가지 이상의 구분자*를 사용하는 것이 좋음

1) 색만으로 구분하지 않고 **색의 의미**를 텍스트로 추가 제공함
2) 그래프의 경우 **모양, 무늬, 굵기, 패턴** 등 다양한 방법으로 구분할 수 있도록 제공하며, 색을 사용할 경우 *색이 의미하고 있는 내용을 추가로 설명*함 
3) 선택 표시를 색으로 구분할 경우 **테두리, 구분선, 밑줄** 등으로 *추가 표시*함
e.g. 슬라이드 버튼, 페이지네이션, 탭 버튼 etc.

<br/>

#### 명확한 지시 사항 제공
> 모양, 크기, 위치, 방향, 색, 소리 등에 관계없이 명확하게 지시 사항을 인식할 수 있어야 함

1) 필수 입력 사항(*)을 표기만 해두지 않음. 상위에 설명문을 추가
```html
<label><i>*</i>아이디(ID)</label>
<span>* 표시는 필수 입력 사항입니다.</span>
```
2) 위치나 방향, 크기만으로 정보 제공하지 않기
> 가리키고자 하는 요소의 명칭, 요소가 포함하고 있는 대체 텍스트 등을 지칭하여 안내함 

3) 색으로만 정보 제공
```html
<!-- 오류 -->
<p>보라색 지역은 관할 지역입니다</p>
<!-- 해결 방안 -->
<p>서울, 경기, 인천지역은 관할 지역입니다</p>
```


<br/>

#### 콘텐츠의 명도 대비
> 저시력자, 고령자 등 색약자들이 콘텐츠를 인식할 수 있도록 콘텐츠와 배경 간의 명도 대비는 **4.5대 1 이상**이어야 함

**명도 대비 평가 도구**
- [Colour Contrast Analyzer](http://www.colorsontheweb.com/Color-Tools/Color-Contrast-Analyzer)
- [Colour Contrast Check](https://snook.ca/technical/colour_contrast/colour.html#fg=33FF33,bg=333333)
- [Contrast Analyser](https://developer.paciellogroup.com/color-contrast-checker/)
- [Colour Contrast](https://juicystudio.com/services/luminositycontrastratio.php)
- *확인 참고용*: 개발도구(F12)창 명도 대비(contrast ratio)

**명도 대비 예외 사항**
1. 콘텐츠와 배경 색의 명도 대비가 3:1까지 허용되는 경우
   - 텍스트가 18pt or bold 14pt 이상의 경우
   - 확대 가능한 페이지의 일반 텍스트 또는 이미지 텍스트
2. 비활성 콘텐츠 
   - 입력 방지용, 사용 불가 표시용
3. 장식 콘텐츠

<br/>

#### 자동 재생 금지
> 배경음 등 자동으로 소리가 재생되지 않아야 하며, 사용자 입력 및 컨트롤을 조작이 가능하도록 제공되어야 함

화면 낭독 프로그램 사용자가 콘텐츠를 인식하고 사용하는 데 방해받을 수 있기에 3초 이상의 배경음은 자동 재생되지 않도록 제공되어야 함.

1) 자동 재생 배경음은 **3초 내에 멈추**거나, 소스 상에서 **가장 먼저 제공**해 정지 기능이 실행 가능하도록 하거나, 지정된 키(e.g. esc키)를 누르면 재생을 멈추도록 구현해야 함
2) 시간 제한이 있는 콘텐츠의 경우, **응답시간을 조절**하거나 **콘텐츠를 제어할 수 있는 수단**을 제공해야 하며, *시간적 제한이 있음을 사용자에게 반드시 알려*야 함.
   e.g. 인증 번호 연장 버튼 등
3) 자동으로 변경되는 배너, 텍스트 스크롤 등 슬라이드 콘텐츠는 **컨트롤 기능**을 제공하여 움직임 제어가 가능하여야 함 
   → 일시정지, 재생 버튼 제공
   → 전체 배너의 갯수 인지할 수 있도록 리스트 제공
   → 해당 컨트롤 요소에 초점 이동 기능 제공

<br/>

#### 콘텐츠 간의 구분
> 이웃한 콘텐츠는 시각적으로 구별될 수 있어야 함 

1) 테두리, 혹은 서로 다른 무늬를 이용하여 구분
2) 콘텐츠 사이 시각적인 구분선 삽입
3) 콘텐츠 배경색 간의 명도대비(채도)를 달리해 구분
4) 줄 간격, 글자 간격 조절하여 구분

<br/>

***

<br/>

### 이해의 용이성
> 콘텐츠는 이해할 수 있어야 한다

<br/>

#### 키보드 사용 보장
> 

<br/>

#### 초점 이동
> 


<br/>

#### 조작 가능
> 


<br/>

#### 정지 기능 제공
> 


<br/>

#### 깜빡임과 반짝임 사용 제한
> 


<br/>

#### 반복 영역 건너뛰기
> 

<br/>

#### 제목 제공
> 

<br/>

#### 적절한 링크 텍스트
>
> 

<br/>

***

<br/>


### 운용의 용이성
> 사용자 인터페이스 구성 요소는 조작 가능하고 내비게이션 할 수 있어야 한다

<br/>

#### 기본 언어 표시
> 


<br/>

#### 사용자 요구에 따른 실행
> 


<br/>

#### 콘텐츠의 선형 구조
> 


<br/>

#### 표의 구성
> 


<br/>

#### 레이블 제공
> 


<br/>

#### 오류 정정
> 


<br/>

***

<br/>

### 견고성
> 웹 콘텐츠는 미래의 기술로도 접근할 수 있도록 견고하게 만들어야 한다

<br/>

#### 마크업 오류 방지
> 


<br/>

#### 웹 애플리케이션 자체 접근성
> 


<br/>