---
title: "Java Stream API: Xử Lý Dữ Liệu Hiện Đại"
date: 2025-10-26T14:30:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - Java
  - Stream API
  - Functional Programming
image: /images/projects/java-stream.png
description: "Hướng dẫn sử dụng Java Stream API để xử lý dữ liệu hiệu quả"
toc: true
---

## Giới thiệu

Stream API là một phần của Java 8, giúp xử lý dữ liệu theo phong cách hàm và bất biến.

## 1. Tạo Stream

```java
List<String> names = Arrays.asList("Thuận", "Nam", "Lan");
Stream<String> stream = names.stream();
```

## 2. Các phép biến đổi dữ liệu

```java
List<String> upperNames = names.stream()
    .map(String::toUpperCase)
    .collect(Collectors.toList());

List<String> filtered = names.stream()
    .filter(name -> name.startsWith("T"))
    .collect(Collectors.toList());
```

## 3. Reduce và Collect

```java
int totalLength = names.stream()
    .map(String::length)
    .reduce(0, Integer::sum);
```

## 4. Parallel Stream

```java
List<Integer> numbers = Arrays.asList(1,2,3,4,5);
numbers.parallelStream()
    .forEach(System.out::println);
```

## Kết luận

Stream API giúp code Java ngắn gọn, dễ đọc và hiệu quả hơn khi xử lý dữ liệu lớn.
