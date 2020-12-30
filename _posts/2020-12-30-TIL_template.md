---
layout: post
title: "👨🏻‍💻[TIL] GIT Blog를 Local에서 미리 작성해 확인하기" # 
date: 2020-12-30 00:00:00 -0400
categories: daily, TIL
background: '/img/bg-post.jpg'
---

> ##### ~~내가 왜 git으로 블로그를 시작한걸까...~~ 

#### [Related]
---
`Github`, `Jekyll`, `Ruby`, `Markdown`, `Bootstrap`
# 1. Prologue
---
Github 블로그를 시작해서 고생받는 이야기, 진행 중 아주 일부... 
(너희는 이런거 하지마라...😐)  

# 2. Issue
---
<h5><ol><b> "Github 블로그의 Commit/Push 전에 로컬에서 수정해보자" </b></ol></h5>
깃허브 블로그는 `Github`에서 제공하는 서버 위에 `Jekyll`의 텍스트 변환 엔진을 통해 `HTML`, `markdown` Language를 미리 정의된 레이아웃에 따라서 표현하는 정적 웹사이트이다. 

문제는 내가 이걸 무식하게 글자하나 맘에 안들면 커밋하고, 폰트가 볼드체여서 커밋하고, 이미지 사이즈 바꾼다고 커밋을 하고 있다. 그 덕에 내게 깃허브의 잔디는 내 부끄러움의 정도를 나타낸다고 볼 수 있겠다. 😂

**포스팅 작성 내용을 localhost에서 확인하고 수정해서 불필요한 커밋을 줄여보자.**

# 3. Resolve
---
1. 일단, `Ruby`를 다운 받아야 한다. [Download](https://www.ruby-lang.org/ko/downloads/) 링크에서 자신의 운영체제에 맞는 프로그램을 설치한다. `Jekyll`이 `Ruby`로 만들어져 있기에 다운을 받아야 한다고 한다.
2. `Jekyll` 외 몇 가지의 패키지를 설치해야한다.  
```Ruby
 > gem install jekyll
 > gem install minima
 > gem install bundler
 > gem install jekyll-feed
 > gem install tzinfo-data
 ```
3. `Jekyll`을 실행한다. (이전에 레포 클론을 해야한다)  
```Ruby
 > jekyll serve
만약, 인코딩 에러가 발생하면,
 > chcp 65001
입력하고 다시 지킬을 실행한다.
```
4. 이후 `localhost:4000`으로 접속하면 로컬의 jekyll 블로그가 웹에 출력된다.

5. 만약 이런 아래와 같은 오류가 뜬다면, `Gemfile`을 원
하시는 대로 변경 해드려야 한다.
<p align = "center">
<img src="https://user-images.githubusercontent.com/26760693/103355846-b12d2900-4af2-11eb-9297-a8cc7f24bdeb.png" width="500" height="130" /> </p> 
# 4. Code 
---
없음 -
# 5. Post Script
---
~~포스팅 한번 하기 더럽게 힘드네 진짜~~