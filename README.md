# aimad_dw

# Chapter 1
- Example 1-1
: 변수 설정

- Example 1-2
: 변수 선언과 값을 할당

- Example 1-3
: primitive data는 모두 불변값이기 때문에 한 번 만들어진 값은 절대 변하지 않는다는 것을 보여준다.
이를 immutable이라 한다.

- Example 1-4
: reference data의 할당. var이 직접 data가 아닌 address를 가르키며 data는 address에 대한 메모리를 할당받는 것을 설명해주고 있음

- Example 1-5
: reference data의 재할당. 기존에 있던 data는 삭제되지 않기 때문에, var의 data를 바꿀 경우 새로운 data를 만든 후에 var가 그 주소를 가르키도록 한다.

- Example 1-6
: 중첩된 reference data의 프로퍼티 할당. array에 index 각각의 indentifier를 할당한다.

- Example 1-7
: 변수 복사. 하나의 객체(b)가 값을 가진 객체(a)를 copy할 경우 객체(a)가 가르키는 주소를 동일하게 가르킨다.

- Example 1-8
: 변수 복사 이후 객체의 **프로퍼티**를 변경할 경우 저장되어 있던 기존의 data가 바뀐다. 

- Example 1-9
: 변수 복사 이후 객체 자체를 변경할 경우 기존의 data는 변하지 않고 새로운 data가 메모리에 할당되어 객체와 연결된다.

- Example 1-10
: 객체의 가변성에 따른 문제점을 보여준다. 정보가 바뀐 시점을 알고 싶을 경우, 변경 전과 후에 객체가 서로 다른 객체를 가르키도록 만들어야한다.

- Example 1-11
: Example 1-10의 문제점의 해결 방법이다. 새로운 object를 만들고, 그 주소를 return 하여 두 객체가 서로 다른 객체를 보도록 만들었다.

- Example 1-12
: 기존 정보를 복사하여 새로운 객체를 반환하는 것을 얕은 함수라 부른다.
  result가 target의 정보를 복사하고 있다.

- Example 1-13
: copy0bject 기능을 이용하여 객체를 복사하는 방법. for loop 없이 함수를 통해 복사가 가능하다.

- Example 1-14
: 중첩된 객체에 대한 얕은 복사. user2가 user1의 정보를 복사하고 있다.

- Example 1-15
: Example 1-14에서 user.urls 프로퍼티를 불변 객체로 만듦.
  copy0bject를 통해 urls까지 따로 복사하여 불변 객체를 만들고 있다.

- Example 1-16
: 객체의 깊은 복사를 수행함. target의 property까지 복사하여 target과 result가 가르키는 것이 다르도록 함.

- Example 1-17
: 얕은 복사와 깊은 복사를 함께 수행함. 얕은 복사로 인해 a b c d 는 (단, 가르키는 것이 다름) 동일하게 갖고있으나 a b c d가 가르키는 data가 다르다.

- Example 1-18
: JSON function을 이용하여 깊은 복사를 진행한다. for loop 없이 함수를 통해 복사가 가능하다.

- Example 1-19
: undefined가 부여되는 경우를 설명.
 (1) 값을 대입하지 않은 변수에 접근한 경우
 (2) 존재하지 않는 프로퍼티에 접근한 경우
 (3) 반환 값이 없는 경우

- Example 1-20
: array data를 사용했을때 undefined가 나타나는 경우를 설명. arr3에서 나온 결과 [undefined]는 error의 undefined가 아니라 data 이다.
  배열에 들어간 data가 없을 경우 empty로 나타남.
  (비어있음을 나타내고 싶을 때는 undefined가 아닌 null을 사용해야 한다.)

- Example 1-21
: 정의된 arr1 arr2 array가 forEach, map, filter, reduce 함수를 사용했을 때의 결과를 나타낸다.
 (1) forEach : Array에 있는 모든 element에 대해 for loop를 진행함 (v:array[i], i:index)
 (2) map : 새로운 array element 생성 (new_array[i] <- v + i)
 (3) filter : 조건에 맞지 않는 element 제거, 새로운 array 생성
 (4) reduce : transform (p <- p + array[i] + i)

- Example 1-22
: undefined와 null을 비교함. null의 type은 object이기 때문에 사용에 주의해야 함.
  '==' '==='의 차이는 후자의 경우 더 엄격하게 구분한다. 








# Chapter 2
- Example 2-1
: 실행 컨텍스트와 콜 스택. 
  global E.context, outer E.context, inner E.context 순으로 stack에 쌓여 inner 부터 global까지 하나씩 out되는 과정이다.

- Example 2-2
: 매개변수와 변수에 대한 Hoisting.
  global, a 순으로 stack에서 쌓이고 a, global 순으로 처리된다.
  function a () {} ; function에 대한 declaration

- Example 2-3
: 매개변수와 변수에 대한 Hoisting 2.
  매개변수가 변수의 선언 및 할당과 같다고 여겨져 함수 안에서 매개변수가 선언되었다. 

- Example 2-4
: 매개변수와 변수에 대한 Hoisting 3.
  var x; 3줄이 순서대로 수집 대상 1,2,3의 변수 선언 부분을 뜻한다. 

- Example 2-5
: 함수 선언의 Hoisting.
  선언 부분 처리 후에 data가 할당되어 첫번째 console.log(b)는 function b() {}, 두번째와 세번째는 bbb를 나타낸다.

- Example 2-6
: 함수 선언의 Hoisting 2.
  선언 부분이 위에서 처리됨. Example 2-5와 결과는 같다.

- Example 2-7
: 함수 선언의 Hoisting 3.
  var b = function b() {}; 으로 바뀌었다.
  Example 2-5,6 과 같이 Var b가 두 번 선언되지 않고 한 번만 선언되어 function을 가르키게 된다.

- Example 2-8
: 함수를 정의하는 방식에 대한 설명.
  (1) function a() {}          //함수선언문
  (2) var b = function () {}   //익명함수표현식
  (3) var c = function d() {}  //기명함수표현식

- Example 2-9
: 함수 선언문과 함수 표현식. 함수 선언문 sum과 함수 표현식 multiply가 있다.

- Example 2-10
: 함수 선언문과 함수 표현식 2. 함수 선언문은 전체를 Hoisting하고 함수 표현식은 변수 선언부만 Hoisting한다.
  multiply function 에서 선언부만 호이스팅되어 찾을 수 없기 때문에 TypeError: multiply is not a function이 출력된다.
  변수의 할당부는 제자리에 남겨둠

- Example 2-11
: 함수 선언문의 위험성.
  전역 컨텍스트가 활성화될 때 처음 할당된 sum 함수에 두번째 sum 함수가 덮어쓰기 된다. 따라서 첫번째 sum 함수가 실행되지 않는 문제가 생긴다.

- Example 2-12
: Example 2-11의 문제로 인해 함수 표현식이 상대적으로 안전하다는 것을 보여줌.

- Example 2-13
: 스코프 체인이란 outerEnvironmentReference가 현재 호출된 함수가 선언될 당시의 LexicalEnvironment를 참조하는 것을 의미한다.
  Call stack에 global, outer, inner 함수 순으로 쌓여 inner부터 실행되는데, 모든 context는 내부/외부 환경이 있어 각 함수의 외부 환경이 '식별자의 유효범위'를 차례대로 검색해나간다.

- Example 2-14
: 스코프 체인 example 1.

- Example 2-15
: 스코프 체인 example 2.

- Example 2-16
: 스코프 체인 example 3.








# Chapter 3
- Example 3-1 & 3-2
: 전역 공간에서의 this.
  전역 컨텍스트를 생성하는 주체가 전역 객체이기 때문에 전역 공간에서의 this는 전역 객체를 가르킨다.
  browser 환경에서 전역객체는 window이고, Node.js 환경에서는 global이다.  

- Example 3-3
: 전역변수와 전역객체.
  자바스크립트의 모든 변수는 실은 특정 객체의 프로퍼티로서 동작하기 때문에, 전역변수 선언 시 이를 전역객체의 property로도 할당한다.

- Example 3-4
: 전역변수와 전역객체 2.
  Example 3-3 내용을 덧붙여서, 전역 공간에서는 var로 변수를 선언하는 대신 window의 프로퍼티에 직접 할당하더라도, 결과적으로 var로 선언한 거과 똑같이 동작하는 것을 확인할 수 있다.

- Example 3-5
: 전역변수와 전역객체 3.
  전역변수 선언과 전역객체의 프로퍼티 할당 사이에 전혀 다른 경우도 있는데, 'delete' 명령의 경우이다.
  다만 example을 보았을때 delete.window의 경우 삭제가 되지만, delete의 경우는 그렇지 않다. 전역변수를 선언하면 자바스크립트 엔진이 이를 자동으로 전역객체의 프로퍼티로 할당하면서,
  해당 프로퍼티의 configurable 속성(변경 및 삭제 가능성)을 false로 정의하는 것이다.

- Example 3-6
: 함수로서 호출, 메서드로서 호출.
  함수는 그 자체로 독립적인 기능을 수행하고, 메서드는 자신을 호출한 대상 객체에 관한 동작을 수행한다.
  함수 앞에 '.'이 있는지의 여부만으로 간단하게 구분할 수 있다.

- Example 3-7
: 메서드로서 호출 - 점 표기법, 대괄호 표기법.
  어떤 함수를 호출할 때 그 함수 이름 앞에 객체가 명시되어 있는 경우에는 메서드로 호출한 것이고, 그렇지 않은 모든 경우에는 함수로 호출한 것이다.

- Example 3-8
: 메서드 내부에서의 this.
  this에는 호출한 주체에 대한 정보가 담긴다. 어떤 함수를 메서드로서 호출하는 경우 호출 주체는 바로 함수명 앞의 객체이다.
  점 표기법의 경우 마지막 점 앞에 명시된 객체가 곧 this이다.

- Example 3-9
: 내부 함수에서의 this.
  첫번째의 this는 obj1, 두번째는 window, 세번째는 obj2를 뜻한다.
  this 바인딩은 함수를 실행하는 당시의 주변 환경은 중요하지 않고, 오직 해당 함수를 호출하는 구문 앞에 점 또는 대괄호 표기가 있는지 없는지가 관건이다.

- Example 3-10
: 내부 함수에서 this를 우회하는 방법.
  변수를 활용해 this를 우회할 수 있다. example에서 변수 self가 이 역할을 하여 this를 우회한다.

- Example 3-11
: this를 바인딩하지 않는 함수.
  this가 전역객체를 바라보는 문제를 보완하고자, 화살표 함수를 사용한다.
  화살표 함수는 실행 컨텍스트를 생성할 때 this 바인딩 과정 자체가 빠지게 되어, 상위 스코프의 this를 그대로 활용할 수 있다.

- Example 3-12
: 콜백 함수 내부에서의 this.
  콜백 함수란 함수 A의 제어권을 다른 함수(or 메서드) B에 넘겨주는 경우의 함수 A를 말한다.
  example에서 setTimeout 함수는 시간 지연을 한 뒤 콜백함수를 실행하라는 명령이다.
  forEach 메서드는 배열의 각 요소를 앞에서부터 차례로 하나씩 꺼내어 그 값을 콜백 함수의 첫번째 인자로 삼아 함수를 실행하라는 명령이다.
  addEventListener는 지정한 HTML 엘리먼트에 'click' 이벤트가 발생할 때마다 그 이벤트 정보를 콜백 함수의 첫번째 인자로 삼아 함수를 실행하라는 명령이다.

- Example 3-13
: 생성자 함수.
  자바스크립트는 함수에 instance를 만들어내는 생성자로서의 역할을 부여했다.
  example의 new 명령어로 함수를 호출하면 해당 함수가 생성자로서 동작하게 된다. 

- Example 3-14 & 3-15
: call 메서드.
  call 메서드는 메서드의 호출 주체인 함수를 즉시 실행하도록 하는 명령이다.
  함수를 그냥 실행하면 this는 전역객체를 참조하지만 call 메서드 이용 시 임의의 객체를 this로 지정할 수 있다.
  
- Example 3-16
: apply 메서드.
  call 메서드와 기능적으로 완전히 동일하지만, call은 첫번째 인자를 제외한 나머지 모든 인자들을 호출할 함수의 매개변수로 지정하는 반면, apply는 두번째 인자를 배열로 받는다.

- Example 3-17
: call/apply 메서드의 활용 1-1) 유사배열객체에 배열 메서드를 적용.
  객체에는 배열 메서드를 직접 적용할 수 없지만, slice 메서드를 통해 복사본을 배열로 반환한다.

- Example 3-18
: call/apply 메서드의 활용 1-2) arguments, NodeList에 배열 메서드를 적용.
  함수 내부에서 접근할 수 있는 arguments 객체도 유사배열객체이므로 example 3-17 방법으로 활용할 수 있다.
  querySelectorAll, getElementsByClassName 등의 Node 선택자로 선택한 결과인 NodeList도 마찬가지이다.

- Example 3-19
: call/apply 메서드의 활용 1-3) 문자열에 배열 메서드 적용 예시.
  유사배열객체에는 call/apply 메서드를 이용해 모든 배열 메서드를 적용할 수 있고, 배열처럼 index와 length를 가진 문자열도 적용할 수 있다.
  단, 문자열의 경우 length 프로퍼티가 Read only 이므로 원본 문자열에 변경을 가하는 메서드에는 오류가 발생하며,
  concat 같은 대상이 반드시 배열이어야 하는 경우에는 에러가 나지 않지만 올바른 결과를 얻을 수 없다.

- Example 3-20
: call/apply 메서드의 활용 1-4) ES6의 Array.from 메서드.
  유사배열객체 또는 순회 가능한 모든 종류의 데이터 타입을 배열로 전환하는 Array.from 메서드를 새로 도입함.

- Example 3-21
: call/apply 메서드의 활용 2) 생성자 내부에서 다른 생성자를 호출.
  생성자 내부에 다른 생성자와 공통된 내용이 있을 경우 call or apply를 이용해 간단하게 반복을 줄인다.
  example에선 생성자 함수 내부에서 Person 생성자 함수를 호출하고 있다.

- Example 3-22
: call/apply 메서드의 활용 3-1) 최대/최솟값을 구하는 코드를 직접 구현.
  여러 개의 인수를 받는 메서드에게 하나의 배열로 인수들을 전달하고 싶을 때 apply 메서드를 사용하면 좋다.
  
- Example 3-23
: call/apply 메서드의 활용 3-2) 여러 인수를 받는 메서드(Math.max/Math.min)에 apply를 적용.
  example 3-22의 경우 코드가 불필요하게 길지만, Math.max/Math.min를 사용함으로써 훨씬 간단하게 만들었다.
  
- Example 3-24
: 


























