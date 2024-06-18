## inputmode
> 입력 가능한 컨트롤 요소(```input type="text"```)나 ```contenteditable="true"```속성을 사용해 편집 가능한 요소의 **가상 키보드 입력 모드**를 설정함

token | note
-- | --
```none``` | 가상 키보드를 표시하지 않음
```text``` | ```[default]``` 사용자의 locale에 대한 텍스트를 입력할 수 있는 가상 키보드를 표시함
```tel``` | 전화번호 입력이 가능한 가상 키보드를 표시함. 숫자 ```0~9```, ```#```, ```*``` 문자에 대한 키가 포함됨 <br/> 일반적으로는 해당 속성보다 ```<input type="tel">``` 사용
```url``` | url 입력을 보조하기 위한 키, ```/```, ```.``` 문자와 ```www.``` ```.com```과 같은 빠른 입력 키 제공 <br/> 일반적으로는 해당 속성보다 ```<input type="url">``` 사용
```email``` | 전자 메일 주소 입력데 도움되는 키, ```@```, ```.``` 문자 제공 <br/> 일반적으로는 해당 속성보다 ```<input type="mail">``` 사용
```numeric``` | 숫자 입력이 가능한 가상 키보드 표시, PIN 입력에 유용
```decimal``` | 분수 숫자 입력이 가능한 가상 키보드 표시, 숫자 키와 locale의 형식 구분자 표시해야 함
```search``` | 검색에 최적화된 가상 키보드 표시 <br/> 일반적으로는 해당 속성보다 ```<input type="search">``` 사용

## enterkeyhint 
> 가상 키보드의 ```enter```키에 대해 표시할 텍스트, 아이콘 모양 등의 레이블을 명시적으로 설명하여 ```enter```키에 대한 힌트(hint)를 제공

token | note
-- | --
```enter``` | 새 줄을 삽입하는 'enter(입력)' 작업에 대한 단서를 제시
```done``` | '완료' 작업에 대한 단서를 제시, 일반적으로 더 이상 입력할 내용이 없고 IME(Input Method Editor)가 닫힘
```go``` | 사용자를 입력한 텍스트의 대상으로 데려가는 것을 의미하는 '이동' 작업에 대한 단서를 제시
```next``` | '다음' 작업에 대한 단서를 제공해야 하며 일반적으로 사용자를 텍스트를 허용하는 다음 필드로 안내
```previous``` | '이전' 작업에 대한 단서를 제시해야 하며 일반적으로 사용자를 텍스트를 허용하는 이전 필드로 안내
```search``` | 사용자가 입력한 텍스트 검색 결과로 사용자를 안내하는 '검색' 작업에 대한 단서를 제공
```send``` | 사용자에게 텍스트를 전달하는 '보내기' 작업에 대한 신호를 제공

## autocomplete  
> 자동완성을 허용할 양식 입력 필드 지정 및 기능 안내 가능

```input``` ```textarea``` ```select``` ```form```요소에서 사용 가능 <br/>
해당 요소들은 아래 조건을 만족해야 사용자 에이전트가 자동완성을 제공함
1. ```name``` 또는 ```id``` 특성 존재
2. ```<form>```요소의 자손
3. 양식에 ```제출```버튼이 있을 것

token | note
-- | --
```off``` | 브라우저가 이 필드에 값을 자동으로 넣는 것을 금지 <br/> ※ 단, 브라우저가 저장한 값을 사용해 자동완성을 하거나, 사용자에게 계정 이름, 비밀번호 저장 여부를 묻는 것은 막을 수 없음.
```on``` | 브라우저의 자동완성을 허용
```name``` | 사람의 전체 이름, 개별 이름 구성 요소보다 해당 태그를 많이 사용하지만 하나씩 받아야 하는 경우라면 아래 값들도 사용 가능 <br/>
```honorific-prefix```- **호칭** ```Mrs``` ```Mr``` ```Miss``` ```Ms``` ```Dr.``` ```Mlle.``` 등 <br/>
```family-name```- 성 <br/>
```given-name```- 이름 <br/>
```additional-name```- 미들네임 <br/>
```honorific-suffix```- 접미사, ```Jr.``` ```B.Sc.``` ```PhD.``` ```MBASW``` ```IV``` 등 <br/>
```nickname```- 별명, 별칭 <br/>
```email``` | 이메일 주소 
```username``` | 사용자 또는 계정 이름 
```new-password``` | 새로운 비밀번호 
```current-password``` | 사용자의 현재 비밀번호
```one-time-code``` | 사용자를 인증할 때 사용하는 1회성 코드
```organization-title``` | 직위, ```사장``` ```매니저``` 등 
```organization``` | 회사 또는 조직명 
```street-address``` | 도로 주소  <br/>
여러 줄 가능 <br/>
두 번째 행정구역(시/군/구) 내에서 구분할 수 있는 주소 <br/>
도시 이름, 우편번호, 국가 이름은 포함 불가 <br/>
```address-line1, address-line2, address-line3``` | 도로 주소의 각 줄, street-address가 존재하지 않는 경우에만 사용
```address-level4``` | 4단계 주소에서 가장 상세한 행정구역
```address-level3``` | 최소 3단계 주소에서의 3단계 행정구역
```address-level2``` | 최소 2단계 주소에서의 2단계 행정구역(도시, 마을)
```address-level1``` | 최소 2단계 주소에서의 2단계 행정구역(특별시, 광역시/도, 주)
```country``` | 국가 코드
```country-name``` | 국가 이름
```postal-code``` | 우편번호
```cc-name``` | 신용카드 등 지불수단 소유자의 전체 이름
```cc-family-name``` | 지불수단 소유자의 성
```cc-given-name``` | 지불수단 소유자의 이름
```cc-additional-name``` | 지불수단 소유자의 가운데 이름
```cc-number``` | 신용카드 번호, 계좌번호 등 지불수단 식별 번호.
```cc-exp``` | 지불수단 유효기간. 보통 MM/YY 또는 MM/YYYY의 형태
```cc-exp-month``` | 지불수단 유효기간의 월
```cc-exp-year``` | 지불수단 유효기간의 연도
```cc-csc``` | 지불수단 보안 코드
```cc-type``` | 지불수단 유형 (visa, master card etc.)
```transaction-currency``` | 거래에 사용할 통화 단위
```transaction-amount``` | 결제 양식에 나타나는 거래량, 금액
```language``` | 선호 언어 ([유효한 BCP 47 언어 태그](https://ko.wikipedia.org/wiki/IETF_%EC%96%B8%EC%96%B4_%ED%83%9C%EA%B7%B8) 내)
```bday``` | 생년월일
```bday-day``` | 생일
```bday-month``` | 생월
```bday-year``` | 생년
```sex``` | 성별 (줄바꿈 없는 자유형식 텍스트)
```tel``` | 국가 코드를 포함한 전체 전화번호, 개별 전화번호 구성요소가 필요한 경우, 아래 값 사용 가능 <br/>
```tel-country-code```: 국가 코드(1-북미, 82-대한민국 등) <br/>
```tel-national``` | 국가 코드를 제외한 전체 전화번호. 지역번호도 포함 e.g. 82-2-555-6502 > *02-555-6502* <br/>
```tel-area-code``` | 지역번호 <br/>
```tel-local``` | 국가 코드와 지역번호를 제외한 전화번호 e.g. 555-6502 > ```tel-local-prefix```: 555, ```tel-local-suffix```: 6502 <br/>
```tel-extension``` | 내선번호
```impp``` | 인스턴트 메시지 프로토콜 엔드포인트의 URL
```url``` | URL (홈페이지, 회사 웹사이트 주소 등)
```photo``` | 이미지 URL
