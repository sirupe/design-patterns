# Decorator 패턴
- 구현방법은 프록시 패턴과 같다.
- 클라이언트가 받는 반환값에 장식을 덧입힌다.
  - proxy pattern : 반환값은 조작하지 않고 제어의 흐름을 컨트롤하기 위한 목적
  - decorator pattern : 반환값에 변경을 가할 목적
  
### POINT
- 데코레이터는 인터페이스를 사용하여 실제 서비스와 같은 이름의 메서드를 구현한다.
- 데코레이터는 실제 서비스에 대한 참조변수를 갖는다.(합성)
- 데코레이터는 실제 서비스의 같은 이름을 가진 메서드를 호출하고 그 반환값에 장식을 더해 클라이언트에게 돌려준다.
- 데코레이터는 실제 서비스의 메서드 호출 전후에 별도의 로직을 수행할 수도 있다.
- 데코레이터 : Decorator 클래스, 인터페이스 : IService 인터페이스, 실제 서비스 : Service 클래스, 같은 이름을 가진 메서드 : runSomething() 메서드

### 결론
- 프록시 패턴과 동일한 구조를 갖기에 동일하게 OCP 와 DIP 가 적용된 설계 패턴이다.