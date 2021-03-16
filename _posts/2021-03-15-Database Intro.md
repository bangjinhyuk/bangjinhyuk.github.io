---
layout: post
title: "Database, DBMS 정의"
subtitle: "아주대학교 데이터 베이스 수업"
categories: [Database]
tags: [Ajou]
date: 2021-03-15 08:00:00
background: '/img/5.jpg'
---

# Database

##### DBMS  = Database Management System
1. DBMS 종류: 상용버전(오라클,MS) , 오픈소스 (MySQL, PostgreSQL,SQLite)

2. DBMS를 통해서 데이터 베이스에 저장하고 접속(read/write)할수 있게 해준다.

3. DataBase 특징
    + Massive (큰사이즈의 데이터를 다룬다)
    + Persistent (한번 저장되면 지우기 전까지 저장)
    + Safe (안전하다)
    + Multi-user(동시 공유=>concurrent sharing)
    + Convenient (복잡하지 않다. high-level query language, physical data independence=>table 개념 )
    + Efficient (처리속도가 높다)
    + Reliable (안정적)

4. Database 어플리케이션은 framework를 통해 프로그래밍 된다.

5. 데이터 중심 어플리케이션(Data-intensive applications)는 DBMS를 사용하지 않는다.

6. Key concepts
    + Data model (데이터를 어떻게 구성하는지 정한 모델, 구성 요소 정의 ex) table , set of records, XML, graph)
    + Schema versus data
        * schema = 데이터 베이스 안에 구성요소들의 구조 =>type
            <img src="/img/schema.jpg"  width="400" height="370">
        * 해당 위의 사진에서 내부 스키마 부분
        * data => variables 실제 데이터들
    + Data definition language(DDL) => 스키마 정의 부분 ex) create
    + Data manipulation or query language (DML) => 데이터 read(quering)/write(modifying) 쿼리문들

7. Key people
    + DBMS implementer (DBMS를 만드는 사람들)
    + Database designer (스키마 디자이너)
    + Database application developer(어플리케이션을 개발하는 사람=> 흔히 말하는 서버 개발자)
    + Database administer (데이터 베이스 관리자)
        

[맨위로👆](#){: .btn .btn--primary }
