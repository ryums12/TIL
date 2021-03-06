# Entity, Dto, Vo



회사의 업무로 Spring과 mybatis를 사용한 프로젝트를 진행하면서, 동시에 개인적으로 JPA를 공부하기 시작하면서 한 가지 궁금한 것이 생겼다.



**Entity, Dto** 그리고 **Vo**.



비슷하면서도 엄연히 다른 저 세 가지의 차이점은 무엇일까.

어떻게 보면 저 세 개에 대해 자세히 몰라도 프로그래밍을 진행하는 데에는 문제가 없지만, 

그렇게 모른 채로 넘어 갈 경우 그저 시키는 대로만 할 개발자가 될 뿐이기에 한 번 알아보기로 결심했다.  

- **Entity**

​	JPA를 공부하게 되면서 처음 접하게 된 Entity다.

​	Entity는 기본적으로 테이블과 매칭되는 존재며 절대 상속받거나 구현체여서는 안 된다.

​	

​	즉 Member라는 테이블이 id, name, password라는 칼럼을 가지고 있다면, 

​    memberEntity 또한 id, name, password를 속성으로 가져야 한다.



- **Dto**

​	Dto, 이 말을 풀어보자면 Data Transfer Object이다. 

​	즉, 뒤에서 설명할 Vo와 달리 계층간의 이동(Controller, service, db) 등에서 서로 이동할 때 Dto를 사용한다.



- **Vo**

​	Value Object, 글자 그대로 값을 가진 존재이다.

​	Dto와 달리 같은 시스템 내에서만 사용되며, 또 다른 차이점은 가변성인 Dto와 달리 불변성을 가지고 있다.  



