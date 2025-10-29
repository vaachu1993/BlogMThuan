---
title: "Lập Trình Mạng với Java"
date: 2025-10-26T13:30:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - Java
  - Network Programming
  - Socket
image: /images/projects/java-network.png
description: "Giới thiệu về lập trình mạng và socket trong Java"
toc: true
---

## Giới thiệu

Lập trình mạng là lĩnh vực quan trọng trong phát triển phần mềm. Java cung cấp các API mạnh mẽ để xây dựng ứng dụng mạng.

## 1. Socket Programming

```java
// Server
ServerSocket serverSocket = new ServerSocket(8080);
Socket clientSocket = serverSocket.accept();

// Client
Socket socket = new Socket("localhost", 8080);
```

## 2. Đọc/Ghi dữ liệu qua mạng

```java
BufferedReader in = new BufferedReader(new InputStreamReader(socket.getInputStream()));
PrintWriter out = new PrintWriter(socket.getOutputStream(), true);

String request = in.readLine();
out.println("Phản hồi từ server");
```

## 3. UDP Socket

```java
DatagramSocket socket = new DatagramSocket();
byte[] buf = "Hello".getBytes();
DatagramPacket packet = new DatagramPacket(buf, buf.length, InetAddress.getByName("localhost"), 8080);
socket.send(packet);
```

## Kết luận

Lập trình mạng với Java giúp bạn xây dựng các ứng dụng giao tiếp qua Internet, từ chat, truyền file đến các hệ thống phân tán.
