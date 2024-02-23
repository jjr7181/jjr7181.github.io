---
title: "[Git] Git 기초지식 #1"
excerpt: "Git 기초지식 #1"

categories:
  - Git
tags:
  - [Git, VCS]

permalink: /git/post-name-here-4/

toc: true
toc_sticky: true

date: 2022-07-24
last_modified_at: 2022-07-24
---

<h2>Git 기초지식 #1</h2>

### What is Git?  

Git은 VCS(Version Control System) 중 하나로 프로그램의 버전 관리를 위한 툴이다.  
여기서 버전을 관리한다는 것은 프로젝트의 **시간**과 **차원**을 관리한다는 것으로 이해 할 수 있다.

>\* 시간과 차원  
시간 - 프로젝트의 버전을 과거로 되돌리거나 특정 내역을 취소하도록 함.  
차원 - 프로젝트의 여러 모드를 쉽게 전환하고 관리할 수 있다.

이러한 특징은 여러 사람들이 Git을 통해 프로젝트에서 협업할 수 있도록 도와준다.

---

### Git을 사용하는 두가지 방법
>CLI(Command Line Interface) vs GUI(Graphical user interface)

하나를 정해서 사용해야 하는 것이 아니라,
Git에서 뭔가를 실행하기 위한 즉, 어떤 명령들을 사용할 때는 CLI 방법을 쓰고, Git상태에서 자세히 살펴보기 위해서는 소스트리 창(GUI)를 사용한다.

---

### .gitignore

터미널에 git status를 입력하였을 때 나타나는 untracked files(git에 의해 아직 관리되지 않는 파일)에서 배제하는 것

## 배제하는 이유
1. 포함할 필요가 없을 때  
- 자동으로 생성 또는 다운로드 되는 파일들 (빌드 결과물, 라이브러리)
  
2. 포함하면 안되는 파일들
- 보안상 민감함 정보를 담은 파일
- 따로 관리해야하는 파일  