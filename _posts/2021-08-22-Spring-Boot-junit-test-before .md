---
layout: post
title: "Spring Boot junit 5 어노테이션 정리"
subtitle: "Spring Boot 공부 기록"
categories: [server]
tags: [Spring Boot, server]
date: 2021-08-22 08:00:00
background: '/img/13.jpg'
---

## Spring Boot junit 5에 쓰이는 어노테이션들 정리 

#### 1. @BeforeAll 
 
 테스트가 실행될때 가장 처음 실행 (@BeforeEach보다 먼저 실행 됨)


#### 2. @BeforeEach
 
 각 테스트 메소드가 실행될때 실행됨


#### 3. @AfterAll
    
 모든 테스트가 끝나고 실행 (@AfterEach보다 늦게 실행 됨)


#### 4. @AfterEach

 각 테스트 메소드가 끝나고 실행됨


#### 5. @Disabled
 
 해당 어노테이션이 붙은 메소드는 실행에 빠짐


#### 6. @DisplayName
    
 클래스 또는 메소드에 붙어 테스트 이름을 지정해줄수 있음 


#### 7. @SpringBootTest
    
 클래스에 붙는 통합 테스트 어노테이션, 모든 빈을 가져오므로 막 붙여서는 안된다.


#### 8. @WebMvcTest
 
 컨트롤러 테스트 어노테이션, 웹의 요청 응답 테스트에 필요한 빈을 가져온다.   
 속성 controllers= 클래스, MockMvc를 가져와 다음과 같이 사용
 ``` java
     @Autowired
        private MockMvc mockMvc;
     
     @Test
     void helloWorld() throws Exception{
        mockMvc.perform(MockMvcRequestBuilders.get("/api/hello"))
                .andDo(print())
                .andExpect(status().isOk())
                .andExpect(content().string("hello-world"));
     }
 ```


[맨위로👆](#){: .btn .btn--primary }
