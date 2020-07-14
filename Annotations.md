# Annotations

- **@NoArgsConstructor, @AllArgsConstructor**  
	각각 아무것도 받지 않는 기본 생성자와, 모든 필드값을 받는 생성자를 생성한다
	

	* @NoArgsConstructor는 다음과 같다  
		```{java}
		public class test() {
		
			private String test;
			private String test2;
	    
			public test() {
			
			}
		    
		}
		```
		
	* @AllArgsConstructor는 다음과 같다
		```{java}
		public class test() {
		
			private String test;
			private String test2;
	    
			public test(String test, String test2) {
				this.test = test;
				this.test2 = test2;
			}
		    
		```
	
- **@CreatedDate**  
	Entity가 생성되어 저장 될 때의 시간이 저장된다. MySql의 NOW()와 비슷하다고 생각하면 될 듯 하다.  
	비슷한 기능을 하는 것으로 @LastModifiedDate가 있다. Entity가 수정 될 때의 시간을 저장한다.
	
	```{java}
	public class TimeEntity() {
		
		@CreatedDate
		private LocaleDateTime regDt;
		
		@LastModifiedDate
		private LocaleDateTime chgDt;
	    
	}
	```

