# Operating System (5)

Understanding operating system is essential, not only for someone who working in the IT industry, but for everyone if they live on the earth.  The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education. 

### Date: August 15, 2020

## Process Management (프로세스 관리)

1. Job / Program vs Process
    1. Program: 우리가 일반적으로 사용하는 그 "프로그램". 컴퓨터 시스템에 실행 요청 전의 상태.
    2. Process: 실행을 위해 시스템(Kernal)에 등록된 작업. 시스템 성능 향상을 위하여 커널에 의해 관리.

![Untitled](Operating%20System%20(5)%2083173a9b2bed4d84a0376be434eb6d7c/Untitled.png)

Reference: HPC Lab. KOREATECH, Lecture 3. Process Management (1/2)

---

1. **Process ?**

    ![Untitled](Operating%20System%20(5)%2083173a9b2bed4d84a0376be434eb6d7c/Untitled%201.png)

    Reference: HPC Lab. KOREATECH, Lecture 3. Process Management (1/2)

    1) 실행중인 프로그램

    - 커널에 등록되고 커널의 관리하에 있는 작업
    - 각종 자원들을 요청하고 할당 받을 수 있는 개체
    - 프로세스 관리 블록을 할당받은 개체
    - 능동적인 개체 (active entity)
        - 실행 중에 각종 자원을 요구, 할당, 반납하며 진행

    2) Process Control Block (PCB)

    - 커널 공간 (Kernal Space) 내에 존재한다.
    - 각 프로세스들에 대한 정보를 관리한다.

---

1. **Resource**

    1) 의미: 커널의 관리 하에 프로세스에게 할당 / 반납되는 수동적 개체 (Passive entity)

    2) Category of "Resource" in Computer Science

    - H/W:

        Processor, Memory, Disk, Monitor, Keyboard, etc.

    - S/W:

        Message, Signal, Files, Installed SWs, etc.

---

1. **Process Control Block (PCB)**

![Untitled](Operating%20System%20(5)%2083173a9b2bed4d84a0376be434eb6d7c/Untitled%202.png)

Reference: HPC Lab. KOREATECH, Lecture 3. Process Management (1/2)

![Untitled](Operating%20System%20(5)%2083173a9b2bed4d84a0376be434eb6d7c/Untitled%203.png)

Reference: HPC Lab. KOREATECH, Lecture 3. Process Management (1/2)

---

1. **Process States**

![Untitled](Operating%20System%20(5)%2083173a9b2bed4d84a0376be434eb6d7c/Untitled%204.png)

Reference: HPC Lab. KOREATECH, Lecture 3. Process Management (1/2)

![Untitled](Operating%20System%20(5)%2083173a9b2bed4d84a0376be434eb6d7c/Untitled%205.png)

Reference: HPC Lab. KOREATECH, Lecture 3. Process Management (1/2)

1) **Created State**

- 어떤 작업(Job)이 생성 및 Submit 되어, PCB 할당과 커널에 프로세스가 생성 된 상태.
- 가용 메모리 공간 체크 및 프로세스 상태 전이 (Ready or Suspended ready)

    메모리가 남아있냐 없냐에 따라 상태가 결정되어진다.

2) **Ready State**

- 프로세서 (CPU) 외에 다른 모든 자원을 할당 받은 상태. 프로세서만 없는 상태
    - 프로세서 할당 대기 상태
    - 즉시 실행 가능 상태
- Dispatch (or Schedule)
    - Ready State → Running State

 3) Running State

- 프로세서와 필요한 자원을 모두 할당 받은 상태
- Preemption
    - Running State → Ready States
    - 프로세서 스케쥴링 (ex: time-out, priority changes)
- Block / Sleep
    - Running State → asleep state
    - I/O와 같은 자원할당을 요청한다.

 4) Blocked / Asleep State

- 프로세서 외에 다른 자원을 기다리는 상태
    - 자원 할당은 System Call에 의해 이루어 짐.
- Wake-up
    - Asleep State → Ready State

 5) Suspended State

![Untitled](Operating%20System%20(5)%2083173a9b2bed4d84a0376be434eb6d7c/Untitled%206.png)

- 메모리를 할당 받지 못한 (빼앗긴) 상태
    - Memory Image를 Swap Device에 보관
        - Swap Device: 프로그램 정보 저장을 위한 특별한 파일 시스템
- Swap-out (Suspended), Swap-in (Resume)

 6) Terminated / Zombie State

- 프로세스 수행이 끝난 상태
- 모든 자원 반납 후, 커널 내에 일부 PCB 정보만 남아있는 상태.