# IoC (Inversion of Control)

한글로 번역하면 제어의 역전.  
인스턴스의 생상과 소멸 등을 개발자가 아닌 외부,  즉 컨테이너에서 담당한다는 뜻이다.

- **IoC 컨테이너**
	IoC 컨테이너라 불리우는 존재는 bean 들을 인스턴스화하고 조합하여 관리하는 역할을 한다.   이 때 여기서 관리되는 bean 들은 [의존성 주입](https://github.com/ryums12/TIL/blob/master/%EC%9D%98%EC%A1%B4%EC%84%B1%20%EC%A3%BC%EC%9E%85(DI).md) 을 통해 IoC를 지원한다.
	
	이 컨테이너의 존재로 인해 제어권이 역전 될 경우  객체의 생성부터 생명 주기까지의 관한 모든 제어권이 개발자의 손을 떠나며, 컨테이너에 의해 관리된다.
	이는 적절한 설정이 되어 있다면, 프로그래머 본인의 호출 없이도 직접 코드를 참조하여 객체의 생성과 관리를 할 수 있게 된다는 것을 의미한다., 
  
- **Bean(s)**
	스프링 IoC 컨테이너에 의해 생성 되가나 관리되는 객체들을 말한다.
	Bean Factory, 혹은 Application Context에 의해 관리된다.
	
- **Bean Factory**
	Bean(s)를 생성하고 관리하는 컨테이너.
	팩토리 디자인 패턴을 구현했으며, 빈의 정의는 즉시 로딩하지만 빈 자체가 필요해지기 전까지는 인스턴스화 하지 않는다.
	보통의 경우, Bean Factroy보단 Application Context를 사용한다.

- **Application Context**
	Bean Factory를 상속한 것으로, 기본적으로는 Bean Factory와 같은 기능을 가지고 있지만 그 외에 좀 더 많은 기능을 제공한다. 이것이 Bean Factory 대신 Application Context를 사용하는 이유다.
	- 추가로 제공하는 기능등
		- 국제화가 지원되는 텍스트 메시지 지원
		- 파일 자원을 로드할 수 있는 방법 지원
		- 리스너를 통해 등록된 빈에게 이벤트 발생 전달


**추후 추가 필요**

