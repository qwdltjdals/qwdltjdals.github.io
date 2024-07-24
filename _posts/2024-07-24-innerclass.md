---
layout: single
title:  "내부 클래스"
categories : 코딩
tag : [스프링부트, Di, IoC]
---

# 내부클래스
```Java
public class A {
    public class A2
}
```
    선언 하려면?
```Java 
A a = new A();
A.A2 a2 = new a.A2();
```
a를 생성해야 a2를 만들 수 있음
a2 생성하려고 맨날 a를 생성할래???
    -  불편해   -
```Java
A.A2 a2 = new (newA()),A2(); ???
```

개선
```Java
public class A {
    public static class A2 {

    }
}
```
static 활용
```Java
A.A2 a2 = new A.A2();
```

하나의 Class파일 안에 여러개를 넣을 수 있음
