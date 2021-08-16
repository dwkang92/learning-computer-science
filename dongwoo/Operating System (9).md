# Operating System (9)

Understanding operating system is essential, not only for someone who working in the IT industry, but for everyone if they live on the earth.  The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education. 

### Date: August 16, 2021

## 1. FCFS (First-Come-First-Service)

---

![Untitled](Operating%20System%20(9)%20924caa571b014c0790904f1a6a0f9344/Untitled.png)

1) Non-Preemptive Scheduling

2) Criteria for scheduling

1. Ready Queue (도착시간) 기준
2. 말 그대로 선착순이므로, 먼저 도착한 프로세스를 먼저 처리한다.

3) High Resource Utilization = Scheduling Overhead (low) / CPU works continuously

4) Batch system, Interactive System에 부적합하다.

5) FCFS의 단점

1. Convoy Effect

    하나의 수행시간이 긴 프로세스에 의해 다른 프로세스들이 긴 대기시간을 갖게 되는 현상

2. Response Time takes too much.

6) Reference

1. Non-Preemptive Scheduling: 프로세스하나가 코어 하나를 할당받으면, 완료될때까지 계속사용.
2. Burst Time (BT): 실행해야할 Task 하나가 일을 완료하는데에 걸리는 시간
3. Turnaround Time (TT): 처음으로 일을 요청하여 일이 끝날 때까지의 시간
4. Normalized TT = TT / BT (TT를 BT로 나눈 값). BT대비 얼마나 기다렸는가?
5. Normalized ~ : 뭔가 기준이 서로 다를 때, 동일한 선상에 놓고 평가하는 것.

## 2. Round-Robin (RR)

원형탁상위에서 돌아가면서 밥먹는 중국집을 생각하면 됨. 나도 한입 너도 한입 이렇게 일을 처리 해 나감.

---

![Untitled](Operating%20System%20(9)%20924caa571b014c0790904f1a6a0f9344/Untitled%201.png)

1) Preemptive Scheduling 

2) Criteria for scheduling

1. Ready Queue (도착시간) 기준
2. 말 그대로 선착순. 먼저 도착한 프로세스를 먼저 처리한다.

3) Time Quantum이 있음 (자원의 사용시간에 제한이 있음)

1. System Parameter
2. 프로세스는 할당된 시간이 지나면 자원을 반납하고 다음 차례로 넘긴다. (Time-Runout)
3. 특정 프로세스의 자원 독점을 방지한다.
4. Context Switch Overhead가 크다.

4) 대화형, 시분할 시스템에 적합하다.

5) Time Quantum (제한시간) 이 시스템 성능을 결정하는 핵심 요소이다.

6) FCFS의 단점

7) Reference

1. Burst Time (BT): 실행해야할 Task 하나가 일을 완료하는데에 걸리는 시간
2. Turnaround Time (TT): 처음으로 일을 요청하여 일이 끝날 때까지의 시간
3. Normalized TT = TT / BT (TT를 BT로 나눈 값). BT대비 얼마나 기다렸는가?
4. Normalized ~ : 뭔가 기준이 서로 다를 때, 동일한 선상에 놓고 평가하는 것.