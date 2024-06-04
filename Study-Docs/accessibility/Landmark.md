# 랜드마크(Landmark)
> 웹 페이지의 구조를 설명하고 웹 접근성을 향상시키는 데 사용되는 특별한 역할을 하는 요소 <br/>
> 웹 페이지를 이해하고 탐색하는 데 도움을 주며, 스크린 리더 및 다른 보조 기술을 사용하는 사용자에게 페이지의 레이아웃 및 구조를 전달하는 데 중요한 역할

HTML Element | Default Landmark Role
-- | --
```aside``` | ```complementary```
```form``` | ```form```은 다음 속성이 있으면 같이 사용하는 것이 좋음 ```aria-labelledby```, ```aria-label```, ```title```
```header``` | body 요소와 인접한 경우 ```banner``` <br/>다음 html 섹션 요소 하위로 위치할 경우 해당하지 않음 (articel, aside, main, nav, section)
```main``` | ```main```
```nav``` | ```navigation```
```section``` | ```region```은 다음 속성이 있으면 같이 사용하는 것이 좋음 ```aria-labelledby```, ```aria-label```, ```title```
```footer``` | body 요소와 인접한 경우 ```contentinfo``` <br/> 다음 html 섹션 요소 하위로 위치할 경우 해당하지 않음 (articel, aside, main, nav, section)

## banner
> 각 페이지의 시작 부분에서 사이트의 중심 콘텐츠(로고, 검색도구 등)를 식별함 <br/>
> 일반적으로 페이지 상단에서 전체 너비에 걸쳐 표시됨

* 각 페이지에는 하나의 ```banner```랜드마크가 존재
* ```banner```는 최상위 랜드마크여야 함
* 페이지에 중첩된 문서나 애플리케이션 역할이 포함된 경우, 각 역할에는 하나의 ```banner```랜드마크가 있을 수 있음 (e.g. ```iframe```, ```frame``` 요소 사용할 경우)
* 페이지에 둘 이상의 ```banner``` 랜드마크가 포함된 경우, 각 랜드마크에는 고유한 레이블이 있어야 함

```html
<header>
  <h1>website information<h1>
  .... banner content....
</header>

<div role="banner">
  <h1>page title identifying website<h1>
  .... banner content....
</div>
```


## Complementary 
> 문서의 지원 및 기본 콘텐츠와 분리되어도 의미가 유지됨

* 다른 랜드마크에는 포함되지 않으며, 최상위 레벨이어야 함
* 주요 내용과 관련이 없는 경우 좀 더 일반적인 역할을 할당해야 함
* 두 개 이상의 ```Complementary``` 랜드마크가 포함된 경우, 각 랜드마크에는 고유한 라벨이 있어야 함

```html
<aside>
  <h2>Title for complementary area<h2>
  .... complementary content area ....
</aside>
<!-- or -->
<div role="complementary">
  <h2>Title for complementary area<h2>
  .... complementary content area ....
</div>

<!-- ===== -->

<aside aria-labelledby="comp1">
  <h2 id="comp1">Title for complementary area 1</h2>
  ... complementary content area 1 ...
</aside>
<aside aria-labelledby="comp2">
  <h2 id="comp2">Title for complementary area 2</h2>
  ... complementary content area 2 ...
</aside>
<!-- or -->
<div role="complementary" aria-labelledby="comp1">
  <h2 id="comp1">Title for complementary area 1</h2>
  ... complementary content area 1 ...
</div>
<div role="complementary" aria-labelledby="comp2">
  <h2 id="comp2">Title for complementary area 2</h2>
  ... complementary content area 2 ...
</div>
```

## Contentinfo
> 페이지의 하단에서 저작권, 개인정보 보호 및 접근성 설명에 대한 링크와 같은 정보를 포함하는 공통 정보를 식별함

* 각 페이지에 하나의 ```Contentinfo``` 랜드마크를 가짐
* ```Contentinfo```는 최상위 랜드마크여야 함
* 페이지에 중첩된 문서나 애플리케이션 역할이 포함된 경우, 각 역할에는 하나의 ```Contentinfo```랜드마크가 있을 수 있음 (e.g. ```iframe```, ```frame``` 요소 사용할 경우)
* 두 개 이상의 ```Contentinfo``` 랜드마크가 포함된 경우, 각 랜드마크에는 고유한 라벨이 있어야 함

```html
<footer>
  <h2>Contact, Policies and Legal<h2>
  .... contentinfo area content ....
</footer>

<div role="contentinfo">
  <h2>Contact, Policies and Legal<h2>
  .... contentinfo area content ....
</div>
```
