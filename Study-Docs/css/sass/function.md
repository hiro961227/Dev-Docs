# 함수

## map-get($map, $key)
> key를 통해 value값을 취득할 수 있음

```css
//원본 scss
$testColor : (
  primary: #F79B06;
  error: #EB2F00;
  success: #3769f4;
);

.testSuccess {
  color: map-get($testColor, success);
}
.testError {
  background-color: map-get($testColor, error);
}

//출력 css
.testSuccess{
  color: #EB2F00;
}
.testError{
  background-color: #3769f4;
}
```
