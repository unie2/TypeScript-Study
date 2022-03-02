## 1. 정적 타이핑(Static Typing) 이란?
  - 타입을 선언하고 선언된 타입에 맞는 값만이 할당 또는 반환되어야 한다는 의미이다.

------------------

## 2. 타입 추론(Type Inference) 

- 타입스크립트에서는 타입 표기가 없는 경우 타입 정보를 제공하기 위해 타입을 추론한다.
```javascript
let a = 5;
// 변수 선언 시 변수의 할당값이 숫자이므로, 타입 추론에 의해 변수 a의 타입은 자동으로 숫자로 결정된다.
// a = 'hello'; // 에러 발생
a = 10; // 정상
```

------------------
[출처](https://www.youtube.com/watch?v=rwqqhvR353A&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=4)
