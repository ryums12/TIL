# Binding


- **Arrow funtion**
	ES5와 ES6의 가장 큰 문법적 차이는 Arrow function의 차이라고 볼 수 있다.
	```{javascript}
	var arr = [1, 2, 3,];
	var pow = arr.map(function (x) {
		return x * x;
	});
	```
	*ES5*
	
	```{javascript}
	const arr = [1, 2, 3,];
	const pow = arr.map( x => x * x; );
	```
	*ES6*
	
	이 두 개의 차이는 단순히 문법 차이뿐만 아니라 this에서도 존재한다.
	
- **this**
	자바스크립트의 경우, 함수의 호출 방식에 따라 this에 바인딩할 객체가 정해진다.
	다시 말하자면 함수를 선언할 때 정적으로 this가 정해지는 것이 아닌, 함수를 호추할 때 해당 함수가 어떻게 선언되었는지에 따라 동적으로 정해진다는 것이다.
	
	예를 들어 callback 함수 내부의 this는 해당 함수가 아닌 전역 객체 window를 참조한다. 
	
	```{javascript}
	function Person() {
		this.age = 0;

		setInterval(function growUp() {
			this.age++; // 이것은 age를 참조하지 않음
		}, 1000);
	}
	```
	
	그러나 ES6의 Arrow function을 사용한다면 해당 this값을 바인딩하는 것이 가능해진다.
	
	```{javascript}
	function Person() {
		this.age = 0;

		setInterval( () => {
			this.age++; // age 참조
		}, 1000);
	}
	```
	
	혹은 .bind(this)를 활용한 방법도 가능하다.
	
	```{javascript}
	function Person() {
		this.age = 0;

		setInterval(function growUp() {
			this.age++; // age 참조
		}.bind(this), 1000);
	}
	```