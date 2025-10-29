---
title: "Java Multithreading"
date: 2025-10-26T11:45:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - Java
  - Multithreading
  - Concurrency
image: /images/projects/java-multithreading.png
description: "Giới thiệu về đa luồng trong Java và các kỹ thuật lập trình đồng thời"
toc: true
---

## Giới thiệu

Lập trình đa luồng là một trong những tính năng mạnh mẽ của Java, cho phép thực thi nhiều tác vụ đồng thời.

## 1. Tạo và Quản lý Thread

```java
// Cách 1: Kế thừa Thread
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread đang chạy");
    }
}

// Cách 2: Implements Runnable
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable đang chạy");
    }
}

// Sử dụng
MyThread thread1 = new MyThread();
thread1.start();

Thread thread2 = new Thread(new MyRunnable());
thread2.start();
```

## 2. Synchronization

```java
public class Counter {
    private int count = 0;
    
    public synchronized void increment() {
        count++;
    }
    
    public synchronized int getCount() {
        return count;
    }
}

// Sử dụng synchronized block
public void method() {
    synchronized(this) {
        // Critical section
    }
}
```

## 3. ExecutorService

```java
ExecutorService executor = Executors.newFixedThreadPool(5);

Future<String> future = executor.submit(() -> {
    Thread.sleep(1000);
    return "Kết quả từ thread";
});

String result = future.get(); // Đợi và lấy kết quả
executor.shutdown();
```

## 4. Thread Pools và CompletableFuture

```java
CompletableFuture<String> future1 = CompletableFuture
    .supplyAsync(() -> "Hello")
    .thenApply(s -> s + " World")
    .thenApply(String::toUpperCase);

CompletableFuture<Void> future2 = CompletableFuture
    .runAsync(() -> {
        // Thực thi bất đồng bộ
    });
```

## Kết luận

Lập trình đa luồng trong Java là một công cụ mạnh mẽ nhưng cần được sử dụng cẩn thận. Việc hiểu và áp dụng đúng các pattern đa luồng sẽ giúp ứng dụng của bạn hoạt động hiệu quả và ổn định.
