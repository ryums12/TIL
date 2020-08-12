# Http

Http, Hyper text transfer protocol은 웹 상에서 문서를 주고 받는 프로토콜로써 TCP/UDP 방식을 사용한다.

- **Http Request**

	HTTP 요청과 응답 메시지 구조는 크게 세 가지로 나눌 수 있다. 
	이는 요청과 응답 모두 구조가 동일하다.
	
	- Start Line 
		- HTTP 메소드
			- GET : 리소스 호출
			- HEAD : GET과 비슷하나 Head만 호출
			- POST : 새로운 데이터 전송
			- PUT : 저장된 데이터 전송
			- DELETE : 리소스 삭제
			- OPTIONS, TRACE, CONNECTION etc...
		- 요청 타겟 : 요청이 전송 되는 주소
		- HTTP version
	
	- Header
		글자 그대로 HTTP 요청에 대한 정보를 담고 있으며, Key : Value 형태로 구성.
		- Host : 요청되는 URL 주소
		- User-Agent : 요청을 보내는 클라이언트 정보
		- Accept : 요청이 응답받을 수 있는 body 데이터 타입 정보
		- Connection : 해당 요청이 끝난 후 연결을 지속할 것인지에 대한 정보
		- Connect-Type : body 타입
		- Content-Length : body 총 사이즈
	
	- Body 
		- HTTP 요청에서 전송하는 데이터를 담고 있는 부분
		- 전송하는 데이터가 없을 시 비어 있음
		
	
- **Http Responnse**
	
	- Start Line 
		- HTTP version 
		- Status code : 응답 상태를 나타내는 코드 (ex.200 : 정상 응답)
		- Status message : 상태를 간략히 설명 (ex. ok)
	
	- Header
		- Http Request와 동일 
		- User-Agent 대신 Server 사용
	
	- Body
		- Http Request와 동일
		- 반환된 데이터가 없을 시 비어 있음
	