# Operating System (12)

Understanding operating system is essential, not only for someone who working in the IT industry, but for everyone if they live on the earth. The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education.

### Date: August 16, 2021

## 1. Process Synchronization (동기화)

---

1. 다중 프로그래밍 시스템

1) 여러개의 프로세스들이 존재
2) 프로세스들은 서로 독립적으로 동작
3) 공유 자원 또는 데이터가 있을 때, 문제 발생 가능.

2. 동기화

1) 프로세스들이 서로 동작을 맞추는 것
2) 프로세스들이 서로 정보를 공유 하는 것.
3) 위 두가지를 그냥 간단하게, 프로세스들이 서로 대화를 하면서 동작을 맞춘다는 걸 의미.

3. Asynchronous and Concurrent P's

1) 비동기적 (Asynchronous): 프로세스들이 서로에 대해 모름.
2) 병행적 (Concurrent): 여러개의 프로세스들이 동시에 시스템에 존재한다. ""동시에""
3) 병행수행중인 비동기적 프로세스들이 공유자원에 동시에 접근할 때 문제가 발생 할 수 있음. 왜냐면 서로 동시에 작업하는데 대화도 없고, 그러다보면 문제가 발생하게 된다. 왜 동기화가 필요한지 알겠죠?

4. Reference

1) Shared Data or Critical Data: 여러 프로세스딜이 공유하는 데이터
2) Critical Section (임계 영역): 공유 데이터를 접근하는 코드 영역 (Code Segment)
3) Mutual Exclusion (상호배제): 둘 이상의 프로세스가 동시에 Critical Section에 진입하는 것을 막는다.
4) Machine Instruction cannot be divided (indivisible) = Atomicity (원자성)

## 2. Mutual Exclusion Methods

---

1. Mutual Exclusion Primitives

1) enterCS() Primitive
   - Critical Section 진입 전 검사
   - 다른 프로세스가 Critical Section 안에 있는지 검사
2) ExitCS() Primitive
   - Critical Section을 벗어날 때의 후처리 과정
   - Critical Section을 벗어남을 시스템이 알림

2. Requirements for ME Primitives

1) Mutual Exclusion (상호배제)
   - Critical Section에 프로세스가 있으면, 다른 프로세스의 진입을 금지.
2) Progress (진행)
   - CS안에 있는 프로세스 외에는, 다른 프로세스가 CS에 진입하는 것을 방해하면 안됨.
3) Bounded Waiting (한정대기)
   - 프로세스의 CS진입은 유한시간 내에 허용되어야 함.
