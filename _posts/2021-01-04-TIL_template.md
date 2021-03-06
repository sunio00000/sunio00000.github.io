---
layout: post
tags: [all, til, git, mistake]
title: "👨🏻‍💻 Git 커밋 Template 아름답게 전달하자" # 
date: 2021-01-04 00:00:00 -0400
categories: TIL
background: '/img/bg-post.jpg'
comments: true
---
깃을 통해 정보와 프로젝트, 제대로 공유하는 방법

## Tools
`Git`

## 1. Prologue
---
우리는 서로를 이해시키는 무한한 소통의 과정을 거치며, 그 과정에 따라 웃으며 술 한잔 할 수 있는 팀워크인지 폭망해 카톡 숨김 목록을 차지하는 팀워크를 만나게 된다.  
코드를 Clean 하게 작성하는 것 이외로 우리는 개발을 하면서 협업을 하고 여러 의사결정을 하게 된다.    
도구는 손짓 발짓이 될 수도 있고, 코드 그 자체가 되기도 한다. (뭐 이외에도 굉장하고 무궁무진한 방법들이 많긴하다. 🙄)  
우리는 효율적인 의사소통 도구의 활용이 우리에게 당연히도 최대의 이득을 가져다 줄 것이라 생각한다.  
하지만, 게을러서 포기하는 어떠한 (수많은) 것들이 있다..  
그 중에 버전관리 프로그램을 사용하며 작성하는 `Commit message`를 이쁘고 명료하게 작성해보자.  

## 2. Issue
---
내가 무엇을 `Commit` 했었는지, 전혀 알 수가 없다. 이건 똥이다.
<p align="center"><img src="https://user-images.githubusercontent.com/26760693/103532788-363b8800-4ecf-11eb-8429-f39a62c129e8.png" width="700" height="400"></p>  

## 3. Resolve
---

1. Commit template이 될 작성 파일을 생성한다.
```shell
# windows powershell
$ ni ~/.gitmessage.txt
# linux shell
$ touch ~/.gitmessage.txt
```
2. 에디터를 통해 파일에 접근하여 팀이 정한 템플릿(**[목차 4] Code** 참고)을 그대로 넣고 저장한다.  
3. `commit.template`에 이 파일을 적용해준다.
```shell
git config --global commit.template ~/.gitmessage.txt
```
4. 이 후의 깃 커밋 시에는 git commit (옵션 없이)를 치면 아래와 같은 화면이 나온다  
5. 제목/본문/꼬릿말로 구성된 내용을 수정하고 커밋한다
<p align='center'><img src="https://user-images.githubusercontent.com/26760693/103534155-b531c000-4ed1-11eb-8d29-1e2c0df910e0.png" width="650" height="500"></p>  


 
## 4. Code 
---
템플릿 예제.
```shell
# <타입>: <제목>

##### 제목은 최대 50 글자까지만 입력 ############## -> |


# 본문은 위에 작성
######## 본문은 한 줄에 최대 72 글자까지만 입력 ########################### -> |

# 꼬릿말은 아래에 작성: ex) #이슈 번호

# --- COMMIT END ---
# <타입> 리스트
#   feat    : 기능 (새로운 기능)
#   fix     : 버그 (버그 수정)
#   refactor: 리팩토링
#   style   : 스타일 (코드 형식, 세미콜론 추가: 비즈니스 로직에 변경 없음)
#   docs    : 문서 (문서 추가, 수정, 삭제)
#   test    : 테스트 (테스트 코드 추가, 수정, 삭제: 비즈니스 로직에 변경 없음)
#   chore   : 기타 변경사항 (빌드 스크립트 수정 등)
# ------------------
#     제목 첫 글자를 대문자로
#     제목은 명령문으로
#     제목 끝에 마침표(.) 금지
#     제목과 본문을 한 줄 띄워 분리하기
#     본문은 "어떻게" 보다 "무엇을", "왜"를 설명한다.
#     본문에 여러줄의 메시지를 작성할 땐 "-"로 구분
# ------------------
```  
## 5. Post Script
---
일의 마무리를 보람차게 매듭짓도록 커밋메시지를 작성해보자.
## 6. Reference
---
Git Documentation 中 :: [8.1 Git맞춤-git-설정하기](!https://git-scm.com/book/ko/v2/Git%EB%A7%9E%EC%B6%A4-Git-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0)