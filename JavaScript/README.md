# JavaScript 기초

### JavaScript의 표기법

1. dash-case(kebab-case) <br/>
HTML, CSS에서 주로 사용한다. <br/>
the-quick-brown-fox-jumps-over-the-lazy-dog

2. snake_case <br/>
HTML, CSS에서 주로 사용한다. <br/>
the_quick_brown_fox_jumps_over_the_lazy_dog

3. **camelCase** <br/>
JS에서 주로 사용한다. <br/>
theQuickBrownFoxJumpsOverTheLazyDog

4. ParcelCase <br/>
JS에서 사용하지만 특수한 경우에 사용한다. <br/>
TheQuickBrownFoxJumpsOverTheLazyDog

프로그래밍 환경에서는 Zero-based Numbering 0 기반으로 번호를 매긴다. 특수한 경우를 제외하고 0부터 숫자를 시작한다.
- [Zero-based Numbering 0](https://en.wikipedia.org/wiki/Zero-based_numbering)에 대한 Wiki 문서

 ### 데이터 종류(자료형)
 
- string(문자 데이터) <br/>
따옴표를 사용한다.

```jsx
let myName = "pearl"
let email = 'pearl-maris@nnn.com'
let hello = `Hello ${myName}?!`

console.log(myName);
console.log(email);
console.log(hello);
```

- number(숫자 데이터) <br/>
정수 및 부동소수점 수자를 나타낸다.

```jsx
let number = 123;
let opacity = 1.57;
// number는 따옴표 사용하지 않는다. 그건 문자(String)다.

console.log(number);
console.log(opacity);
```

- boolean <br/>
true, false 두 가지 값 밖에 없는 논리 데이터

```jsx
let checked = true;
let isShow = false;

console.log(checked);
console.log(isShow);
```

- underfined <br/>
값이 할당되지 않는 상태를 나타낸다.

```jsx
let undef;
let obj = { abc: 123 };

console.log(undef);
console.log(obj.abe);
console.log(obj.xyz);
```

- null <br/>
어떠한 값이 **의도적으로 비어있음**을 의미한다.

```jsx
let empty = null;

console.log(empty);
```

- object(객체 데이터) <br/>
여러 데이터를 Key:Value 형태로 저장한다. 객체 데이터는 {}를 쓴다.

```jsx
let user = {
	name : 'monroe',
	age : 23,
	isValid: true
};

console.log(user.name);
console.log(user.age);
console.log(user.isValid);
```

- array 배열 <br/>
**여러 데이터를 순차적으로 저장**한다. 배열을 사용할 때는 []를 쓴다.

```jsx
let fruits = ['Apple', 'Banana', 'Cherry'];

console.log(fruits[0]);
console.log(fruits[1]);
console.log(fruits[2]);
```

객체 데이터와 배열 쓸 때 쓰는 기호는 절대 헷갈리지 말도록 한다.


```jsx
let fruits = ['Apple', 'Banana', 'Cherry']

console.log(fruits[0]);
console.log(fruits[1]);
console.log(fruits[2]);

console.log(new Date('2022-01-29').getDay());
console.log(new Date('2022-01-30').getDay());
console.log(new Date('2022-01-31').getDay());

// 보통 이러한 주석을 사용함
/* 한 줄 메모 */
/**
 * 여러 줄을 메모할 때는
 * 이런 주석을
 * 사용한다.
 */
```
### 변수
데이터를 저장하고 참조(사용)하는 데이터의 이름

1. let
2. const
3.  ~~var~~

```jsx
// 재사용이 가능
// 변수 선언
let a = 2;
let b = 5;

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
//let이라는 키워드를 사용해서 a라는 변수 이름을 지정하고 2를 저장하는 것을 변수를 선언한다라고 한다.

// let 키워드를 사용해서 값(데이터)의 재할당 가능!
let a = 12;
console.log(a);

a = 999;
console.log(a);

// const에는 값(데이터)의 재할당이 불가능하다
const a = 12;
console.log(a);

a = 999;
console.log(a); //TypeError
```

### 예약어
특별한 의미를 가지고 있어, 변수나 함수 이름 등으로 사용할 수 없는 단어 <br/>
if, this, break 등등

```jsx
let this = 'Hello'; // syntaxError(문법에러) 예약어를 쓰면 이렇게 뜬다
let if = 123;
let break = true;
```

### 함수 (function)
특정 동작(기능)을 수행하는 일부 코드의 집합(부분)

```jsx
//함수 선언
function helloFunc() {
	//실행 코드
	console.log(1234);
}

//함수 호출
helloFunc(); // 1234

/// 123숫자를 반환시킨다.
function returnFunc() {
	return 123;
}
let a = returnFunc(); //호출된다는건 실행한다()는 뜻
console.log(a);

//함수 선언!
function sum(a, b) { //a와 b는 매개변수(Parameters)
	return a + b;
}

//재사용!
let a = sum(1, 2); // 1과 2는 인수(Arguments)
let b = sum(7, 12);
let c = sum(2, 4);

console.log(a, b, c);
```

```jsx
//아래와 같은 것을 기명(이름이 있는)함수
//함수 선언
function hello() {
	console.log('hello~');
};

//익명(이름이 없는)함수. 아래와 같이 이름도 없이()를 시작하면 익명함수
//이것을 함수 표현한다라고 한다.
let world = function () {
	console.log('World!!');
};

//함수 호출
hello();
world();

//객체 데이터
const monroe = {
	name: 'monroe',
	age: 23;
	//메소드 Method(함수의 표현. 속성 부분에 함수가 할당되어 있으면 메소드라고 부른다)
	getName: function () {
		return this.name;
	}
};

const shesName = monroe.getName();
console.log(shesName);
//혹은
console.log(monroe.getName());
```

### 조건문

조건의 결과(truthy, falsy)에 따라 다른 코드를 실행하는 구문

if, else

#### if

```jsx
let isShow = true;
let checked = false;

if (isShow) {
	console.log('Show!');
} //조건구문

if (checked) { //false는 '조건에 부합하지 않는다' 라고 한다
	console.log('Checked!');
}
```

#### else

```jsx
let isShow = true;

if(isShow) {
	console.log('Show!');
} else {
	console.log('Hide?'); //실행되지 않음
}

let isShow = false;

if(isShow) {
	console.log('Show!'); //실행되지 않음
} else {
	console.log('Hide?');
}
```

### DOM API

Document Object Model. Application Programming Interface

자바스크립트에서 HTML을 제어하는 명령들

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <script src="./main.js"></script>
</head>
<body>
  <div class="box">box</div>
</body>
</html>
```

위와 같이 작성된 script 코드는 div.box를 읽지 못한다. 그 이유는 코드를 위에서 아래로 읽어내리는데 갑자기 script에서 main.js 읽어서 브라우저에 적용하려고 해달라고 했지만 아직 밑의 내용을 아직 읽지 않았기 때문에 div.box를 가진 요소를 찾을 수가 없었던 것이다.


```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <div class="box">box</div>
  <script defer src="./main.js"></script>
</body>
</html>
```

head 태그 안(정보의 부분)에서 scirpt(정보)를 적용시키는데, 저러한 반응 때문에 body(구조의 부분)에 적용시키는 일은 그다지 좋은 방법은 아니다. 그래서 `defer`라는 속성을 추가하는데 이것은 html을 다 읽은 상태서 script를 실행해 달라고 하는 것이다.

```jsx
// HTML 요소(Element) 1개 검색/찾기
const boxEl = document.querySelector('.box');

// HTML 요소에 적용할 수 있는 메소드
boxEl.addEventListener();

// 인수(Arguments)를 추가 가능
boxEl.addEventListener(1, 2);

// 1 - 이벤트(Event, 상황)
boxEl.addEventListener('click', 2);

// 2 - 핸들러(Handler, 실행할 함수(익명함수))
boxEl.addEventListener('click', function () {
  console.log('Click~!');
});
```

```jsx
// HTML 요소 (Element) 검색/찾기
const boxEl = document.querySelector('.box');

// 요소의 클래스 정보 객체 활용
boxEl.classList.add('active');
let isContains = boxEl.classList.contains('active'); //active라는 클래스가 있는지 확인함
console.log(isContains); //active라는 클래스가 있어서 true를 띄운다.

boxEl.classList.remove('active');
isContains = boxEl.classList.contains('active'); //let으로 재할당된 부분, 클래스 active가 포함되어있는지 확인하는 구문
console.log(isContains); // active가 포함이 되지 않아서 false가 뜬다
```

여기서 let을 써서 재할당이 된 것이다. 만약 여기에 const를 썼다면 재할당이 되지 않았을 것이다.

contains() 명령어

```jsx
// HTML 요소(Element)요소 검색/찾기
const boxEls = document.querySelectorAll('.box');
console.log(boxEls);

// 찾은 요소들 반복(forEach)해서 함수 실행
// 익명 함수를 인수로 추가
boxEls.forEach(function () {});
// boxEls는 복수 형태로(querySelectorAll로 .box 들을 포함하고 있는 형태로 배열데이터로 만들어진다,
// 정확하게는 배열 데이터가 아니라서 유사배열(array-like)이라는 형태를 갖춘다)

// 첫 번째 매개변수(boxEl): 반복 중인 요소.
// 두 번째 매개변수(index): 반복 중인 번호.
boxEls.forEach(function (boxEl, index) {});

// 출력
boxEls.forEach(function (boxEl, index) {
  boxEl.classList.add(`order-${index + 1}`);
  console.log(index, boxEl);
})
```

이러한 데이터가 어떻게 동작되는지 머릿속에 그려내려면 데이터의 종류를 반드시 숙달해야함!

textContent 속성 
```jsx
const boxEl = document.querySelector('.box');

// Getter, 값을 얻는 용도
console.log(boxEl.textContent); //Box

// Setter, 값을 지정하는 용도
boxEl.textContent = 'Monroe';
console.log(boxEl.textContent); //monroe;
```