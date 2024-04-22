# @-Rule 정리

## @at-root
> 중첩에서 벗어날 때 사용됨

### 예제1
* 원본 sass
```css
.list{
  $w: 100px;
  $h: 50px;
  li{
    widht: $w;
    height: $h;
  }
@at-root .box{
    widht: $w;
    height: $h;
  }
}
```

* 변환된 css
```css
.list li{
  width: 100px;
  height: 50px;
}
.box{
  width: 100px;
  height: 50px;
}
```

### 예제2
* 원본 sass
```css
@media print{
  .page{
    width: 8in;
    @at-root(without: media){
      color: #111;
    }
    @at-root(with: rule){
      font-siez: 1rem;
    }
  }
}
```

* 변환된 css
```css
@media print{
  .page{
    width: 8in;
  }
}
.page{
  color: #111;
}
.page{
  font-size: 1rem;
}
```
___

## @for
### @for $var from (start number) to (end number) { ... }
> from ~to 의 경우 **미만**의 반복 값을 사용함
```css
/* sass */
@for $i from 1 to 3{
  .icon_#{ $i }{
    background-position: 0 ($i * -10px);
  }
}

/* css */
.icon_1{background-position: 0 -10px;}
.icon_2{background-position: 0 -20px;}
```


### @for $var from (start number) through (end number) { ... }
> from ~to 의 경우 **이하**의 반복 값을 사용함
```css
/* sass */
li{
  @for $i from 1 to 3{
    &:nth-last-child(#{$i}),
    &:nth-last-child(#{$i}) ~ li{
      width: calc(100%/ #{$i});
    }
  }
}

/* css */
li:nth-last-child(1), li:nth-last-child(1) ~ li {
  width: calc(100% / 1);
}
li:nth-last-child(2), li:nth-last-child(2) ~ li {
  width: calc(100% / 2);
}
li:nth-last-child(3), li:nth-last-child(3) ~ li {
  width: calc(100% / 3);
}
```

## @use
> dart-sass에서 사용 가능한 함수, 네임스페이스를 생성하여 전역으로 사용되던 import의 문제점을 보완 가능
> @use를 사용하여 가져온 스타일시트를 ```모듈(modules)```이라 부름

### 기본 형식
```css
//test.scss
$radius: 3px;
@mixin rounded{
  border-radius: $radius;
}

//style.scss
@use "/test";

.button{
  @include test.rounded;
  padding: 5px + tset.$radius;
}

//style.css
.button{
  border-radius: 3px;
  padding: 8px;
}
```

### 네임스페이스 선택
```css
//test.scss
$radius: 3px;
@mixin rounded{
  border-radius: $radius;
}

//style.scss
@use "/test" as t;

.button{
  @include t.rounded;
  padding: 5px + t.$radius;
}

//style.css
.button{
  border-radius: 3px;
  padding: 8px;
}
```
