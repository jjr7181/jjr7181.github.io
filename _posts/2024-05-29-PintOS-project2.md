---
title: "[PintOS] Project2: Argument Passing 회고"
excerpt: "Kaist-PintOS Project2: User Programs: Argument Passing"

categories:
  - CS
tags:
  - [PintOS, OS]

permalink: /CS/PintOS-project2/

toc: true
toc_sticky: true
classes: wide

date: 2024-05-29
last_modified_at: 2024-05-29
---

### Argument Passing 구현 과제

> process_exec() 함수를 수정하여 커맨드 라인의 문자열을 토큰으로 분리하는 기능을 구현해야 한다. 

 현재 PintOS는 프로그램과 인자를 구분하지 못하는 구조이다. 때문에 프로그램 이름과 인자를 구분하여 스택에 저장하고, 인자를 프로그램에 전달해야 한다.

Argument Passing을 위해서 x86-64의 calling convention에 대한 선행지식이 필요하다.

<br>

#### x86-64 Calling Convention

Calling convention은 다음과 같다

1. 파싱된 argument들은 `%rdi`, `%rsi`, `%rdx`, `%rcx`, `%r8`, `%r9` 순으로 정수 레지스터 들에 저장되어 전달된다.
2. caller(함수를 호출하는 부분)의 다음 수행 명령어 주소를 스택에 저장하고 callee(호출 받은 함수)의 첫 번째 명령어로 jump한다. x86-64 명령어인 `CALL`이 저장과 jump 모두 수행
3. callee가 실행된다.
4. callee가 반환하는 값이 있다면 RAX register에 저장한다.
5. x86-64 명령어인 `RET`를 통해 callee는 스택으로부터 return address를 pop해서 return하고 해당 장소로 jump한다.

---

### Trouble Shooting












