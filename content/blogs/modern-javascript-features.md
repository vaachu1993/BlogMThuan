---
title: "Modern JavaScript: ES6+ Features"
date: 2025-10-26T11:00:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - JavaScript
  - ES6
  - Web Development
image: /images/projects/modern-js.png
description: "Khám phá những tính năng hiện đại của JavaScript ES6+ và cách áp dụng chúng"
toc: true
---

## Giới thiệu

ES6 (ECMAScript 2015) và các phiên bản sau đã mang đến nhiều tính năng mạnh mẽ cho JavaScript. Hãy cùng khám phá những tính năng quan trọng nhất.

## 1. Arrow Functions

```javascript
// Cách viết truyền thống
function add(a, b) {
    return a + b;
}

// Arrow function
const add = (a, b) => a + b;

// Arrow function với object
const createPerson = (name, age) => ({ name, age });
```

## 2. Destructuring

```javascript
// Array destructuring
const [first, second, ...rest] = [1, 2, 3, 4, 5];

// Object destructuring
const person = { name: 'Thuận', age: 25 };
const { name, age } = person;
```

## 3. Template Literals

```javascript
const name = 'Thuận';
const greeting = `Xin chào ${name}!
Chúc một ngày tốt lành!`;
```

## 4. Async/Await

```javascript
async function fetchData() {
    try {
        const response = await fetch('https://api.example.com/data');
        const data = await response.json();
        return data;
    } catch (error) {
        console.error('Lỗi:', error);
    }
}
```

## 5. Modules

```javascript
// math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;

// main.js
import { add, subtract } from './math.js';
```

## Kết luận

Các tính năng hiện đại của JavaScript giúp code trở nên sạch sẽ và dễ bảo trì hơn. Việc sử dụng thành thạo các tính năng này sẽ giúp bạn trở thành một lập trình viên JavaScript chuyên nghiệp.
