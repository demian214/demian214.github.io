---
layout: post
title: Kotlin Base (1)
subtitle: 개발 환경 세팅 및 변수
categories: Kotlin
tags: Kotlin
---

## 코틀린(Kotlin)

1) 안드로이드(Android) 개발언어

2) 웹 프로그램
   
   - javascript의 대용(Client)
   
   - jsp/servlet의 대용(Server)

프로그램 실행시 내부적으로 코드를 변환해 실행해준다.

*.kt → *.java 

 

## 특징

- 축약된 표현

- 객체지향 언어 + 함수형 언어



## 함수형 언어

함수(간결하게 작성 - 람다식)를 변수처럼

1. 변수에 대입

2. 매개변수로 전달

3. 리턴값으로 사용



## 코틀린과 자바의 문법 차이

### Java 예시 1)

```java
A obj = new A();
obj.setTitle("ABC");
system.out.println(obj.getTitle());
```

### Kotlin 예시 1)

```kotlin
val obj: A = A()
obj.title = "ABC"
println(obj.title)
```

Java 코드와 Kotlin 코드 모두 같은 기능을 하는 코드이지만 위와 같은 문법의 차이를 갖는다.

### Java 예시 2)

```java
class A{
    ...
    public void main(){
        ...
    }
    ...
}
```

### Kotlin 예시 2)

```kotlin
fun m1(){    // Function - 함수의 줄임말로 앞 3글자를 키워드로 지정함
    ...
}
```

Java 코드는 메서드는 항상 클래스 안에서 존재하지만 Kotlin의 함수는 클래스 밖에서 독립되어 존재할 수 있다.

### Java 예시 3)

```java
class Test{
    public static void main(String[] args){
        // 실행코드
    }
```

### Kotlin 예시 3)

```kotlin
fun main(){
    // 실행코드
}

fun m1():리턴값{
    // 실행코드
}
fun main(){    
    val myfun = m1 // → 함수 - 값에 실행코드를 지정한다.
                   //         실행코드의 적재 위치를 저장해서 변수처럼 사용가능하다.
    m1() // → 메서드
}
```
