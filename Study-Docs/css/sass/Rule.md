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
