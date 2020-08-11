# TCP / UDP


- **TCP**
	TCP, Transmission Control Protocol
	
	- 연결 지향형 프로토콜
	- 서버와 클라이언트는 1대1로 연결
	- 패킷에 대한 응답을 하기에 UDP보다 느림
	- 흐름 제어 및 혼잡 제어
		- 데이터 처리 속도 제어
		- 패킷 수가 넘치지 않게 제어
	- 3-way handshaking 과정을 통해 연결 설정, 4-way handshaking을 통해 해제.
	- 신뢰성 보장
	- 바이트 스트림을 통해 연결
	- HTTP, FTP 등 에서 사용

- **UDP**
	UDP, User Datagram Protocol
	
	- 비연결형 지향형 프로토콜
	- 각각의 패킷은 서로 독립적인 관계를 가짐에 따라 각각 독립적인 경로로 데이터 처리
	- 순서가 보장되지 않는 대신에, TCP보다 빠름
	- 흐름 제어, 혼잡 제어 X
	- 데이터 신뢰성 보장 X
	- 메시지 스트림을 통해 연결
	- 도메인, 스트리밍 등 에서 사용