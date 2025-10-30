---
title: "Giới Thiệu Node.js: JavaScript trên Server"
date: 2025-10-26T15:00:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - Rich content
  - Node.js
  - Backend
image: /images/anhnodejs.jpg
description: "Khám phá Node.js và cách xây dựng ứng dụng backend với JavaScript"
toc: true
---

## Node.js là gì?

Node.js là môi trường chạy JavaScript phía server, giúp xây dựng các ứng dụng backend hiệu quả.

## 1. Tạo server đơn giản với Node.js

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Xin chào từ Node.js!');
});

server.listen(3000, () => {
  console.log('Server đang chạy tại http://localhost:3000');
});
```

## 2. Quản lý package với npm

```shell
npm init -y
npm install express
```

## 3. Express.js: Framework phổ biến

```javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello Express!');
});

app.listen(3000);
```

## Kết luận

Node.js mở ra cơ hội phát triển ứng dụng web toàn diện với JavaScript, từ frontend đến backend.
