# Singleton Pattern
- 인스턴스를 하나만 만들어 사용하기 위한 패턴
- 오직 인스턴스 하나만 만들고 그것을 계속해서 재사용 한다.
- 필요한 요소
  - new를 실행하지 못하도록 한다 -> 생성자를 private 으로 지정.
  - 단일 객체를 반환할 수 있는 정적 메서드 필요
  - 단일 객체를 참조할 수 있는 정적 참조변수 필요
- 단일객체의 경우 결국 공유객체로 사용되기에 속성을 가지지 않게 하는 것이 정석이다. -> 전역/공유 변수를 가능한 한 사용하지 말자
- 읽기 전용 속성을 갖는 것은 문제되지 않는다.
- 단일 객체가 다른 단일 객체에 대한 참조를 속성으로 가진 것 또한 문제되지 않는다.
- 이는 스프링 싱글턴 빈이 가져야 할 제약조건이다.

### 특징
- private 생성자
- 단일 객체 참조 변수를 정적 속성으로 갖는다.
- 단일 객체 참조 변수가 참조하는 단일 객체를 반환하는 getInstance() 정적 메서드를 갖는다.
- 단일 객체는 쓰기 가능한 속성을 갖지 않는 것이 정석이다.

### 요약
- 클래스의 인스턴스, 즉 객체를 하나만 만들어 사용하는 패턴