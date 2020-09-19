# Optional

- **정의**
	- Optional은 null을 대신하기 위해 만든 데이터 타입으로서, null이나 null이 아닌 다른 값을 담을 수 있다. 즉 가장 흔한 오류인 NPE를 해결할 수 있다는 뜻이다.
	- 자바에서는 JDK 8 버젼에서 최초 등장

- **Optional 객체**
	- Optional,emtpy() : 빈 Optional 객체 생성
	- Optional.of(value) : value값이 null이 아닌 경우 value값 사용, value값의 null일 경우 NPE 발생
	- Optional.ofNullalbe() : value값이 null인지 아닌지 확실하지 않은 경우에 사용, value가 null 일 경우 빈 Optional 객체를 생성함으로써 NPE를 피할 수 있음

**[참고 자료](https://advenoh.tistory.com/15)**