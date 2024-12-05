# ```@import```는 더이상 사용되지 않는다. [#sass-lang](https://sass-lang.com/blog/import-is-deprecated/)
<br>
dart sass가 1.80.0버전으로 업데이트 되면서부터 @import를 사용하지 못하게 되었다.<br>
vue3로 이관 작업을 하다 sass 빌드가 되지 않아 기존 파일들을 어떻게 수정했는지 예시로 남겨둔다.
<br>
<br>

## ```@use```의 사용

```@import```를 사용하던 구문을 ```@use 'path' as var;``` 로 변경해야 한다. <br>
use로 불러온 데이터를 사용하기 위해서는 정의한 변수 값을 사용해야 한다.
<br>
<br>
**예시**<br>
*- 변경 전*
```sass
@import "./common/_variable";
@import "./common/_mixin";

.test1{
    font-size: $fs14;
    color: $primary;
}
.test2{
    @include commonTestContent;
}
```
*- 변경 후*
```sass
@use './common/_variable' as vars;
@use './common/_mixin' as mixin;

.test1{
    font-size: vars.$fs14;
    color: vars.$primary;
}
.test2{
    @include mixin.commonTestContent;
}
```
<br><br>

## ```mixin```을 사용할 때 변수를 사용하면 key값을 정의해야 함
기존의 mixin에서는 include 시 mixin에서 사용되는 ```$변수``` 의 값을 별도 지정하지 않았지만 업데이트 이후부터는 해당 변수 또한 데이터 값으로 지정해 주어야 한다.
<br>
<br>
**예시**<br>
*- 변경 전*
```sass
// _mixin.scss

@mixin testFunction {
    width: $iconSize;
    height: $iconSize;
    border-radius: $iconRadius;
}

// style.scss
@use './common/_mixin' as mixin;

$iconSize: 1.6rem;
$iconRadius: 0.8rem;

.title{
    @include testFunction;
}
```
*- 변경 후*
```sass
// _mixin.scss

@mixin testFunction($iconSize, $iconRadius) {
    width: $iconSize;
    height: $iconSize;
    border-radius: $iconRadius;
}

// style.scss
@use './common/_mixin' as mixin;

$iconSize: 1.6rem;
$iconRadius: 0.8rem;

.title{
    @include mixin.testFunction($iconSize, $iconRadius);
}
```
<br><br>


## ```중첩 규칙```
기존 @include를 사용할 때는 어느 위치에서 호출을 하든 경고문이 뜨지 않았는데, 업데이트 이후부터는 선언 순서를 확인하라는 경고문이 발생한다.
<br>
<br>
**예시**<br>
*- 변경 전*
```sass
// _mixin.scss
@import './common/_variable_';
@import './common/_mixin';

.title{
    display: flex;
    color: vars.$txt-black;
    &:hover{
        color: vars.$parimary;
    }
    @include testFunction;
}
```
*- 변경 후*
```sass
@use './common/_variable_' as vars;
@use './common/_mixin' as mixin;

.title{
    display: flex;
    color: vars.$txt-black;
    @include testFunction;
    &:hover{
        color: vars.$parimary;
    }
}
```
<br><br>

