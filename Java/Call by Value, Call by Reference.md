# Call by Value, Call by Reference


- **정의**
	- Call by Value, 메모리에 저장되어 있는 값을 넘겨주는 호출 방식
	- Call by Reference, 값이 저장되어 있는 주소를 넘겨주는 호출 방식
	- C언어에서 등장

- **자바에선**
	```{java}
	public static void main(String[] args) {
		int a = 1;
		int b = 2;
		swap(a, b);

		System.out.println(a);
		System.out.println(b);
	}

	static void swap(int a, int b) {
		int tmp = a;
		a = b;
		b = tmp;
	}
	```
	
	위 코드는 C에서 Call by 개념을 배울 때 가장 흔하게 사용되는 예제인
	두 숫자의 메소도를 자바로 구현한 것이다.
	
	얼핏 보기에는 main의 a와 b의 값이 서로 바뀌어 출력 되는 것으로 생각할 수 있겠지만 결과는 똑같이 나온다.
	
	main에서 선언된 a와 b는 메모리의 A번 주소와 B번 주소에 할당 되었다.
	그리고 swap 메소드에서 선언된 a와 b는 A번 주소와 B번 주소에 있는 값만을 가져와
	C번 주소와 D번 주소에 저자된다.
	
	즉 기존의 A번 주소와 B번 주소 자체가 아닌 값만을 호출해 저장했기 때문에
	기존의 값는 변동이 없는 것이다. 이것이 Call By Value라고 할 수 있다.
	
	그렇다면 자바는 Call By Value 형식을 따르는가 하면 그것 또한 아니다.
	
	```{java}
	class MyClass{
		int index;

		public MyClass(int index) {
			this.index = index;
		}

		public int getIndex() {
			return index;
		}

		public void setIndex(int index) {
			this.index = index;
		}
	}
	```
	위와 같이 임의의 int값에 대한 getter/setter 메소드를 가지는 클래스를 선언한 후
	최초 생성한 값에 대한 setter를 호출한다면 해당 클래스의 int 값은 변경된다.
	이는 Call By Reference 방식을 따른다고 볼 수 있다.
	
	결론적으로 c와 달리 자바는 사용 방식에 따라 호출 방식이 변경된다고 볼 수 있기에 자바에서는 호출 방식이 그렇게 중요하지는 않은 것 같다.
	
	

**출처 : https://siyoon210.tistory.com/104**