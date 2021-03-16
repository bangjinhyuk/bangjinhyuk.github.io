---
layout: post
title: "Database Relational Model"
subtitle: "아주대학교 데이터 베이스 수업."
categories: [Database]
tags: [Ajou]
date: 2021-03-15 08:00:00
background: '/img/6.jpg'
---

# Database

#### Relational Model
1. 특징
    + major commercial database system에 주로 사용
    + 매우 단순한 모델 (table)
    + Query with high-level languages => read(retrieve)/write(modify)
    + 효율적이다.    
    
2. Schema
    + tabel (relations)의 구성 성분 ex) 테이블명 ,테이블에서 columns 
    + Relational Model 에서는 attribute(columns)라 불림 
    + 각각의 attribute들은 type(domain)을 가짐

3. Instance
    + data들
    + Relational Model 에서는 tuple(row)라고 불림

4. NULL (두가지 경우)
    + "unknown" 아직 없다.
    + "undefined" 정의되어있지 않다.

5. Key 
    + 각각의 tuple에서 고유한 값
    
6. create relations in SQL

    + ```sql
        Create Table Studen(ID, name, GPA, photo);
       ``` 
    + ```sql
        Create Table College(name string, state char(2), enrollment integer);
        ```
    

    
    
[맨위로👆](#){: .btn .btn--primary }
