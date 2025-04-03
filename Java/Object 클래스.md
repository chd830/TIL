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

#### 정적 의존관계 vs 동적 의존관계
 