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