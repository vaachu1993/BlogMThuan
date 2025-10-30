---
title: "Giới Thiệu React.js cho Lập Trình Viên JavaScript"
date: 2025-10-26T14:00:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - JavaScript
  - React
  - Frontend
image: /images/anhreactjs.jpg
description: "Tìm hiểu về React.js và cách xây dựng giao diện web hiện đại"
toc: true
---

## React là gì?

React là thư viện JavaScript nổi tiếng dùng để xây dựng giao diện người dùng (UI) cho ứng dụng web.

## 1. Component trong React

```javascript
function Welcome(props) {
  return <h1>Xin chào, {props.name}!</h1>;
}
```

## 2. State và Props

```javascript
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>Bạn đã nhấn {count} lần</p>
      <button onClick={() => setCount(count + 1)}>Nhấn</button>
    </div>
  );
}
```

## 3. Lifecycle Methods

```javascript
useEffect(() => {
  // Chạy khi component mount
  console.log('Component đã render');
}, []);
```

## Kết luận

React giúp phát triển giao diện web nhanh chóng, dễ bảo trì và mở rộng. Hãy thử xây dựng một ứng dụng nhỏ với React để trải nghiệm sức mạnh của nó!
