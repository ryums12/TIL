# 콜백 (callback) 함수


- **콜백 (callback) 함수란?**
	콜백 (callback) 함수란, 글자 그대로 미리 정의한 함수를 특정한 시점에 호출하는 것이다.
	즉, 문법적인 구분이 아닌 사용 방법의 구분이라고 볼 수 있다. 
	보통의 경우 함수의 매개변수로 전달하여 특정 시점에서 호출되는 방식으로 사용한다.
	```{javascript}
	function plus(a, b, fnc) {
		const result = a + b;
		fnc(result);
	}
	
	plus(1, 2, (result) => {
		console.log(result);
	});
	```
	
	*이런 식으로 사용하는 것이 콜백.*  
	
	이 외에도 대표적인 예시로 html의 onclick 속성을 통해 함수를 호출할 경우, 이 또한 콜백이라고 볼 수 있다.
	
- **왜?**
	가장 큰 이유는 **비동기적** 프로그래밍을 위한 것이다.
	만일 어떤 동작이 끝나고 함수를 호출하는 것이라면 순차적으로 실행해도 되지 않냐고 생각할수 있겠지만, 만일 순차적으로 실행된 함수에서 처리가 오래 걸릴 경우 이는 자바스크립트 전체의 실행 중단으로 이어지는 문제가 발생할 수 있다.  
	
	```{javascript}
	function plus(a,b) {
		return a + b;
	}
	
	function print(result) {
		console.log(result);
	}
	
	print(plus(a, b));
	```
	
	예시로 든 코드는 되게 간단한 로직으로 구성되어있지만, 만일 예제의 plus 부분이 되게 복잡한 로직일 경우 plus 를 완료하는 동안 자바스크립트 전체가 중단되어 버리는 상황이 발생한다.
	
	```{javascript}
	function plus(a, b, fnc) {
		const result = a + b;
		fnc(result);
	}
	```
	
	맨 처음의 예시처럼 콜백 방식을 사용할 경우, 필요할 경우에만 plus 를 호출하면 되는 것이기에 자바스크립트 전체의 중단을 염려할 필요가 없어진다.
	