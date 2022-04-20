---
layout: post
title: "Docker 엔트리포인트와 커맨드, 환경 변수"
subtitle: "Docker 개념과 명령어 모음집"
categories: [DevOps]
tags: [Server,Docker,DevOps]
date: 2022-04-21 01:00:00
background: '/img/4.jpg'
---

### 엔트리 포인트란?

도커 컨테이너가 실행할때 고정적으로 실행되는 스크립트 혹은 명령어 →  생략가능

생략될 경우 커맨드에 지정된 명령어로 수행

<br>

### 커맨드란?

도커 컨테이너가 실행할 때 수행할 명령어 록은 엔트리 포인트에 지정된 명령어에 대한 인자값

<br>

### Dockerfile 예시

```docker
FROM node:12-alpine
RUN apk add --no-cache python3 g++ make
WORKDIR /app
COPY . .
RUN yarn install --production

ENTRYPOINT ["docker-entrypoint.sh"]         # 해당 sh 파일을 실행한다.
CMD ["node"]
```

<br>

### 명령어 예시

`$ docker run --entrypoint sh ubuntu:focal`

→ shell 실행 → command = sh

`$ docker run --entrypoint echo ubuntu:focal hello world`

→ hello world 출력→ command = echo hello world

<br>

### 환경변수 주입 방법

`$ docker run -i -t -e MY_HOST=bbangi.com ubuntu:focal bash`

파일로 넣는법

- env 파일 생성 : `vim sample.env -> 환경변수 입력후 저장 -> cat sample.env`
- `$ docker run -i -t --env-file ./sample.env ubuntu:focal bash`

<br>

### 환경변수 확인 방법

컨테이너 접속 후 →  `echo $MY_HOST`

전체 환경변수를 보려면 → `env`

<br>

[맨위로👆](#){: .btn .btn--primary }

