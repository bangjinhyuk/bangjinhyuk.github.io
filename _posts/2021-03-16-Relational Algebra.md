---
layout: post
title: "Relational Algebra"
subtitle: "아주대학교 데이터 베이스 수업."
categories: [Database]
tags: [Ajou]
date: 2021-03-16 08:00:00
background: '/img/8.jpg'
---

# Database
* 헷갈리는거 행 - Row- 가로 /  열 - Column - 세로

#### Relational Algebra 쿼리들

1. relation name =>  순수 테이블 이름도 쿼리이다.

2. Select operator 
    + 한테이블 내에서 튜플들을 찾는 쿼리
    + 예시 =>
            <img src="/img/algebra_select.jpeg"  width="400" height="370">
        + r 테이블에서 A = B 이고 D > 5인 튜플을 찾아라

3. Project operator
    + 열을 찾는 쿼리
    + 중복된 행이 있으면 제거 <중요 no duplicate>
    + 예시 =>
            <img src="/img/algebra_project.jpeg"  width="400" height="370">
        + r 테이블에서 A와 C속성을 추출해라
    
4. Select+Project 혼합 연산
    + Select 먼저 한뒤에 Project
    + 예시 =>
        <img src="/img/algebra_select_project.gif"  width="400" height="40">
        + Employee 테이블(relation)안에 EmpNo = 2106 인 Rows 중에서 EmpName, Title Columns를 보여줘라 
5. Cross-product (cartesian product) 
    + 두 테이블을 합치는것
    + 두 데이블의 tuple 개수의 곱만큼 tuple 이 생성 m*n
    + 예시 =>
        <img src="/img/algebra_cross_product.jpeg"  width="400" height="370">
        + 릴레이션 r과 s를 크로스 프로덕트해라.     
    + 예시 =>
        <img src="/img/algebra_cross_product_2.jpg"  width="400" height="370">
        +  크로스 프로덕트한 릴레이션에서 속성 A와 C가 같은 튜플을 선택해라.
        
6. Natural Join 
    + 두개의 relations
    + 같은 이름의 attribute가 존재해야 한다. 
    + 중복된 attributes는 제거 
    + Cross-product에 같은 속성의 같은 값을 찾는 조건을 추가한것과 같음(밑에 예시 보기)
    + 예시 =>
        <img src="/img/algebra_natural_join.png"  width="400" height="370">
        
7. Theta Join
    + cross product를 수행하고, selection을 수행한다.
    + Natural join은 Theta join의 특별한 한 예이다.
    + 수식 =>
        <img src="/img/algebra_theta_join.png"  width="400" height="40">
        
### 요약
+ 쿼리의 결과는 relation 이다. 
+ 가장 간단한 쿼리=> relation name
+ filter => select
+ slice => project
+ combine => cross-product, natural join, theta join
    
### 참고 자료 
+ [1](https://chokyuhwan.tistory.com/15)

[맨위로👆](#){: .btn .btn--primary }
