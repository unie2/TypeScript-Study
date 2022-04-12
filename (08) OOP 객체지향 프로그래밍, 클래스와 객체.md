## 1. 객체지향 프로그래밍(Object Oriented Programming) 이란 ?
  - 연관된 변수와 함수들을 한 덩어리로 묶어서 구조화하여 표현하는 프로그래밍 스타일이다.
  - 어플리케이션을 실제 세상에 존재하는 객체와 같은 단위로 쪼개고 객체들이 서로 상호 작용함으로써 시스템이 동작되는 것이다.  
    > 객체 : 연관된 변수와 함수들의 집합  
  
------------------
## 2. 클래스(Class)
  - 객체는 클래스를 통해서 만들어 질 수 있고 클래스는 객체가 어떤 모습을 가질지를 정의하고 묘사하는 설계도, 생산 틀이라고 할 수 있다.
  - 클래스 내에서는 let이나 const와 같은 키워드가 필요하지 않는다.
  - 클래스 내에서 정의된 변수들은 클래스 속에서 this 키워드를 통해 접근이 가능하다.  
    > 그러므로 클래스 속에서 정의된 함수들은 상대적으로 적은 매개변수를 가진다는 장점이 있다.  
  ```typescript
  class Employee {
    fullName: string;
    age: number;
    jobTitle: string;
    hourlyRate: number;
    workingHoursPerWeek: number;

    printEmployeeDetails = ():void => {
        console.log(`${this.fullName}의 직업은 ${this.jobTitle}이고
        일주일의 수입은 ${this.hourlyRate * this.workingHoursPerWeek} 달러 이다.`)
    }
  }
  
  ```
  ### 2-1. 참고
   - 프로퍼티(Property) : 클래스 내에 정의된 변수
   - 메소드(Method) : 클래스 내에 정의된 함수

------------------
## 3. 객체(Object)
  - 클래스를 통해 객체를 생성할 때 새로운 인스턴스를 만든다.
  ```typescript
  class Employee {
    fullName: string;
    age: number;
    jobTitle: string;
    hourlyRate: number;
    workingHoursPerWeek: number;

    printEmployeeDetails = ():void => {
        console.log(`${this.fullName}의 직업은 ${this.jobTitle} 이고 일주일의 수입은 ${this.hourlyRate * this.workingHoursPerWeek} 달러 이다.`)
    }
  }
  
  // Employee 클래스를 바탕으로 Employee1 객체 생성
  let Employee1 = new Employee(); 
  Employee1.printEmployeeDetails() 
  //결과: undefined의 직업은 undefined 이고 일주일의 수입은 NaN 달러 이다.
  
  // 값 할당 후 함수 호출
  let employee1 = new Employee();
  employee1.fullName = '민수';
  employee1.age = 28;
  employee1.jobTitle = '주니어 웹개발자';
  employee1.hourlyRate = 40;
  employee1.workingHoursPerWeek = 35;
  employee1.printEmployeeDetails();
  // 결과: 민수의 직업은 주니어 웹개발자이고 일주일의 수입은 1400 달러 이다.
  
  ```
  - 이와 같이 클래스를 통해 여러가지 독립된 객체를 만들 수 있다.
------------------

[출처](https://www.youtube.com/watch?v=bdXnsyelOGg&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=9)
