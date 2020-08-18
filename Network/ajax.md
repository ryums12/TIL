# Ajax 

**Ajax, Asynchronous Javascript And Xml**
비동기적 자바스크립트와 Xml. 
브라우저가 가지고 있는 XMLHttpRequest 객체를 이용하여 **전체 페이지를 새로고침 하지 않고도 데이터를 불러 오는**기법이다.  
한 마디로 말하자면 javascript를 사용한 **비동기 통신** 기법이라고 할 수 있다.
특정한 언어가 아닌 하나의 기법인 것이다.

- **javascript**
	- before es6
		```{javascript}
		const xhr = new XMLHttpRequest();
		xhr.open('GET',"localhost:8080")
		xhr.send()
		```
	- es6
		```{javascript}
		fetch('localhost:8080')
			then( res => {
				if(res.status === 200) {
					alert('성공')
				}
			})
			.catch( err => {
				console.log(err)
				alert('실패')
			})
		```

- **jquery**
	```{jquery}
	$.ajax({
    	url: ,
    	type: 'GET',
    	success: function onData (data) {
        	console.log(data);
   		},
    	error: function onError (error) {
        	console.error(error);
    	}
	});
	```