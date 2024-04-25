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
: 객체 복사. 하나의 객체(b)가 값을 가진 객체(a)를 copy할 경우 객체(a)가 가르키는 주소를 동일하게 가르킨다.

- Example 1-8
: 객체 복사 이후 객체의 **프로퍼티**를 변경할 경우 저장되어 있던 기존의 data가 바뀐다. 

- Example 1-9
: 객체 복사 이후 객체 자체를 변경할 경우 기존의 data는 변하지 않고 새로운 data가 메모리에 할당되어 객체와 연결된다.

- Example 1-10
: 객체의 가변성에 따른 문제점을 보여준다. 정보가 바뀐 시점을 알고 싶을 경우, 변경 전과 후에 객체가 서로 다른 객체를 가르키도록 만들어야한다.

- Example 1-11
: Example 1-10의 문제점의 해결 방법이다. 새로운 object를 만들고, 그 주소를 return 하여 두 객체가 서로 다른 객체를 보도록 만들었다.

- Example 1-12
: 기존 정보를 복사하여 새로운 객체를 반환하는 것을 얕은 함수라 부른다. result가 target의 정보를 복사하고 있다.






















