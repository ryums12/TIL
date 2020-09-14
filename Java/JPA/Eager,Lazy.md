# Eager loading, Lazy loading

두 개의 엔티티가 서로 1:N, N:1의 관계를 맺고 있을 때, 
엔티티에 fetch type 옵션을 설정할 경우 실행되는 jpa query의 형태가 변화한다.

- **Eager loading**
	- 즉시 로딩, fetch type을 EAGER로 설정 시 적용
	- 쿼리 호출 시 연관된 엔티티를 동시에 호출함
	- @ManyToOne, @OneToOne 등의 X : 1의 관계를 설정하는 어노테이션들은 기본 타입이 EAGER
	- 따라서 서로 관계를 맺은 엔티티에서 하나의 엔티티의 데이터를 필요로 할 경우, Eager loading 을 쓰는 것을 비효율적

- **Lazy loading**
	- 지연 로딩, fetch type을 lazy로 설정 시 적용
	- 엔티티 조회 시에는 해당 엔티티의 데이터만을 호출, 관계된 엔티티는 사용자가 호출하고자 할 때 호출됨
	- @OneToMany와 @ManyToMany는 기본이 Lazy
	- fetch join을 사용 시 각각의 엔티티에 대해 두 번의 쿼리를 호출하는 문제점을 대체 가능



