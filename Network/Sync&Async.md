# Synchronous & Asynchronous

![동기 비동기](https://t1.daumcdn.net/cfile/tistory/998750415BCB139209)

- **Synchronous (동기 통신)**
	동기식 통신, 글자 그대로 동시에 통신한다.
	
	Request를 보내면 시간이 얼마나 걸리든지 간에 Response를 받기 전까지 Block 상태에 있다.
	
	장점으로는 요청과 응답값 순서와 Request의 결과값을 보장 받기 때문에 결과에 따라 다른 처리를 해야만 하는 동작에서 사용한다.
	
	단점으로는 Request에 대한 Response의 응답이 오래 걸릴 경우, 해당 Thread는 계속 Block 상태에 있기 때문에 다른 작업을 진행할 수 없다.
	
- **Asynchronous (비동기 통신)**
	비동기식 통신, 글자 그대로 동시에 통신하지 않는다.
	
	동기 통신과 달리, 하나의 Request를 보낸 후 Response를 받지 않아도 또 다른 작업을 진행 할 수 있다.
	즉, 하나의 Request를 보낸 후 Thread가 Block 상태가 되지 않는다.
	
	동기 통신과 달리 여러 개의 서비스를 순차적으로 기다리지 않고 진행 할 수 있지만,
	동시에 Response값을 필수로 하는 서비스에서 비동기 통신을 사용할 경우, 해당 Response 값을 보장받지 못하기에 불안 요소가 있다.