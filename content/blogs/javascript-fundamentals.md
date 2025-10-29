---
title: "Rich Content"
date: 2021-04-03T19:53:33+05:30
draft: false
author: "Gurusabarish"
tags:
  - Rich content
  - Sample
  - example
image: /images/projects/js-fundamentals.png
description: ""
toc: 
---

## Giới thiệu

JavaScript là một trong những ngôn ngữ lập trình phổ biến nhất thế giới. Trong bài viết này, chúng ta sẽ tìm hiểu về những khái niệm cơ bản nhất của JavaScript.

## 1. Biến và Kiểu dữ liệu

JavaScript có các kiểu dữ liệu cơ bản sau:
- String (chuỗi)
- Number (số)
- Boolean (true/false)
- Object (đối tượng)
- Array (mảng)
- null và undefined

```javascript
let name = "Minh Thuận";    // String
const age = 25;             // Number
let isStudent = true;       // Boolean
let skills = ["JS", "Java"]; // Array
```

## 2. Functions trong JavaScript

Functions là các khối mã có thể tái sử dụng:

```javascript
// Function Declaration
function sayHello(name) {
    return `Xin chào ${name}!`;
}

// Arrow Function
const add = (a, b) => a + b;
```

## 3. Objects và Methods

Objects là cấu trúc dữ liệu quan trọng trong JavaScript:

```javascript
const person = {
    name: "Minh Thuận",
    age: 25,
    sayHi() {
        console.log("Xin chào!");
    }
};
```

## 4. Arrays và Array Methods

JavaScript cung cấp nhiều phương thức xử lý mảng hữu ích:

```javascript
const numbers = [1, 2, 3, 4, 5];

// Map
const doubled = numbers.map(num => num * 2);

// Filter
const evenNumbers = numbers.filter(num => num % 2 === 0);

// Reduce
const sum = numbers.reduce((acc, curr) => acc + curr, 0);
```

## Kết luận

JavaScript là một ngôn ngữ đa năng với cú pháp dễ học. Việc nắm vững các khái niệm cơ bản sẽ giúp bạn có nền tảng vững chắc để phát triển các ứng dụng web phức tạp hơn.
