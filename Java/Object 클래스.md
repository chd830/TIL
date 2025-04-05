### 다형성
상속을 따로 선언하지 않는 객체의 경우 Object 를 기본으로 상속
-> 모든 객체를 상속할 수 있음
##### 다운캐스팅
```java
if(obj instsance of Dog dog) {
 dog.sound();
}
```
 obj 를 Dog의 dog로 자동 다운캐스팅
#### toString
Object 에서 기본적으로 제공
```java

System.out.println(obj);
System.out.println(obj.toString()); // 기본적으로 제공되기 때문에 toString을 입력할 필요X
println(Object obj) {
	return object.getClassName()+"@"+System.identityHashCode(obj);
}
```

#### 객체의 참조값
```java
System.identityHashCode(object);
System.out.println(Integer.toHexString(System.identityHashCode(object)));
```

## equals()
##### Identity(동일성)
완전히 같음을 의미
== 연산자를 사용해서 두 객체의 참조가 동일한 객체를 가리키고 있는지 확인
##### Equality(동등성)
같은 가치나 수준을 의미하지만 형태나 외관이 같이 않음
equals() 메서드를 사용하여 두 객체가 논리적으로 동등한지 확인

##### equals()
반사성(Reflexivity): 객체는 자기 자신과 동등
대칭성(Symmetry): 두 객체가 서로 동일하다고 판단되면 양방향으로 동일
추이성:(Transitivity) 한 객체가 두번째 객체가 동일하고, 두번째 객체와 동일하면 첫번째 객체는 세번째 객체와 동일
일관성(Constency): 두 객체의 상태가 변경되지 않는 한 equals() 메소드는 항상 동일한 값 반환
null에 대한 비교: 모든 객체는 null과 비교했을 때 반환