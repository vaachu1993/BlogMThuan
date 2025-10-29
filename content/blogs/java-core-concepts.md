---
title: "Java Core: Những Khái Niệm Nền Tảng"
date: 2025-10-26T10:30:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - Java
  - Programming
  - OOP
image: /images/projects/java-core.png
description: "Tìm hiểu về các khái niệm cốt lõi trong Java và lập trình hướng đối tượng"
toc: true
---

## Giới thiệu về Java

Java là một ngôn ngữ lập trình hướng đối tượng, mạnh mẽ và được sử dụng rộng rãi trong phát triển phần mềm doanh nghiệp.

## 1. Các đặc điểm của Java

- **Hướng đối tượng**: Mọi thứ trong Java đều là đối tượng
- **Độc lập nền tảng**: Write Once, Run Anywhere (WORA)
- **Bảo mật cao**: Chạy trong môi trường máy ảo JVM
- **Đa luồng**: Hỗ trợ lập trình đa luồng

## 2. Lập trình hướng đối tượng trong Java

```java
public class Student {
    private String name;
    private int age;
    
    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
    
    public void study() {
        System.out.println(name + " đang học Java");
    }
}
```

## 3. Collection Framework

Java Collection Framework cung cấp các cấu trúc dữ liệu quan trọng:

- List: ArrayList, LinkedList
- Set: HashSet, TreeSet
- Map: HashMap, TreeMap
- Queue: PriorityQueue

```java
List<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.add("JavaScript");
```

## 4. Exception Handling

Xử lý ngoại lệ trong Java:

```java
try {
    // Code có thể gây ra ngoại lệ
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Không thể chia cho 0");
} finally {
    System.out.println("Luôn được thực thi");
}
```

## Kết luận

Java là một ngôn ngữ mạnh mẽ với nhiều tính năng hữu ích cho phát triển phần mềm quy mô lớn. Việc nắm vững các khái niệm cơ bản sẽ giúp bạn trở thành một lập trình viên Java giỏi.
