# IoC (Inversion of Control)

한글로 번역하면 제어의 역전.  
인스턴스의 생상과 소멸 등을 개발자가 아닌 외부,  즉 컨테이너에서 담당한다는 뜻이다.


- **IoC 컨테이너**
	IoC 컨테이너라 불리우는 존재는 bean 들을 인스턴스화하고 조합하여 관리하는 역할을 한다.   이 때 여기서 관리되는 bean 들은 [의존성 주입]([https://github.com/ryums12/TIL/blob/master/%EC%9D%98%EC%A1%B4%EC%84%B1%20%EC%A3%BC%EC%9E%85(DI).md](https://github.com/ryums12/TIL/blob/master/의존성 주입(DI).md) 을 통해 IoC를 지원한다.
	
	이 컨테이너의 존재로 인해 제어권이 역전 될 경우  객체의 생성부터 생명 주기까지의 관한 모든 제어권이 개발자의 손을 떠나며, 사용자의 호출에 따라 작동되는 컨테이너에 의해 관리된다.
  


**추후 추가 필요**

