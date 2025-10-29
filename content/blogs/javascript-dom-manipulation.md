---
title: "DOM Manipulation với JavaScript"
date: 2025-10-26T13:00:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - JavaScript
  - DOM
  - Web Development
image: /images/projects/js-dom.png
description: "Hướng dẫn thao tác DOM bằng JavaScript cho người mới bắt đầu"
toc: true
---

## DOM là gì?

DOM (Document Object Model) là mô hình dữ liệu dạng cây đại diện cho cấu trúc của trang web. JavaScript có thể dùng DOM để thay đổi nội dung, thuộc tính, và sự kiện trên trang.

## 1. Truy cập phần tử DOM

```javascript
const heading = document.getElementById('main-title');
const items = document.querySelectorAll('.item');
```

## 2. Thay đổi nội dung và thuộc tính

```javascript
heading.textContent = 'Chào mừng đến với Blog!';
heading.style.color = 'blue';
```

## 3. Thêm/Xóa phần tử

```javascript
const newItem = document.createElement('li');
newItem.textContent = 'Item mới';
document.querySelector('ul').appendChild(newItem);
```

## 4. Xử lý sự kiện

```javascript
document.getElementById('btn').addEventListener('click', function() {
    alert('Bạn vừa nhấn nút!');
});
```

## Kết luận

Thao tác DOM là kỹ năng quan trọng giúp bạn xây dựng các trang web tương tác và động với JavaScript.
