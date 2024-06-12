---
title: "[PintOS] Project3: Memory Management 회고"
excerpt: "Kaist-PintOS Project3: Virtual Memory: Memory Management"

categories:
  - CS
tags:
  - [PintOS, OS]

permalink: /CS/PintOS-project3-1/

toc: true
toc_sticky: true

date: 2024-06-07
last_modified_at: 2024-06-07
---

### Virtual Memory

> Virtual Memory를 구현하여 여러 개의 프로그램을 동시에 실행하고, 대용량 프로그램이 메인 메모리의 크기에 제약받지 않도록 한다.




<br>

#### Memory Management

Calling convention은 다음과 같다

1. 파싱된 argument들은 `%rdi`, `%rsi`, `%rdx`, `%rcx`, `%r8`, `%r9` 순으로 정수 레지스터 들에 저장되어 전달된다.
2. caller(함수를 호출하는 부분)의 다음 수행 명령어 주소를 스택에 저장하고 callee(호출 받은 함수)의 첫 번째 명령어로 jump한다. x86-64 명령어인 `CALL`이 저장과 jump 모두 수행
3. callee가 실행된다.
4. callee가 반환하는 값이 있다면 RAX register에 저장한다.
5. x86-64 명령어인 `RET`를 통해 callee는 스택으로부터 return address를 pop해서 return하고 해당 장소로 jump한다.

---

### Trouble Shooting











