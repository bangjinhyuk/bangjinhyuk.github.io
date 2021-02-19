---
layout: post
title: "github-vscode-ubuntu 연동 오류들"
subtitle: "AWS-Node.js 서버 구축 공부."
date: 2021-02-15 08:00:00
background: '/img/posts/01.jpg'
---
## AWS-Node.js 서버 구축하여 github-vscode-ubuntu 사용시 발생했던 오류들

1. vscode에서 ftp-simple을 사용하여 코드 수정시 Permission Denied가 뜰때
    ```
    $ chown -R root:root (디렉토리 이름)
    $ chmod -R 777 (디렉토리 이름)
    ```
    
1. ubuntu에서 깃허브로 올리는 순서
    ```
    $ sudo git init
    $ git status
    $ sudo git add -A : 모든 파일 추가
    $ sudo git commit
    $ sudo git commit -m "커밋 메세지 작성"
    $ sudo git push origin +master(또는 main)
    $ sudo git pull(저장소 업데이트)
    $ git log
    ```

3. error: Your local changes to the following files would be overwritten by merge: 와 같은 에러 발생시
    ```
    $ git stash
    $ sudo git pull(저장소 업데이트)
    ```
+ 참조 사이트
    + [git pull 에러시] (https://steemit.com/develope/@snowsprout/git-git-pull-error-your-local-changes-to-the-following-files-would-be-overwritten-by-merge)
    + [ftp-simple 수정 권한 에러시] (https://share4share.tistory.com/32) 

[맨위로👆](#){: .btn .btn--primary }
