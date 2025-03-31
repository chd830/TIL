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
#### 객체의 참조값
```java
System.identityHashCode(object);
System.out.println(Integer.toHexString(System.identityHashCode(object)));
```