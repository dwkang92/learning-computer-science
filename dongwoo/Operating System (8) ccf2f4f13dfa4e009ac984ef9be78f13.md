# Operating System (8)

Understanding operating system is essential, not only for someone who working in the IT industry, but for everyone if they live on the earth.  The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education. 

### Date: August 15, 2020

## Multi-programming (다중 프로그래밍)

---

1. 여러개의 프로레스가 시스템 내 존재한다.
2. 프로세스가 여러개이기 때문에, 자원을 할당 할 프로세스를 선택 해야 한다. (Scheduling)
3. 자원관리
    1. 시간 분할 관리 (Time Sharing)
        1. 하나의 자원을 여러 스레드들이 번갈아 가며 사용. 예) Processor (CPU)
        2. Process scheduling (프로세스 스케쥴링) : 프로세서 사용시간을 프로세스들에게 분배.
    2. 공간 분할 관리 (Space Sharing) 
        1. 하나의 자원을 분할하여 동시에 사용.
        2. 메모리

1. Purpose of Scheduling
    1. 시스템의 성능 향상
    2. 성능이란? 
        1. 응답시간, 작업 처리량, 자원 활용도
    3. 목적에 맞는 지표를 고려하여 스케쥴링 기법을 선택한다.

    ![Untitled](Operating%20System%20(8)%20ccf2f4f13dfa4e009ac984ef9be78f13/Untitled.png)

1. Criteria for Scheduling (스케쥴링 기법이 고려하는 항목들)
    1. Process의 특성 (I/O-bounded or compute -bounded)
    2. 시스템 특성 (Batch System or Interactive system)
    3. 프로세스의 긴급성 (Hard or Soft Real time, non-real time systems)
    4. 프로세스 우선순위 (Priority)
    5. 프로세스 총 실행 시간.