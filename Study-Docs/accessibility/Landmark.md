# 랜드마크(Landmark)
> 웹 페이지의 구조를 설명하고 웹 접근성을 향상시키는 데 사용되는 특별한 역할을 하는 ```Role``` 요소 <br/>
> 웹 페이지를 이해하고 탐색하는 데 도움을 주며, 스크린 리더 및 다른 보조 기술을 사용하는 사용자에게 페이지의 레이아웃 및 구조를 전달하는 데 중요한 역할

HTML Element | Default Landmark Role
-- | --
[```header```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#banner) | body 요소와 인접한 경우 ```banner``` <br/>다음 html 섹션 요소 하위로 위치할 경우 해당하지 않음 (articel, aside, main, nav, section)
[```nav```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#navigation) | ```navigation```
[```search```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#search) | ```search```
[```main```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#main) | ```main```
[```section```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#region) | ```region```은 다음 속성이 있으면 같이 사용하는 것이 좋음 ```aria-labelledby```, ```aria-label```, ```title```
[```aside```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#complementary) | ```complementary```
[```form```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#from) | ```form```은 다음 속성이 있으면 같이 사용하는 것이 좋음 ```aria-labelledby```, ```aria-label```, ```title```
[```footer```](https://github.com/hiro961227/Dev-Docs/blob/main/Study-Docs/accessibility/Landmark.md#contentinfo) | body 요소와 인접한 경우 ```contentinfo``` <br/> 다음 html 섹션 요소 하위로 위치할 경우 해당하지 않음 (articel, aside, main, nav, section)


## banner
> 각 페이지의 시작 부분에서 사이트의 헤더(머리말)를 식별함. 주로 로고, 내비게이션 및 검색 입력이 포함됨 <br/>
> 일반적으로 페이지 상단에서 전체 너비에 걸쳐 표시됨

* 각 페이지에는 하나의 ```banner```랜드마크가 존재
* ```banner```는 최상위 랜드마크여야 함. main이나 다른 섹션 요소의 자식 요소로 사용되지 않은 경우 ```banner```의 역할이 할당됨
* 페이지에 중첩된 문서나 애플리케이션 역할이 포함된 경우, 각 역할에는 하나의 ```banner```랜드마크가 있을 수 있음 (e.g. ```iframe```, ```frame``` 요소 사용할 경우)
* 페이지에 둘 이상의 ```banner``` 랜드마크가 포함된 경우, 각 랜드마크에는 고유한 레이블이 있어야 함

```html
<body>
  <header>
    <h1>website information<h1>
    .... banner content....
  </header>
</body>
<!-- or -->
<div role="banner">
  <h1>page title identifying website<h1>
  .... banner content....
</div>
```

## navigation
> 사용자가 웹 페이지 또는 관련된 웹 페이지를 탐색하는 데 도움이 되는 링크의 집합을 식별하는 데 사용

* ```nav``` 요소는 암묵적으로 ```navigation```의 역할을 가지고 있음

```html
<nav aria-label="Primary">
  <!-- 스크린 리더가 읽을 때 '주요(primary) 네비게이션' 이라고 읽음 -->
    <ul>
        <li><a aria-current="page" href="/">Home</a></li>
        <li><a href="/menu">Our pizzas</a></li>
        <li><a href="/contact">Get in touch</a></li>
    </ul>
</nav>
```

## search
> 웹 사이트의 검색 수단을 함께 제공하는 요소들을 그룹화하는 데 사용

```html
<header>
  <h1>Movie website</h1>
  <search>
    <form action="./search/">
      <label for="movie">Find a Movie</label>
      <input type="search" id="movie" name="q" />
      <button type="submit">Search</button>
    </form>
  </search>
</header>

```
※ [search element1](https://www.scottohara.me/blog/2023/03/24/search-element.html) | [search element2](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/search)

## main
> 페이지에는 단 하나의 ```main```요소만 존재할 수 있음

```html
<header></header>
<main>
  main content
</main>
<footer></footer>
```

## region
> 사용자가 가장 관심을 갖고 탐색하고자 하는 페이지의 주요 영역들을 식별할 때 사용됨 

```html
<section aria-labelledby="our-pizzas-heading">
  <h2 id="our-pizzas-heading">Our pizzas</h2>
  <!-- 
    1. section을 지역 내비게이션 랜드마크로 바꿈
    2. h2의 내용을 통해 해당 section에 대한 고유한 이름이 부여됨
  -->
  <p>
    All our pizzas come with the best pizza topping in the world. Pineapple!
  </p>
  <ul>
    <li>Margherita with pineapple</li>
    <li>Veggie with pineapple</li>
    <li>Meaty with pineapple</li>
  </ul>
</section>
```

## complementary 
> 메인 콘텐츠와 분리되어도 여전히 의미를 가지면서, 메인 콘텐츠를 보완하는 콘텐츠를 식별할 때 사용됨

* ```aside```는 암묵적으로 보완(complementary)의 역할을 가짐
* 다른 랜드마크에는 포함되지 않으며, 최상위 레벨이어야 함
* 주요 내용과 관련이 없는 경우 좀 더 일반적인 역할을 할당해야 함
* 두 개 이상의 ```complementary``` 랜드마크가 포함된 경우, 각 랜드마크에는 고유한 라벨이 있어야 함

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

## from
> 양식을 생성하는 항목 및 객체의 컬렉션을 포함하기 위해 결합함

* form 랜드마크에는 사용자가 양식의 목적을 이해할 수 있도록 레이블이 있어야 함
* 눈에 보이는 제목 요소에 대해 ```aria-labelledby```를 사용해 식별해야 함
* 둘 이상의 랜드마크가 존재할 경우, 각 랜드마크의 고유한 레이블이 있어야 함

```html
<div class="newsletter">
    <h3 id="newsletter-subscribe-form-heading">
        Subscribe to Mr. Pineapple's newsletter
    </h3>
    <form
        aria-labelledby="newsletter-subscribe-form-heading"
        name="newsletter"
        action="/subscribe"
        type="post"
    >
        <label for="email">Please provide your email address</label>
        <input type="email" id="email" name="email" />

        <button type="submit">Pineapple Me 🍍</button>
    </form>
</div>
```

## contentinfo
> 페이지의 하단에서 저작권, 개인정보 보호 및 접근성 설명에 대한 링크와 같은 정보를 포함하는 공통 정보를 식별함

* 각 페이지에 하나의 ```contentinfo``` 랜드마크를 가짐
* ```contentinfo```는 최상위 랜드마크여야 함, main이나 다른 섹션 요소 내부에 위치하지 않도록 주의해야 함
* 페이지에 중첩된 문서나 애플리케이션 역할이 포함된 경우, 각 역할에는 하나의 ```contentinfo```랜드마크가 있을 수 있음 (e.g. ```iframe```, ```frame``` 요소 사용할 경우)
* 두 개 이상의 ```contentinfo``` 랜드마크가 포함된 경우, 각 랜드마크에는 고유한 라벨이 있어야 함

```html
<footer>
  <h2>Contact, Policies and Legal<h2>
  .... contentinfo area content ....
</footer>
<!-- or -->
<div role="contentinfo">
  <h2>Contact, Policies and Legal<h2>
  .... contentinfo area content ....
</div>
```


***

> 참고 페이지
> [ARIA Landmarks Example](https://www.w3.org/WAI/ARIA/apg/patterns/landmarks/examples/general-principles.html) | [HTML 랜드마크 역할을 사용하여 접근성 향상시키기](https://velog.io/@sejinkim/HTML-%EB%9E%9C%EB%93%9C%EB%A7%88%ED%81%AC-%EC%97%AD%ED%95%A0%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EC%97%AC-%EC%A0%91%EA%B7%BC%EC%84%B1-%ED%96%A5%EC%83%81%EC%8B%9C%ED%82%A4%EA%B8%B0)
