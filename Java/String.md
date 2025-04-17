 참조형
 9버전 이전 - char[]
 9버전 이후 - byte[]
 덧셈이나 초기화시 문자열을 바로 넣는 경우 자주 쓰는 기능이라 포함
String 내부에는 byte(>9version)나 char(<9version) 배열로 이루어져있다
class 이기 때문에 메서드를 제공
속성과 기능을 가짐
참조형
원칙적으로는 + 연산을 사용할 수 없음(Object a + Object b). 
→ 자주 사용하기 때문에 연산 지원
비교는 equals(동등성 비교)를 사용해야 함
```java
String s1 = "hello";
String s2 = "hello";

System.out.println(s1 == s2); // true
System.out.println(s1.equals(s2)) // true

String s3 = new String("hello");
String s4 = new String("hello");

System.out.println(s3 == s4) // false
System.out.println(s3.equals(s4)) // true
```
생성을 리터럴로 한다면 같은 리터럴은 같은 참조값을 가져 == 비교일 때 true가 반환된다
→ 하지만 항상 equals 를 사용하자

#### 속성
char[] 에 보관
영어나 숫자는 1byte 사용. 나머지는 UTF-16 Encoding 을 사용해서 2byte로 사용
→  메모리를 더 효율적으로 사용
#### 기능
length(), charAt(), subString(), indexOf(), toLowerCase(), trim(), concat(),,,

### 불변객체
불변객체이기 때문에 변경이 되었을 경우 새로운 결과를 반환
```java
String str1 = "hello";
String str2 = " java";

str1.concat(str2);
System.out.println(str1); // hello

String str3 = str1.concat(str2);

System.out.println(str3); // hello java
```
문자열 풀을 통해 최적화가 되는데 내부 값이 변경되면 같은 문자열을 풀을 참고하는 변수도 같이 변경되기 때문
사이드 이펙트 방지

