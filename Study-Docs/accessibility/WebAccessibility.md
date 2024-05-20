# 웹 콘텐츠 접근성 지침(WCAG)2
## Table of Contents
1. [인식의 용이성(perceivable)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#인식의-용이성)
   1. [적절한 대체 텍스트 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#적절한-대체-텍스트-제공)
   2. [자막 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#자막-제공)
   4. [표의 구성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#표의-구성)
   3. [콘텐츠의 선형 구조](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#콘텐츠의-선형-구조)
   5. [명확한 지시 사항 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#명확한-지시-사항-제공)
   6. [색에 무관한 콘텐츠 인식](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#색에-무관한-콘텐츠-인식)
   7. [자동 재생 금지](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#배경음-사용-금지)
   8. [텍스트 콘텐츠의 명도 대비](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#텍스트-콘텐츠의-명도-대비)
   9. [콘텐츠 간의 구분](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#콘텐츠-간의-구분)
2. [운용의 용이성(operable)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#운용의-용이성)
   1. [키보드 사용 보장](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#키보드-사용-보장)
   2. [초점 이동](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#초점-이동)
   3. [조작 가능](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#조작-가능)
   4. [문자 단축키](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#문자-단축키)
   5. [응답 시간 조절](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#응답-시간-조절)
   6. [정지 기능 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#정지-기능-제공)
   7. [깜빡임과 번쩍임 사용 제한](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#깜빡임과-번쩍임-사용-제한)
   8. [반복 영역 건너뛰기](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#반복-영역-건너뛰기)
   9. [제목 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#제목-제공)
   10. [적절한 링크 텍스트](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#적절한-링크-텍스트)
   11. [고정된 참조 위치 정보](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#고정된-참조-위치-정보)
3. [이해의 용이성(understandable)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#이해의-용이성)
   1. [단일 포인터 입력 지원](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#단일-포인터-입력-지원)
   2. [포인터 입력 취소](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#포인터-입력-취소)
   3. [레이블과 네임](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#레이블과-네임)
   4. [동작기반 작동](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#동작기반-작동)
   5. [기본 언어 표시](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#기본-언어-표시)
   6. [사용자 요구에 따른 실행](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#사용자-요구에-따른-실행)
   7. [찾기 쉬운 도움 정보](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#찾기-쉬운-도움-정보)
   8. [오류 정정](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#오류-정정)
   9. [레이블 제공](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#레이블-제공)
   10. [접근 가능한 인증](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#접근-가능한-인증)
   11. [반복 입력 정보](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#반복-입력-정보)
4. [견고성(robust)](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#견고성)
   1. [마크업 오류 방지](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#마크업-오류-방지)
   2. [웹 애플리케이션 자체 접근성](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#웹-애플리케이션-자체-접근성)

<br/>

***
***
***

<br/>

### 인식의 용이성
> 웹사이트에서 제공하는 **모든 콘텐츠를 동등하게 인식**할 수 있도록 제공하는 것

<br/>

### <대체 텍스트 제공>
***

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

7) 캡차(captcha) 이미지
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

### <멀티미디어 대체 수단>
***

#### 자막제공
> 멀티미디어 콘텐츠에는 콘텐츠와 동등한 내용의 ```자막```, ```대본``` 또는 ```수어``` 제공을 해야 함 <br/>
> 주의할 점: **자동 소리 재생 기능 금지**

1) 영상, 이미지 정보를 제공할 경우 시각 정보나 음성 정보에 대해 요약하지 않고 **빠짐없이 전달**해야 함
2) 음성이 나오지 않는 멀티미디어의 경우, **원고** 등의 **대체 콘텐츠를 제공**해야 함
3) 영상의 자막을 시청하거나 음성을 듣기 어려운 경우, *시각*을 통해 내용을 이해할 수 있도록 해야 함 (**수어**를 제공할 경우 충분한 해상도 제공 필요)

<br/>

### <적응성>
***

#### 표의 구성
> 이해하기 쉽게 구성해야 함 <br/>
> [참고 사이트](https://worker-k.tistory.com/entry/table-%ED%83%9C%EA%B7%B8-%EC%9B%B9-%EC%A0%91%EA%B7%BC%EC%84%B1-caption-scope-%EC%A4%91%EC%8B%AC%EC%9C%BC%EB%A1%9C)

※ 데이터가 아닌 콘텐츠는 table로 마크업하지 않길 권장 <br/>
※ scope: 스크린 리더기에서 읽히는 순서에 관여함. thead의 th scope="col"속성부터 읽게 됨.

1) 데이터 테이블
   > 표에 적절한 *제목과 요약 정보* 제공
   * scope 속성을 가지고 있는 th 존재
   * caption 가지고 있음
   * thead 영역에는 td태그가 올 수 없음
   * tbody만 사용하거나 thead와 tbody만 있는 경우, thead tbody tfoot은 생략 가능하며 한 테이블에 여러 번 사용해도 상관 없음
2) 복잡한 테이블
   > 복잡하지 않은 간단한 표로 제공하거나 scope, id, headers를 적용함
   * th, caption, scope 사용 안함
3) 레이아웃 테이블
   > 디자인을 위한 표는 표로 인식하지 않도록 제목과 요약 내용을 제공하지 않음. <br/>
   > 만약 table로 제공한 경우, caption(제목)과 summary(표 내부에 대한 설명)를 제공하지 않아야 함
4) 중첩 테이블
   > 표의 정보를 이해하기 어려운 중첩 표를 넣어 정보를 제공하지 말 것

<br/>


#### 콘텐츠의 선형 구조
> 콘텐츠는 논리적인 순서로 제공해야 함

1) 탭 콘텐츠
   > 제목-내용-제목-내용 순서로 마크업 or 내용에 대한 제목을 숨김처리
2) 더보기 콘텐츠
   > 제목-내용-더보기 순서


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
```html
<p>'나의 정보 확인하기' 버튼을 클릭하여 정보를 확인할 수 있습니다.</p>
<button>나의 정보 확인하기</button>
```

3) 색으로만 정보 제공하지 않기
   > 색상만으로 정보 전달, 행동 지시, 반응 유발, 시각적 요소를 식별하는 용도로 사용하면 안 됨
```html
<!-- 오류 사항 -->
<p>보라색 지역은 관할 지역입니다</p>
<!-- 개선 사항 -->
<p>서울, 경기, 인천지역은 관할 지역입니다</p>
```


<br/>

### <명료성>
***

#### 색에 무관한 콘텐츠 인식
> 특정 색을 구분할 수 없거나, 흑백 디스플레이 사용자와 같이 색상만으로 콘텐츠를 구분할 수 없는 경우가 있기에 콘텐츠는 **색에 관계없이 인식**될 수 있어야 함. *두 가지 이상의 구분자*를 사용하는 것이 좋음

1) 색만으로 구분하지 않고 **색의 의미**를 텍스트로 추가 제공함
2) 그래프의 경우 **모양, 무늬, 굵기, 패턴** 등 다양한 방법으로 구분할 수 있도록 제공하며, 색을 사용할 경우 *색이 의미하고 있는 내용을 추가로 설명*함 
3) 선택 표시를 색으로 구분할 경우 **테두리, 구분선, 밑줄** 등으로 *추가 표시*함
e.g. 슬라이드 버튼, 페이지네이션, 탭 버튼 etc.

<br/>


#### 배경음 사용 금지
> 배경음 등 **자동으로 소리가 재생되지 않아**야 하며, 사용자 입력 및 컨트롤을 조작이 가능하도록 제공되어야 함

화면 낭독 프로그램 사용자가 콘텐츠를 인식하고 사용하는 데 방해받을 수 있기에 3초 이상의 배경음은 자동 재생되지 않도록 제공되어야 함. <br/><br/>

자동 재생 배경음은 **3초 내에 멈추**거나, 소스 상에서 **가장 먼저 제공**해 정지 기능이 실행 가능하도록 하거나, 지정된 키(e.g. esc키)를 누르면 재생을 멈추도록 구현해야 함

<br/>

#### 콘텐츠의 명도 대비
> 저시력자, 고령자 등 색약자들이 콘텐츠를 인식할 수 있도록 콘텐츠와 배경 간의 명도 대비는 최소 **4.5대 1 이상**이어야 함

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
4. 초점을 받았을 때 색이나 명도 대비가 변화하는 콘텐츠

<br/>


#### 콘텐츠 간의 구분
> 이웃한 콘텐츠는 *시각적으로 구별*될 수 있어야 함 

1) 테두리, 혹은 서로 다른 무늬를 이용하여 구분
2) 콘텐츠 사이 시각적인 구분선 삽입
3) 콘텐츠 배경색 간의 명도대비(채도)를 달리해 구분
4) 줄 간격, 글자 간격 조절하여 구분

<br/>

***

<br/>



### 운용의 용이성
> 웹사이트에서 제공하는 **모든 기능을 운용할 수 있도록 제공**하는 것

<br/>


### <입력장치 접근성>
***

#### 키보드 사용 보장
> 모든 기능은 *키보드만으로 사용*할 수 있어야 함

1. a링크 요소 href 속성 필수 제공
2. (PC 웹) 키보드 사용 보장
3. (모바일 웹) 누르기 동작 지원 <br/>
   > 터치(Touch)기반 모바일 기기의 모든 컨트롤¹은 누르기 동작으로 제어할 수 있어야 함(동작 대체 필수) <br/>
   > ¹ 모든 컨트롤: 슬라이드(Slide), 드래그 앤 드롭(Drag and Drop) 

e.g. <br/>
1. 드롭 다운 메뉴 
2. 마우스 오버 시 콘텐츠 노출 > 키보드 접근 시에도 동일하게 제공
3. 이미지, 초점 받을 수 없는 요소에 마우스 이벤트 적용
```html
<!-- 오류 사항 -->
<span onclick="btn_next();">다음 콘텐츠 보기</span>
<!-- 개선 사항 -->
<button>다음 콘텐츠 보기</button>
```

<br/>

#### 초점 이동
> 해당 컨트롤이 초점을 받았을 때 **시각적으로 구별**할 수 있어야 함

1. 논리적, 일관적인 초점 순서 이동 (좌에서 우, 상에서 하) <br/>
   > 초점이 논리적으로 이동하는 선에서 tabindex 사용 제한
2. 레이어 팝업 초점 이동 <br/>
   > 레이어 팝업 노출 시, 초점은 팝업 내부로 이동하여야 하며 팝업이 닫히면 다시 노출시킨 컨트롤로 초점이 이동해야 함
3. 키보드 접근 시 **초점이 표시**되도록 제공 <br/>
   > hideFocus, outline:none, onfocus="this.blur();" 사용 제한

<br/>

#### 조작 가능
> 사용자의 **입력 및 컨트롤을 조작 가능**하도록 제공되어야 함

1. 콘텐츠 **대각선 길이 6mm 이상**으로 제공
   - 모바일의 경우 터치 오류를 최소화하기 위해 [가로 * 세로 = 9mm * 9mm]이상으로 제작, 2단 구성의 컨텐츠 제작 시 [13mm * 13mm]로 제작 권고
2. 콘텐츠 테두리 안쪽으로 **1px 이상의 여백** 존재

<br/>

#### 문자 단축키
> 문자 단축키는 오동작으로 인한 **오류를 방지**하여야 함(의도치 않게 작동되는 것) <br/>
> ※ ```단일 문자 단축키```: 눌렀을 때 어떠한 기능을 작동시키도록 제공 된 단일 문자키 e.g. gmail에서 제공된 문자키(편지쓰기: c, 새 탭에서 편지쓰기: d, 메일 검색: /) <br/>
> [참고 페이지](https://mulder21c.io/understanding-kwcag-22-character-key-shortcuts/)

*해결 방안* <br/>
1. 문자 단축키를 제공하고자 하는 경우, **설정 기능**을 제공하여 사용자의 판단 하 이용할 수 있도록 제공하는 것이 좋음.  <br/>
   단, 제공 시 default는 false상태여야함. (언제든지 활성/비활성화 시킬 수 있음을 명시)
2. 보조 키를 조합한 단축키로의 재할당 가능 <br/>
   e.g. 답장하기: CTRL + R, 전체 답장하기: CTRL + SHIFT + R
3. 초점을 받은 상태에서만 단일 문자 단축키 기능 작동 <br/>
   특정 컴포넌트가 초점을 가지고 있을 때, 단축키가 작동할 수 있도록 제공되는 것 (e.g. 지도뷰에서 f키를 누르면 확대됨 etc.)

<br/>

### <충분한 시간 제공>
***

#### 응답 시간 조절
> 사용자가 콘텐츠를 읽고 사용할 수 있도록 충분한 시간을 제공해야 하며, 시간제한이 있는 콘텐츠는 **응답시간을 조절**할 수 있어야 함

시간 제한이 있는 콘텐츠의 경우, **응답시간을 조절**하거나 **콘텐츠를 제어할 수 있는 수단**을 제공해야 하며, *시간적 제한이 있음을 사용자에게 반드시 알려*야 함. <br/>
e.g. 인증 번호 연장 버튼 등

1) <**해제**> 사용자가 시간 제한을 해제할 수 있어야 함
2) <**연장**> 시간 연장이 불가능한 콘텐츠를 사용 시, 충분한 시간을 제공하거나 최소 20초 전에 **연장 수단 제공을 안내**해야 함
3) <**조정**> 페이지 자동 전환 시 시간 연장을 **위한 멈춤 버튼 및 재생 버튼 수단**을 제공해야 함


**예외 사항**
1. **실시간 예외**: 시간 제한이 필수적인 이벤트 e.g. 경매
2. **필수 예외**: [시간 제한이 필수적](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/WebAccessibility.md#깜빡임과-번쩍임-사용-제한)이며 시간 연장이 활동을 무효화 하는 경우
3. **20시간 예외**: 제한 시간이 20시간을 초과하는 경우


<br/>

#### 정지 기능 제공
> 이동, 깜빡임, 스크롤, 자동 업데이트 등 **자동으로 변경되는 콘텐츠 움직임을 제어**할 수 있어야 함

1) 자동으로 변경되는 배너, 텍스트 스크롤 등 슬라이드 콘텐츠는 **컨트롤 기능**을 제공하여 움직임 제어가 가능하여야 함  <br/>
   → 일시정지, 재생 버튼 제공 <br/>
      ※ 단, 자동 시작, 5초 이상 지속, 다른 콘텐츠와 병행하여 표시되는 콘텐츠가 활동에 필수적인 구성요소인 경우 예외 <br/>
   → 전체 배너의 갯수 인지할 수 있도록 리스트 제공 <br/>
   → 해당 컨트롤 요소에 초점 이동 기능 제공
2) 자동으로 변경되는 콘텐츠에는 이전, 다음, 정지 기능 혹은 **전체 보기 기능**을 제공해야 함 <br/>
   ※ 단, 자동 시작, 다른 콘텐츠와 병행하여 표시되는 자동 업데이트 정보가 활동에 필수적인 구성요소인 경우 예외 

<br/>


### <광과민성 발작 예방>
***

#### 깜빡임과 반짝임 사용 제한
> 광과민성 증후군 예방을 위하여 초당 3~50회 주기로 깜빡이거나 번쩍이는 콘텐츠는 포함하지 말 것

1) 깜빡이거나 번쩍이는 콘텐츠는 제공하지 않는다
2) 만약 제공할 경우 
   1) 시간을 3초 미만으로 제한
   2) 사전에 경고하고 중단 가능한 수단을 제공
   3) 해당 콘텐츠가 차지하는 면적의 합이 전체 면적의 10% 미만


<br/>


### <쉬운 내비게이션>
***

#### 반복 영역 건너뛰기
> 반복되는 영역은 건너뛸 수 있어야 함

페이지마다 반복되는 영역(e.g. header, navigation)이 있는 경우 아래 해결 방안을 모두 충족하면 조건 준수
1. 마크업 최상단 위치
2. 건너뛰기 링크가 페이지 내 존재
3. 키보드 접근 시 화면 노출
4. '하단 메뉴로 바로 가기' 같은 위치 정보 금지

```html
<body>
   <a href="#container">본문 바로가기</a>
   <header></header>
   <main id="container"></main>
   ...
</body>
```

<br/>

#### 제목 제공
> 페이지, 프레임, 콘텐츠 블록에는 내용을 유추할 수 있는 적절한 제목이 제공되어야 함

1) 페이지 타이틀
   > 반드시 유일하며, 각각 다르게 제공되어야 함
```html
<!-- 오류 사항 -->
<title>google</title>
<!-- 개선 사항 -->
<title>w3c WCAG 2.2 - Google 검색</title>
```
2) 프레임 제목
```html
<!-- 오류 사항 -->
<iframe>…<iframe>
<!-- 개선 사항 -->
<iframe title="광고">…<iframe>
<iframe title="내용 없음">…<iframe>
```
3) 콘텐츠 제목
```html
<!-- 오류 사항 -->
<div><span>쇼핑</span>...<div>
<!-- 개선 사항 -->
<div><h3>쇼핑</h3>...<div>
```


<br/>

#### 적절한 링크 텍스트
> 적절한 용도나 목적을 이해할 수 있도록 제공해야 함

1) 빈 링크는 **제거 혹은 키보드가 접근할 수 없도록** 하거나, 링크의 용도나 목적을 이해할 수 있도록 제공
2) 독립적 이미지 링크에는 이미지에 대체 텍스트 제공
3) 독립적 배경 이미지 링크에는 IR기법으로 대체 텍스트 제공
4) 썸내일 이미지는 이미지에 해당하는 텍스트를 a태그로 묶어 중복 제공되지 않도록 제공(묶을 수 없는 경우, 중복되더라도 이미지에 대한 대체 텍스트를 제공해야 함)
5) **명확한 링크**
```html
<!-- 오류 사항 -->
더 자세한 내용을 확인하려면 <a href="#">여기</a>를 클릭하세요
<!-- 개선 사항 -->
<a href="#">다음 콘텐츠 보기</a>
```
6) 한국어 설정 시 영어로 제공된 정보는 의도되지 않은 발음으로 읽힐 수 있기에 한국어로 레이블을 명확하게 설정해 제공
```html
<a herf="#" title="테스트 이미지 바로가기 새 창 열림">
   <img src="testImg.png" alt="테스트 이미지" >
</a>
```

<br/>

#### 고정된 참조 위치 정보
> 전자출판문서 형식의 웹 페이지는 각 페이지로 이동할 수 있는 기능이 있어야 하고, 서식이나 플랫폼에 상관없이 **참조 위치 정보를 일관되게 제공ㆍ유지**해야 함

페이지 구분이 있는 전자출판문서 형식의 웹 페이지는 일관된 위치에 **참조 위치 정보**(e.g. 페이지 번호와 같은 페이지 구분자)를 제공해야 하고, 각 페이지로 이동할 수 있는 기능을 제공/유지해야 함. 이는 콘텐츠의 확대/축소 등으로 서식이 변경되거나 플랫폼이 변경되어 정보가 사라지거나, 일관된 위치에 제공되지 않을 경우 *위치 정보를 제공할 수 있도록 존재*하는 것임.

<br/>


### <쉬운 내비게이션>
***

#### 단일 포인터 입력 지원
> 다중 포인터 또는 경로기반 동작을 통한 입력은 **단일 포인터 입력으로도 조작**할 수 있어야 함
> ※ ```다중 포인터```: 두 개 이상의 손가락을 동시에 사용 e.g. 핀치 줌, 두 손가락 탭 등
> ※ ```경로 기반 동작```: 쓸어 넘기기 동작 e.g. 스와이프, 끌기와 놓기, 그리기 등

*예외사항*
1. 필수적인 경우: 피아노 앱의 건반 누르기, 서명 등 입력이 반드시 실행되어야 하는 경우
2. 운영체제나 사용자 에이전트(e.g. 브라우저), 보조기기 등이 지원하는 동작(e.g. 운영체제가 제공하는 손가락 두 개 끌어 스크롤하기)을 통한 입력 


<br/>

#### 포인터 입력 취소
> **단일 포인터 입력으로 실행되는 기능은 취소**할 수 있어야함(실수로 실행되는 것을 방지하기 위함)

아래 중 하나 이상을 준수해야 함
1. 다운 이벤트로만 실행 금지
2. 중지 또는 실행취소: 기능은 업 이벤트에 완료되어야 하며, 실행 전 중지시키거나 실행 후 취소시킬 수 있어야 함
3. 되돌리기: 다운 이벤트로 실행된 모든 기능은 업 이벤트로 되돌릴 수 있어야 함
4. 필수적인 경우: 기능을 완료하는 데 다운 이벤트가 반드시 필요한 경우(e.g. 화면 피아노 건반, 슈팅게임 등)

<br/>

#### 레이블과 네임
> 텍스트 또는 텍스트 이미지가 포함된 레이블이 있는 사용자 인터페이스 구성요소는 **네임에 시각적으로 표시되는 해당 텍스트를 포함**해함

사용자 인터페이스 구성요소(e.g. 메뉴, 버튼, 링크 등)에서 시각적으로 표시되는 텍스트를 네임에 제공하지 않은 경우 보조기술이 해당 사용자 인터페이스 구성요소를 인식할 수 없기 때문에 **네임에는 시각적으로 표시되는 텍스트를 제공**해야 함. 네임과 텍스트를 다르게 제공한 경우, 해당 정보 사용자(e.g. 음성명령 사용자)가 혼란을 겪을 수 있기 때문에 **네임-텍스트는 동일하게 제공**하는 것이 좋으며, 그러지 않을 경우 텍스트는 네임의 앞 부분에 제시하는 것이 좋음
- 음성 입력 사용자가 시각적으로 표시되는 텍스트를 사용해 사용자 인터페이스 구성요소를 제어할 수 있음
- 텍스트 음성 변환(TTS)사용자는 보조기술을 통해 음성으로 전달되는 텍스트와 시각적으로 표시되는 텍스트가 일치하기에 사용자 인터페이스 구성요소를 혼란 없이 보다 쉽게 인지/활용이 가능함

<br/>

#### 동작기반 작동 
> 동작기반으로 작동하는 기능은 **사용자 인터페이스 구성요소로 조작**할 수 있고, 동작기반 기능을 비활성화할 수 있어야 함. <br/>
> ※ ```동작기반 작동 기능```: 흔들어서 실행 취소, 손동작을 이용한 사진 촬영 등

단, 아래와 같은 사항은 예외로 간주함
1. 접근성 지원 인터페이스 e.g. 안구마우스
2. 동작이 기능의 실행에 반드시 필요하며, 실행에 대한 비활성화가 기능 자체를 무효화할 수 있는 경우 e.g. 만보기

<br/>

***

<br/>


### 이해의 용이성
> 웹사이트에서 제공하는 서비스의 콘텐츠, 기능 사용법 등을 **사용자가 이해하기 쉽게 제공**하는 것

<br/>


### <가독성>
***

#### 기본 언어 표시
> 주로 사용하는 언어를 명시해야 함

1. lang 속성으로 적절한 언어 제공
2. 언어 표준 명시
```html
<!-- HTML4.01 / HTML5 -->
<!DOCTYPE HTML >
<html lang="ko">
<!-- 
   한국어: ko / 영어: en / 중국어: zn / 일본어: ja
   프랑스어: Fr / 독일어: De / 이탈리아어: it / 스페인어: es
-->

<!-- XHTML1.0 -->
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="ko" lang="ko">

<!-- XHTML1.1 -->
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="ko">
```

<br/>

### <예측 가능성>
***

#### 사용자 요구에 따른 실행
> 사용자가 **의도하지 않은 기능(새 창, 초점 변화 등)은 실행되지 않아야 함**

1. 페이지 진입 시 새 창이 뜨지 않도록 제공 e.g. 팝업
2. 화면을 가리는 레이어 팝업이 뜨지 않도록 제공 <br/>
   → 화면을 가리는 경우 최상단에 마크업, 혹은 화면을 가리지 않도록 상단에 제공
3. 사전에 인식할 수 없는 새 창이 열리지 않도록 제공
```html
<a href="...">개인정보처리방침<span class="blind">새창</span></a>
<a href="..." title="개인정보처리방침 새창 열림">개인정보처리방침</a>
<a href="..." target="_blank">개인정보처리방침</a>
```
4. 컨트롤 선택 시 기능 실행하도록 제공
5. select에는 키보드 접근이 불가능하므로 따로 버튼을 제공해 onchange 이벤트 적용 실행

<br/>

#### 찾기 쉬운 도움 정보
> 도움 정보가 제공되는 경우, **각 페이지에서 동일한 상대적인 순서로 접근**할 수 있어야 함 e.g. 화면 옆 고정되어 보여지는 도움말 메뉴 <br/>
> 단일 페이지 웹 애플리케이션/웹 페이지 세트에서 하나 이상의 도움 정보가 제공될 때, 최소한 하나의 도움 정보는 해당 페이지에서 동일한 상대적 순서대로 제공되어야 함

*최소 1개 이상, 페이지에 표시해야 될 정보*
1. ```담당자 상세 연락처``` e.g. 전화번호, 이메일, 운영시간 등
2. ```담당자 연락 방법``` e.g. 메신저, 채팅장, 게시판, SNS 등
3. ```도움말 옵션``` e.g. FAQ, 사용법 등
4. ```자동화된 연결방법``` e.g. 챗봇 등

<br/>

### <입력 도움>
***

#### 오류 정정
> 입력 오류를 정정할 수 있는 방법 제공

1. 입력 오류 시 입력 내용이 모두 사라지는 경우
   > 입력 완료 후나 제출 시 *오류가 발생하면 내용이 사라지지 않고 유지*되도록 제공
2. 오류 내용 및 정정 수단 제공
   > 오류의 원인을 알 수 있도록 *적절한 설명 텍스트*를 제공
   ```html
   <label for="user_ymd">생년월일<span class="info_txt">형식: yyyy-mm-dd</span></label>
   <input type="text" id="user_ymd" />
   ```
3. 오류 *발생 시점으로 초점 이동*
   > 오류가 발생한 서식으로 초점 이동

<br/>

#### 레이블 제공
> 입력에 대응하는 레이블을 제공해야 함

```input``` ```textarea``` ```select```요소에 1:1로 대응하는 ```label```요소 또는 ```title```속성을 제공해야 함

1. 시각적으로 노출된 경우, 입력 서식과 레이블을 1:1로 매칭함
```html
<label for="user_id">아이디</label>
<input type="text" id="user_id" />
```
2. 시각적으로 노출되지 않은 경우, 입력 서식에 title 제공
```html
<!-- title 제공 -->
<input type="text" id="user_id" title="아이디" />
```

<br/>

#### 접근 가능한 인증
> 인증 과정은 인지 기능 테스트에만 의존해서는 안됨

사용자 로그인 등과 같은 인증 과정이 ```인지 기능 테스트```에 의존하는 경우, 그에 ```의존하지 않는 인증 방법```을 적어도 하나 이상 제공해야 함 <br/>
※ ```인지 기능 테스트```: 로그인을 위한 비밀번호 입력, 터치스크린 화면의 패턴 인식, 임의의 문자열 기억, 특정 개체를 포함하고 있는 이미지 찾기 등 <br/>
※ ```의존하지 않는 인증 방법```
   1. 브라우저가 아이디/비밀번호를 저장할 수 있도록 마크업된 서식
   2. 공개인증(OAuth: Open Authorization)을 통한 서드 파티
   3. 신체(얼굴, 지문 등)나 물건(휴대폰, USB 등)을 이용한 인증

<br/>

#### 반복 입력 정보
> 반복되는 입력 정보는 **자동 입력 또는 선택 입력**할 수 있어야 함

이는 개인화 설정을 통해 맞춤 설정 가능하며, 활성화 시 기억/인지 기능에 어려움을 겪는 사용자의 특정 정보에 대한 스트레스 및 실수 발생 가능성을 줄일 수 있으며 움직임에 제약이 있는 사용자의 텍스트 입력 부담을 줄일 수 있음. <br/>
e.g. 이전 단계에서 입력한 주문자 주소를 재입력 없이 선택해 채울 수 있음

<br/>

***

<br/>


### 견고성
> 사용자가 웹 콘텐츠는 모든 기기 및 브라우저에서 접근/사용이 가능해야 하며, **기술에 영향을 받지 않아**야 함

<br/>

### <문법 준수>
***

#### 마크업 오류 방지
> 열고 닫음, 중첩 관계 및 속성 선언에 오류가 없어야 함

1) 요소의 열고 닫음이 매칭되도록 제공
   ```html
   <!-- 오류 사항 -->
   <p><img src="testimg.png">
   <p>이 문법은 잘못된 <i>사용</p></i>

   <!-- 개선 사항 -->
   <p><img src="testimg.png" alt="테스트이미지" ></p>
   <p>이 문법은 <i>올바른 사용</i></p>
   ```
2) 요소가 중첩되지 않도록 제공
   ```html
   <!-- 오류 사항 -->
   <p style="color: #000" class="notice" style="width: 50em">

   <!-- 개선 사항 -->
   <p class="notice" style="color:#000; width:50em">
   ```
3) 속성이 중복되지 않도록 제공
   ```html
   <!-- 오류 사항 -->
   <div id="content" > ... </div>
   <textarea id="content" name="content"></textarea>
   
   <!-- 개선 사항 -->
   <div id="content-area" > ... </div>
   <textarea id="content" name="content"></textarea>
   ```
4) id 속성 값 중복되지 않도록 제공

<br/>

### <웹 애플리케이션 접근성>
***

#### 웹 애플리케이션 자체 접근성
> 콘텐츠에 포함된 웹 애플리케이션은 접근성이 있어 사용자가 웹 페이지에 접근하여 사용하는 것을 방해하지 않아야 함

e.g 사이트 전체가 플래시로 구현된 경우
   > 대체할 수 있는 접근 가능 콘텐츠로 제공(플래시 종료로 해당 사항 없음)

<br/>
<br/>



<br/>

> **참고 사이트** <br/>
> [웹접근성 가이드](https://blog.naver.com/ideavillage/222294734324) | [NULI](https://nuli.navercorp.com/guideline/s01/g01) | [Naver 접근성](https://accessibility.naver.com/accessibility) | [웹접근성 4대원칙](https://365kim.tistory.com/71) | [웹 접근성 실무가이드](http://www.websoul.co.kr/consulting/guide1_01.asp) | [WCAG2.1](http://www.kwacc.or.kr/WAI/wcag21/#perceivable) | [한국형웹콘텐츠접근성지침2.2](http://www.websoul.co.kr/accessibility/PDF/%ED%95%9C%EA%B5%AD%ED%98%95%EC%9B%B9%EC%BD%98%ED%85%90%EC%B8%A0%EC%A0%91%EA%B7%BC%EC%84%B1%EC%A7%80%EC%B9%A82.2.pdf)| [WCAG3](https://www.w3.org/TR/wcag-3.0/) | [웹 콘텐츠 접근성 지침 추가 내역 확인](https://velog.io/@planic324/2022%EB%85%84-%ED%95%9C%EA%B5%AD%ED%98%95-%EC%9B%B9-%EC%BD%98%ED%85%90%EC%B8%A0-%EC%A0%91%EA%B7%BC%EC%84%B1-%EC%A7%80%EC%B9%A8-feat.-%EC%B6%94%EA%B0%80%EB%90%9C-%EB%82%B4%EC%97%AD-%ED%99%95%EC%9D%B8%ED%95%98%EA%B8%B0)
