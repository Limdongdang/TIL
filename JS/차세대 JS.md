let/const 변수
=====
> let과 const는 ES6(ECMAScript 2015)에서 새로 도입된 변수
### let
> let은 값을 재할당할 수 있는 변수를 선언할 때 사용
```js
let x = 10;
x = 20; // x의 값을 변경할 수 있음
}
```
### const
> const는 값을 재할당할 수 없는 상수를 선언할 때 사용
```js
const y = 10;
y = 20; // 오류 y는 상수이므로 값을 변경할 수 없음
```
## Arrow function
> ES6에서 도입된 새로운 함수 표현 방식 js 환경에서 함수를 생성하는 또 다른 방법
* 기존 함수 구문
```js
function funjs(x, y) { 
    return x + y;
}
```
* Arrow function
```js
const funjs = (x, y) => { 
    return x + y;
}
```
* 매개변수가 없다며 빈 괄호로 두면 된다.
```js
const funjs = () => { 
    return 0;
}
```
* 수의 매개변수가 하나인 경우 괄호를 생략 가능하다
```js
const funjs = x => {
    return x;
}
```
* return을 한 줄로 표시가 가능하다
```js
const funjs = x => x; // x를 반환
```
### arrow function을 쓰는 이유
1. 코드가 직관적이다.
2. 내부의 this 값을 재정의 하지 않는다

## Exports & Imports
리액트 프로젝트는 모듈이라 불리는 js파일들에 코드를 분리함
이런 파일들을 연결 하기 위해 Exports & Imports가 필요하다.

> export 두 가지 방식으로 할 수 있는데 default 방식과 named 방식이 있다.
## spread operator
```...```이 구문으로 사용 가능 배열이나 객체의 요소를 가져올 수 있다.
## Destructuring
배열이나 객체 값에 쉽게 액세스 하는 방법
## 참고
* https://developer.mozilla.org/ko/docs/Web/JavaScript
