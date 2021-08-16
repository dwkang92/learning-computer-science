# Operating System (10)

Understanding operating system is essential, not only for someone who working in the IT industry, but for everyone if they live on the earth.  The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education. 

### Date: August 16, 2021

## 1. SPN (Shortest-Process-Next)

---

![Untitled](Operating%20System%20(10)%2082100a73cbbb4c3db2968169efdd5988/Untitled.png)

1) Non-Preemptive Scheduling

2) Criteria for scheduling

1. Burst Time (실행시간) 기준
2. Burst Time 이 가장 작은 프로세스를 먼저 처리한다. (SJF Scheduling)

3) SPN 의 장점

1. 평균 대기시간 (Waiting Time) 최소화
2. 시스템 내 프로세스 수 최소화

    스케쥴링 부하 감소, 메모리 절약 → 시스템 효율 향상

3. 많은 프로세스 들에게 빠른 응답시간을 제공한다.

4) SPN 의 단점

1. Starvation (무한대기) 현상 발생
2. Burst Time 이 긴 프로세스는 자원을 할당 받지 못할 수도 있음. 이런 경우, Aging 등으로 해결한다.
3. 정확한 실행시간을 알 수 없다. 따라서 실행시간 예측 기법이 필요하다.

## 2. SRTN (Shortest Process Time Next)

---

1) SPN의 변형, Preemptive Scheduling

잔여 실행시간이 더 적은 프로세스가 Ready 상태가 되면 선점되어진다.

2) SRTN의 장점 : SPN의 장점 극대화

3) SRTN의 단점

1. 프로세스 생성시, 총 실행 시간 예측이 필요하다.
2. 잔여 실행을 계속 추적해야 한다. = Overhead
3. Context switching overhead

4) Reference

1. Preemptinve Scheduing: 잔여시간이 적은 프로세스가 등장하면, 순서를 뺏긴다.
2. Overhead = 부하가 걸린다.

## 3. HRRN (High-Response-Ratio-Next)

---

![Untitled](Operating%20System%20(10)%2082100a73cbbb4c3db2968169efdd5988/Untitled%201.png)

1) SPN의 변형

SPN + ***Aging concepts,*** Non-preemptive scheduling 

2) Aging Concepts

1. 프로세스의 대기시간 (WT)를 고려하여 기회를 제공한다.

3) Criteria for Scheduling

1. Response Ratio가 높은 프로세스 우선
2. Response Ratio = (WT+BT / BT)
3. SPN의 장점 + Starvation 방지
4. 실행 시간 예측 기법 필요 (Overhead)

## 4. 이해관계도 (相関図)

---

![Untitled](Operating%20System%20(10)%2082100a73cbbb4c3db2968169efdd5988/Untitled%202.png)