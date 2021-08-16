# Operating System (11)

Understanding operating system is essential, not only for someone who working in the IT industry, but for everyone if they live on the earth.  The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education. 

### Date: August 16, 2021

## 1. MLQ (Multi-level Queue)

---

![Untitled](Operating%20System%20(11)%2006696d4e35964d29be2933be155a40a9/Untitled.png)

1) 작업 (or 우선순위)별 별도의 Ready Queue를 가짐

1. 최초 배정 된 queue를 벗어나지 못함
2. 각각의 queue는 자신만의 스케쥴링 기법 사용

2) Queue 사이에는 우선순위 기반의 스케쥴링 사용

3) MLQ 의 장점

1. 빠른 응답시간

4) SPN 의 단점

1. 여러개의 Queue 관리 등, 스케쥴링 Overhead
2. 우선순위가 낮은 Queue는 Starvation 발생 가능.

## 2. MFQ (Multi-level Queue)

---

![Untitled](Operating%20System%20(11)%2006696d4e35964d29be2933be155a40a9/Untitled%201.png)

1) 프로세스의 Queue간 이동이 허용된 MLQ

2) Feedback을 통해 우선 순위 조정

현재까지의 프로세서 사용 정보(패턴) 활용

3) MFQ의 특성

1. Dynamic Priority
2. Preemptive Scheduling
3. Favour short burst-time processes
4. Favour I/O bounded processes
5. Improve adaptability

4) 프로세스에 대한 사전 정보 없이 SPN, SRTN, HRRN 기법의 효과를 볼 수 있음.

5) MFQ의 단점

1. 설계 및 구현이 복잡하고, 스케쥴링 overhead가 크다.
2. Starvation 문제가 있음.

6) 변형

1. 각 준비 큐마다 시간 할당량을 다르게 배정

    프로세스의 특성에 맞는 형태로 시스템 운영이 가능.

2. 입출력 위주 프로세스들을 상위 단계의 큐로 이동시켜 우선 순위를 높인다.
    - 프로세스가 block될 때 상위의 준비 큐로 진입하게 함.
    - 시스템 전체의 평균 응답 시간을 줄이고, 입출력 작업을 분산시킴.
3. 대기 시간이 지정된 시간을 초과한 프로세스들을 상위 큐로 이동시킨다.
    - Aging 기법