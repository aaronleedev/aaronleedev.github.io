---
layout: post
title: Jekyll을 이용한 github에 블로그 만들기
---

1. [github](https://github.com/) 계정생성
2. github repository 생성
*  repository name을 "github username.github.io"으로 생성
*  "Initialize this repository with a README" 체크
*  ![_config.yml]({{ site.baseurl }}/images/2017-07-25-github-jekyll-01.png)
3. [wingit](https://git-scm.com/download/win) 설치
4. [Jekyll 소스코드](https://github.com/barryclark/jekyll-now) 다운
5. 새 로컬저장소에 github repository init
*  $ git init
*  $ git remote add origin https://github.com/username/repositoryname.git
*  $ git pull origin master
6. github repository에 Jekyll 소스코드 push
*  새 로컬저장소에 Jekyll 소스코드 copy
*  $ git add .
*  $ git commit -m "commit description
*  $ git push -u origin master
7. https://repositoryname url 확인