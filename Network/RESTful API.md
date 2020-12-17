# Rest Api 

- **Rest Api 설계 규칙**
  - URL의 마지막에는 슬래쉬(/)를 포함하지 않는다.
    대부분의 웹 컴포넌트는 후행 슬래쉬의 포함 여부에 상관없이  두 개를 동일한 경로로 인식한다.
    그러나 URL의 모든 문자들은 리소스의 고유한 ID로 계산되며, 혼선을 피하기 위해 후행 슬래쉬는 지양해야 한다.

    - Bad case
    	``` get http://api.com/main/ ```
    - Good case
    	``` get http://api.com/main ```

  - 자원 간의 계층 관계를 표현 할 때는 슬래쉬를 사용한다.
    ``` get http://api.com/boards/1 ```

  - 언더바(_) 대신 하이픈(-)을 사용한다
    기본적으로 하이픈의 사용조차 최소한으로 해야 되지만, 긴 단어를 표현해야 할 경우는 하이픈을 사용한다 . 

    - Bad case
    	``` get http://api.com/country_asia ```
    - Good case
    	``` get http://api.com/country-asia ```

  - 모든 경로는  소문자로 작성한다.
  	- Bad case
  		``` get http://api.com/Main ```
  	- Good case
  		``` get http://api.com/main ```
  	
  - 행위는 경로에 포함하지 않는다.

    - Bad case
    	``` get http://api.com/boards/show/1 ```
    - Good case
    	``` get http://api.com/boards/1 ```

  - HTTP Methods

    - GET
    	``` get http://api.com/boards ```
    	해당 컬렉션에 속한 자원 호출
    	``` get http://api.com/boards/1 ```
    	해당 컬랙션의 특정 자원 호출
    - POST
    	``` post http://api.com/boards ```
    	해당 컬렉션의 속한 자원 생성
    	``` post http://api.com/boards/1 ```
    	해당 해당 자원 수정
    - PUT
    	``` put http://api.com/boards/1 ```
    	해당 자원 수정
    - DELETE
    	``` delete http://api.com/boards/1 ```
    	해당 자원 삭제
    	
    	

- 참고
	- https://sas-study.tistory.com/265
	- https://sanghaklee.tistory.com/57
	- https://spoqa.github.io/2012/02/27/rest-introduction.html
