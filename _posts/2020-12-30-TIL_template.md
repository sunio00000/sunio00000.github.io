---
layout: post
tags: [all, til, git, jekyll, ruby, blog]
title: "💻 Git Blog를 Local Host에서 미리 보기" # 
date: 2020-12-30 00:00:00 -0400
categories: TIL
background: '/img/bg-post.jpg'
comments: true
---

> ##### ~~내가 왜 git으로 블로그를 시작한걸까...~~ 

# Tools
---
`Github`, `Jekyll`, `Ruby`, `Markdown`, `Bootstrap`  

## 1. Prologue
---
Github 블로그를 시작하기로 해버린 이상 하긴 해야하는데, 정말 하나부터 열까지 직접 구현을 해야한다.  
우습게도 정적 페이지로 깃 서버에서 돌아가기 때문에, 여느 블로그에나 있는 좋아요, 댓글과 같은 기능을 직접 구현할 수는 없어 여러 툴을 활용해야 한다. (최근, disqus를 통해서 댓글 기능을 추가하였다.)  
이러한 이유로 수정할 일도 많고 테스트 해보는 경우도 매우 잦은 블로그 시스템인데 문제는 내가 이걸 무식하게 글자하나 맘에 안들면 커밋하고, 폰트가 볼드체여서 커밋하고, 이미지 사이즈 바꾼다고 커밋을 하고 있다.  
그 덕에 깃허브의 잔디는 나에겐 발갛게 달아오른 얼굴 같은 것이 되었다. 😂  
(깃허브 블로그 시작하지마.. 아무튼 하지마...😐)  
## 2. Issue
---
깃허브 블로그는 `Github`에서 제공하는 서버 위에 `Jekyll`의 텍스트 변환 엔진을 통해 `HTML`, `markdown` Language를 미리 정의된 레이아웃에 따라서 표현하는 정적 웹사이트이다. 그 만큼 손이 많이 가기 때문에 이 것을 로컬 호스트에서 추가/변경 작업을 하고 싶다.

나의 목표는 **포스팅 작성 내용을 localhost에서 확인하고 수정해서 불필요한 커밋을 줄여보는 것이다.**

## 3. Resolve
---
1. 일단, `Ruby`를 다운 받아야 한다. [_Download_](https://www.ruby-lang.org/ko/downloads/) 링크에서 자신의 운영체제에 맞는 프로그램을 설치한다. `Jekyll`이 `Ruby`로 만들어져 있기에 다운을 받아야 한다고 한다.
2. `Jekyll` 외 몇 가지의 패키지를 설치해야한다.  
```ruby
 > gem install jekyll
 > gem install minima
 > gem install bundler
 > gem install jekyll-feed
 > gem install tzinfo-data
 ```
3. `Jekyll`을 실행한다. (이전에 jekyll이 포함된 repo를 클론하여야 하는 것을 잊지말자.)  
```ruby
 > jekyll serve
#만약, 인코딩 에러가 발생하면,
 > chcp 65001
#입력하고 다시 지킬을 실행한다.
```
4. 이후 `localhost:4000`으로 접속하면 로컬의 jekyll 블로그가 웹에 출력된다.

5. 만약 이런 아래와 같은 오류가 뜬다면, `Gemfile`이 원
하시는 모습으로 변경 해드려야 한다. (버전 번호를 변경해보자.)
<p align = "center">
<img src="https://user-images.githubusercontent.com/26760693/103355846-b12d2900-4af2-11eb-9297-a8cc7f24bdeb.png" width="500" height="130" /> </p>  

## 4. Code 
---
없음 -
## 5. Post Script
---
~~포스팅 한번 하기 더럽게 힘드네 진짜~~