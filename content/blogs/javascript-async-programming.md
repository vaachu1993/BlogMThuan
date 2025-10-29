---
title: "Lập Trình Bất Đồng Bộ Trong JavaScript"
date: 2025-10-26T12:00:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - JavaScript
  - Async
  - Programming
image: /images/projects/async-js.png
description: "Tìm hiểu về lập trình bất đồng bộ trong JavaScript với Promises, Async/Await"
toc: true
---

## Giới thiệu

Lập trình bất đồng bộ là một phần quan trọng trong JavaScript, đặc biệt là trong phát triển web hiện đại.

## 1. Callbacks

```javascript
function fetchData(callback) {
    setTimeout(() => {
        const data = { id: 1, name: 'JavaScript' };
        callback(data);
    }, 1000);
}

fetchData(data => {
    console.log(data);
});
```

## 2. Promises

```javascript
const fetchUser = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            const user = { id: 1, name: 'Thuận' };
            resolve(user);
            // reject(new Error('Không thể tải dữ liệu'));
        }, 1000);
    });
};

fetchUser()
    .then(user => console.log(user))
    .catch(error => console.error(error));
```

## 3. Async/Await

```javascript
async function getUserData() {
    try {
        const user = await fetchUser();
        const posts = await fetchUserPosts(user.id);
        return { user, posts };
    } catch (error) {
        console.error('Lỗi:', error);
    }
}
```

## 4. Promise.all và Promise.race

```javascript
const promise1 = fetch('/api/users');
const promise2 = fetch('/api/posts');

// Đợi tất cả promises hoàn thành
Promise.all([promise1, promise2])
    .then(([users, posts]) => {
        console.log(users, posts);
    });

// Lấy kết quả của promise nhanh nhất
Promise.race([promise1, promise2])
    .then(result => {
        console.log('Kết quả đầu tiên:', result);
    });
```

## Kết luận

Lập trình bất đồng bộ là kỹ năng thiết yếu cho mọi lập trình viên JavaScript. Việc sử dụng đúng các pattern này sẽ giúp ứng dụng của bạn hoạt động hiệu quả và mượt mà hơn.
