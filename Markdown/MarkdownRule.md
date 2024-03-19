# 제목(header)
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6

```plaintext
# 제목(header)
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6
```

<br/>

## 문장(Paragraph) & 줄바꿈(Line Breaks)
그냥 쓰면 문장 써지는 것 p 태그와 동일
두 번 띄어쓰기 후 줄바꿈을 하면 줄바꿈 처리로 인식 되지만<br/>
사용 안 되는 때가 있기에 이럴 땐 br코드를 사용하여 줄바꿈 처리가 가능하다.
```plaintext
그냥 쓰면 문장 써지는 것 p 태그와 동일  두 번 띄어쓰기를 하면 줄바꿈 처리가 되지만<br/>
사용 안 되는 때가 있기에 이럴 땐 br코드를 사용하여 줄바꿈 처리가 가능하다.
```

<br/>


## 강조(Emphasis)
기본
_이텔릭_
**두껍게**
**_이텔릭 + 두껍게_**
~~취소선~~
<u>밑줄 표시되는 기능 별도 제공하지 않기에 u 태그를 사용</u>

```plaintext
기본
_이텔릭_
**두껍게**
**_이텔릭 + 두껍게_**
~~취소선~~
<u>밑줄 표시되는 기능 별도 제공하지 않기에 u 태그를 사용</u>
```

<br/>


## 목록(List)
#### ol태그 개념
1. 순서가 필요한 목록
1. 순서가 필요한 목록
1. 순서가 필요한 목록
    1. 순서가 필요한 목록(들여쓰기 두 번 필요)
    1. 순서가 필요한 목록
1. 순서가 필요한 목록

#### ul태그 개념
- 순서가 필요하지 않는 목록
- 순서가 필요하지 않는 목록
    - 순서가 필요하지 않는 목록(들여쓰기 두 번 필요)
    - 순서가 필요하지 않는 목록
- 순서가 필요하지 않는 목록

```plaintext
#### ol태그 개념
1. 순서가 필요한 목록
1. 순서가 필요한 목록
1. 순서가 필요한 목록
    1. 순서가 필요한 목록(들여쓰기 두 번 필요)
    1. 순서가 필요한 목록
1. 순서가 필요한 목록

#### ul태그 개념
- 순서가 필요하지 않는 목록
- 순서가 필요하지 않는 목록
    - 순서가 필요하지 않는 목록(들여쓰기 두 번 필요)
    - 순서가 필요하지 않는 목록
- 순서가 필요하지 않는 목록
```

<br/>


## 링크(Links)
**_마크다운에서는 target="_balnk" 속성 제공x_**
#### 기존 태그
<a href="https://google.com">Google</a>
#### 마크다운 태그
[Google](https://google.com)
#### 기존 태그
<a href="https://naver.com" title="naver로 이동">Naver</a>
#### 마크다운 태그
[Naver](https://naver.com "naver로 이동")


```plaintext
#### 기존 태그
<a href="https://google.com">Google</a>
#### 마크다운 태그
[Google](https://google.com)
#### 기존 태그
<a href="https://naver.com" title="naver로 이동">Naver</a>
#### 마크다운 태그
[Naver](https://naver.com "naver로 이동")
```

<br/>

## 이미지(Images)
_이미지 출력_ <br/>
![대체 텍스트](https://avatars.githubusercontent.com/u/67949100?v=4) <br/>
__이미지 연결 링크 출력__ <br/>
[![대체 텍스트](https://avatars.githubusercontent.com/u/67949100?v=4)](https://github.com/hiro961227/Dev-Docs)

```plaintext
_이미지 출력_
![대체 텍스트](https://avatars.githubusercontent.com/u/67949100?v=4)
__이미지 연결 링크 출력__
[![대체 텍스트](https://avatars.githubusercontent.com/u/67949100?v=4)](https://github.com/hiro961227/Dev-Docs)
```

<br/>


## 인용문(BlockQuote)
> 남의 말이나 글에서 직접 또는 간접으로 따온 문장.
> (네이버 국어 사전)

> 인용문 중첩 가능
>> 중첩된 인용문
>>> 중중첩된 인용문
>>> 중중첩된 인용문

```plaintext
> 남의 말이나 글에서 직접 또는 간접으로 따온 문장.
> (네이버 국어 사전)

> 인용문 중첩 가능
>> 중첩된 인용문
>>> 중중첩된 인용문
>>> 중중첩된 인용문
```

<br/>


## 인라인(inline) 코드 강조
css에서 `background` 혹은 `background-image` 속성으로 요소에 배경 이미지를 삽입할 수 있습니다.
(``을 사용하여 코드라는 것을 강조함)

```plaintext
css에서 `background` 혹은 `background-image` 속성으로 요소에 배경 이미지를 삽입할 수 있습니다.
(``을 사용하여 코드라는 것을 강조함)
```

<br/>


## 블록(block) 코드 강조
언어 명시하여 코드 강조 사용이 가능하다.
```html
<a href="https://google.com" target="_blank">Google</a>
```
```css
.list > li{
  position: absolute;
  top: 40px;
}
```
```javascript
function func(){
  var a = 'aaa' ;
  return a;
}
```
```bash
$ git commit -m 'Study Markdown'
```
```paintext
개발 언어 외의 텍스트 블록 코드 강조 출력기 가능
```

```plaintext
```html ``` html 코드 하이라이트
```css ``` css 코드 하이라이트
```javascript ``` javascript 코드 하이라이트
```bash ``` 터미널 코드 하이라이트
```paintext ``` 개발 언어 외의 텍스트 강조
```

<br/>


## 표(Table)
1. 마크다운 문법에서 하이픈 기호 두 번씩 (-- | -- | --) 넣은 것은 표의 머리와 몸통 부분 구분 용도
    * -- 왼쪽 정렬(디폴트) :--: 중앙 정렬 --: 오른쪽 정렬
1. 버티컬바( | )로 구분하여 행 구분

< position 속성 표 >
값 | 의미 | 기본값
-- | :--: | --:
static | 기준 없음 | O
relative | 요소 자신 | X
absolute | 위치 상 부모 요소 | X
fixed | 뷰포트 | X

```plaintext
값 | 의미 | 기본값
-- | :--: | --:
static | 기준 없음 | O
relative | 요소 자신 | X
absolute | 위치 상 부모 요소 | X
fixed | 뷰포트 | X
```

<br/>


## 원시 HTML(Raw HTML)
> 마크다운 문법 안에서 실제 HTML 문법을 사용하는 것.

마크다운이란 것은 브라우저에서 출력되어야 하기 때문에 <u>표준 html</u>로 변환된다.<span style="text-decoration: underline;">(변환되기 전에도 html문법을 그대로 사용할 수 있음.)</span><br/>
그것이 변환될 때 환경에 따라 조금씩 다르게 변환될 수 있는데, 이는 마크다운의 표준 개념이 없기 때문.

---

* 사용되는 예시<br/>
<a href="https://google.com" target="_blank">Google</a> <br/>
<img width="70" src="https://avatars.githubusercontent.com/u/67949100?v=4" alt="대체 텍스트">

```plaintext
마크다운이란 것은 브라우저에서 출력되어야 하기 때문에 <u>표준 html</u>로 변환된다.<span style="text-decoration: underline;">(변환되기 전에도 html문법을 그대로 사용할 수 있음.)</span><br/>
그것이 변환될 때 환경에 따라 조금씩 다르게 변환될 수 있는데, 이는 마크다운의 표준 개념이 없기 때문.

* 사용되는 예시<br/>
<a href="https://google.com" target="_blank">Google</a><br/>
<img width="70" src="https://avatars.githubusercontent.com/u/67949100?v=4" alt="대체 텍스트">
```

<br/>


## 수평선(Horizontal Rule)
<br/>

---
***
___

<br/>

```plaintext
---
***
___
```
