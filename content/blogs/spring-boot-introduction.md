---
title: "Spring Boot: Framework Java Hiện Đại"
date: 2025-10-26T11:30:00+07:00
draft: false
author: "Minh Thuận"
tags:
  - Java
  - Spring Boot
  - Web Development
image: /images/projects/spring-boot.png
description: "Tìm hiểu về Spring Boot và cách xây dựng ứng dụng web với Java"
toc: true
---

## Giới thiệu Spring Boot

Spring Boot là một framework giúp đơn giản hóa việc phát triển ứng dụng Spring. Nó cung cấp nhiều tính năng "out of the box" và cấu hình tự động.

## 1. Cấu trúc cơ bản

```java
@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

## 2. REST Controllers

```java
@RestController
@RequestMapping("/api")
public class UserController {
    @GetMapping("/users")
    public List<User> getUsers() {
        return userService.findAll();
    }
    
    @PostMapping("/users")
    public User createUser(@RequestBody User user) {
        return userService.save(user);
    }
}
```

## 3. JPA Repositories

```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
    private String email;
}

@Repository
public interface UserRepository extends JpaRepository<User, Long> {
    List<User> findByEmail(String email);
}
```

## 4. Spring Security

```java
@Configuration
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http.authorizeRequests()
            .antMatchers("/api/public/**").permitAll()
            .antMatchers("/api/private/**").authenticated()
            .and()
            .csrf().disable()
            .oauth2ResourceServer().jwt();
    }
}
```

## Kết luận

Spring Boot đã trở thành một trong những framework phổ biến nhất cho phát triển ứng dụng Java. Với các tính năng mạnh mẽ và cộng đồng lớn, Spring Boot là lựa chọn tuyệt vời cho các dự án enterprise.
