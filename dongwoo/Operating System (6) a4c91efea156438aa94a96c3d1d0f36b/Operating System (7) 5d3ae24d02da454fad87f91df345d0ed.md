# Operating System (7)

Understanding operating system is essential, not only for someone who working in the IT industry, but for everyone if they live on the earth.  The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education. 

### Date: August 15, 2020

## 1. Thread

1) Process vs Thread

이전에 배웠던 대로, Process 는 자원을 할당받고 / 제어해서 결과를 만든다. 그리고 리소스를 제어하는 곳이다.

이중에서 제어를 담당하는 녀석을 Thread 라고 한다. 하나의 Process에는 여러가지 Thread가 존재한다.

2) Thread

- Light Weight Process (LWP)
- 프로세서(i.e. CPU)활용의 기본 단위
- 구성요소
    - Thread ID :나는 누구인가?
    - Register Set (PC, SP, etc.) : 나만의 작업장치
    - Stack (i.e. Local Data) : 나만의 공간
- 제어 요소 외 코드, 데이터 및 자원들은 프로세스 내 다른 스레드들과 공유한다.
- 전통적 프로세스 = 단일 스레드 프로세스

![Untitled](Operating%20System%20(7)%205d3ae24d02da454fad87f91df345d0ed/Untitled.png)

![Untitled](Operating%20System%20(7)%205d3ae24d02da454fad87f91df345d0ed/Untitled%201.png)

---

1. 스레드의 장점
    1. 사용자 응답성: 일부 스레드의 처리가 지연되어도, 다른 스레드는 작업을 계속 처리한다.
    2. 자원공유: 자원을 공유해서 효율성 증가 (커널 개입 회피가능)
    3. 경제성
    4. 멀티 프로세서 활용 (병렬처리) : 
    5. 사용자와 interaction이 있으면 멀티 스레드 사용한다 생각해라

1. 스레드의 구현

    1) 사용자 수준 스레드

    = 사용자 영역의 스레드 라이브러리로 구현 됨.

    - 스레드의 생성, 스케쥴링 등.
    - POSIX threads, Win32 threads, Java thread API, etc.

    = 커널은 스레드의 존재를 모름.

    - 커널의 관리(개입)를 받지 않음. 따라서, 생성 및 관리의 부하가 적으며 유연한 관리가 가능해진다.
    - 커널은 프로세스 단위로 자원을 할당한다. 즉, 하나의 스레드가 block 상태이면, 모든 스레드가 대기.

    2) 커널 수준 스레드 (Kernal Threads)

           = OS (Kernal)가 직접 관리한다.

           = 커널 영역에서 스레드의 생성, 관리 수행

           = 커널이 각 스레드를 개별적으로 관리한다. 하나의 스레드가 block되어도 다른 스레드는 계속 작업.