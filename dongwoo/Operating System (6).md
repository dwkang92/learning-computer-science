# Operating System (6)

Understanding operating system is Essential knowledge, not only for someone who working in the IT industry, but for everyone if they live on the earth.  The main purpose of this course is to understand basic knowledge of Computer Science: Operating System with related references. Basically will Use online courses via Youtube, provided by Korea University of Technology and Education. 

### Date: August 15, 2020

## 1. Interrupt

   

1) 예상치 못한, 외부에서 발생한 이벤트를 의미하며, 아래와 같은 종류의 Interrupt가 존재한다.

- I/O Interrupt
- Clock Interrupt
- Console Interrupt
- Program Check Interrupt
- Machine Check Interrupt
- Inter-Process Interrupt
- System Call Interrupt

![Untitled](Operating%20System%20(6)%20a4c91efea156438aa94a96c3d1d0f36b/Untitled.png)

Reference: HPC Lab. KOREATECH, Lecture 3. Process Management (2/2)

2) Context Switching

![Untitled](Operating%20System%20(6)%20a4c91efea156438aa94a96c3d1d0f36b/Untitled%201.png)

3) Context Switch Overhead

- Context switching에 소요되는 비용
    - Depends on OS
    - OS의 성능에 큰 영향을 준다.

- 불필요한 Context Switching을 줄이는 것이 중요하다.

    ex) Thread 사용 등...