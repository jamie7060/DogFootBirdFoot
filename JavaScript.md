자바스크립 개념 정리
=====

•	Promises
Promise 개체는 비동기 작업의 최종 완료(또는 실패)와 결과 값을 나타낸다. 3가지 상태를 갖는다. pending: promise가 생성되어 데이터를 기다리는 경우. fufilled: 비동기 작업이 성공적으로 처리된 경우. rejected: 비동기 작업이 실패한 경우. fetch() 함수는 promise의 상태를 나타내는 객체를 반환한다.

•	Const / Let
Const.는 상수(const)의 준말이다. 자바스크립트 키워드로서 값이 변하지 않는 변수를 생성한다. 변수는 데이터를 담는 상자로 비유할 수 있다. Const 변수에 새로운 값을 넣으면(assign하면) TypeError가 뜨게 된다.
Let 변수는 const 변수와 달리 새로운 값을 부여(reassign)할 수 있다. 프로그램을 실행하는 과정에서 부여된 값이 변하지 않는 변수는 const 그렇지 않은 경우 let을 이용한다. 

•	Arrow Functions
() => 로 표현되는 함수이며, =를 통해서 변수가 함수를 담고 있음을 나타낸다. Arrow function syntax는 함수 표현(function expression)의 축약형이다. 화살표 함수 표현(arrow function expression)은 자신의 this, arguments, super 또는 new.target을 바인딩 하지 않는다. 화살표 함수는 항상 익명(anonymous)으로 존재한다. 이 함수 표현은 메소드 함수가 아닌 곳에 가장 적합하며 생성자로서 사용할 수 없다. Arrow function은 concise body 형태로 축약해서 표현할 수 있는데, 아래 세 경우에 해당한다. 1. 한 개의 parameter를 받는 경우 ()를 생략 가능(0개는 안 됨). 2. 한 블록으로 된 코드의 경우 ‘=>’ 뒤에 그 내용을 쓰고 return을 생략할 수 있다. 3. 한 블록으로 된 경우 {} 를 생략할 수 있다. 여기서 블록은 {} 괄호를 의미한다.

•	Array Methods (map, reduce, filter, slice, splice) 
자바스크립트는 array를 위한 built-in method들을 갖고 있다.
map: Iterator의 일종으로 배열 내의 모든 요소 각각에 대하여 제공된 함수(callback)를 호출하고, 그 결과를 모아서 새로운 배열을 반환한다.
reduce: 누산기(accumulator)와 배열의 각 요소(왼쪽에서 오른쪽으로)에 대해 하나의 단일 값(single value)으로 줄이는 함수를 적용한다. 문법은 다음과 같다. arr.reduce(callback[, initialValue]) callback 함수는 accumulator, currentValue, currentIndex, array를 인수로 받으며 initialValue는 accumulator의 시작 값을 정해준다. initialValue를 정하지 않았을 경우 배열의 첫 요소가 시작 값이 된다.
slice: 어떤 배열의 begin부터 end까지(end는 불포함)에 대한 shallow copy를 새로운 배열 객체로 반환한다. 원본 배열은 수정되지 않는다. 추출할 시작 부분과 끝부분을 parameter로 받고 -1은 맨 끝, -2는 끝에서 두번째를 의미한다.
splice: 메소드는 배열에 있는 요소를 삭제하고(하거나) 배열에 새 요소를 추가한다. 배열의 지정된 부분을 삭제하거나 요소를 추가하고자 할 때 그에 대한 정보를 매개변수로 받아 실행된다.

•	Spread Operator (Array/Object Spread)
전개 연산자(spread operator)는 표현식(expression)은 2개 이상의 인수arguments(함수 호출 용)나 2개 이상의 요소elements(배열 리터럴 용) 또는 2개 이상의 변수(비구조화 할당 용)가 예상되는 곳에 확장될 수 있도록 한다. Spread 구문을 사용하면 배열이나 문자열과 같이 반복 가능한 문자를 0개 이상의 인수 (함수로 호출할 경우) 또는 요소 (배열 리터럴의 경우)로 확장하여, 0개 이상의 키-값의 쌍으로 객체로 확장시킬 수 있다. 배열의 ,로 구분되는 값들이 함수 argument 등으로 사용할 수 있게끔 한다. Array, object의 복잡한 코드를 단순화 하기 좋다.

•	Export / import
Module은 다른 프로그램에서 다시 사용할 수 있게끔 코드를 부분부분 나눠 놓은 것을 말한다. Export를 통해 Module을 다른 곳에서 접근하여 사용할 수 있게 할 수 있다. 객체를 module.exports를 통해 Export 할 수 있다. ES6에서는 export를 하기 위한 방법으로 default export와 named exports를 제시하고 있다. ES6에서는 module.export를 대체하여 export default를 사용하며 자바스크립트 객체, 함수, primitive data type들을 export할 수 있다. Named exports는 변수를 이용하여 데이터를 export할 수 있게 해준다. {}안에 지정된 변수를 export하며 선언과 동시에 export할 수 있다는 특징이 있다. as keyword는 named export 과정에서 변수명을 바꿀 수 있도록 하는 기능을 수행한다.
Export된 module을 현재 프로그램에서 불러와 사용하는 것을 import라고 한다. 이는 require() 함수를 통해 이루어진다. ES6에서는 import keyword를 사용하여 import를 할 수 있다. 또한 named imports를 사용하여 변수로 지정된 객체를 불러올 수 있다. as keyword는 named import 과정에서 변수명을 바꾸거나 *을 이용하여 전체 모듈을 alias로 불러올 수 있도록 하는 기능을 수행한다
