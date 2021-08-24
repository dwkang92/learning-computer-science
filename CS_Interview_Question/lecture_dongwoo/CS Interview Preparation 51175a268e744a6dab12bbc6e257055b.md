# CS Interview Preparation

# Synchronous & Asynchronous Processing

---

## ⚽️ Goal

---

1.  Understand the exact definition of Syn & Async Processing with proper examples.
2. Can explain the differences with "Blocking" & "Non-Blocking".
3. Reference should be mentioned.

## 📚 Contents

---

1. Why these concepts sare important?
2. Definition and example
3. Reference

## 1. Why these are important?

---

효율성, 한정된 자원안에서 최고의 효율을 뽑아내는 것.

## 2. Definition and Example

---

- 이미지를 통한 예시

    Sync vs. Async

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled.png)

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%201.png)

- Thread?
    1. 예) 4코어 8쓰레드: 4개의 코어로 이루어져있고, 일하는 녀석이 8개가 있다.
    2. 연산처리를 수행하는 친구들.

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%202.png)

    [https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s](https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s)

    c. 만약, Task 3의 업무량이 엄청난다면? 여기서 동기, 비동기의 개념이 나옴.

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%203.png)

    [https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s](https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s)

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%204.png)

- Sync vs. Async

    동기와 비동기는 작업을 수행하는 주체가 2개이상이 필요 합니다.

    한국어, 영어, 일본어 할것없이 이 개념에 대해선 수많은 설명자료들이 많이있습니다.

    각자 더 알아보시고 싶으신 부분이 있으면 그 부분은 각자 찾아보시길 바랍니다.

    **동기**는 말그대로 "요청" 과 " 결과" 가 "동시에" 일어난다는 뜻입니다. 

    작업의 시간 (시작, 종료 등) 을 서로 같은 타이밍에 맞추는 것을 동기라고 부릅니다.

    하나의 요청에 대한 작업이 모두 다 끝나면, 맨 처음에 받았던 요청 + 그에 대한 결과를 제출한 뒤, 그 다음 작업을 실행하고, 또 해당 작업이 끝나면 그 다음 작업으로 넘어가는것을 상상해보면 될듯 합니다. 

    시스템 설계가 간단하겠죠? 방해받는 것도 없고, 순서대로만 잘 진행되면 될테니까요. 직관적이고 간단한 설계방식이 장점이지만, 하나의 업무에 대한 결과가 주어질 때 까지 대기해야하는 단점이 있습니다.

    **비동기**는 말 그대로 "요청" 과 "결과" 가 "동시에 일어나지 않는다" 는 뜻입니다.

    서로의 작업시간이 관계 없다면 이를 비동기라고 부릅니다.

    바쁜 아침출근 준비를 생각하면 됩니다. 샤워하면서 양치하고, 양복 입으면서 아침 간단하게 먹는 거랑 비슷한 느낌이지요. 하나의 작업을 돌려놓고, 그 사이에 다른 작업도 실행해두는 멀티태스킹을 생각해보면 이해하기 쉽습니다.

    아침 출근을 생각한다면, 비동기식 시스템 설계는 왠지 모르게 복잡할 것 같습니다. 동시에 여러가지 처리가 필요하니까요. 결과가 주어지는데 시간이 걸리더라도, 그 사이에 시간이 얼마 걸리지 않는 다른 작업을 할 수 있으므로, 한정된 자원을 효율적으로 사용할 수 있을 겁니다.

- Blocking vs. Non-blocking

    다른 작업을 수행하는 주체를 어떻게 상대하는지가 중요합니다. 

    자신의 작업을 하다가 다른 작업 주체가 하는 작업의 시작부터 끝까지 기다렸다가, 다시 자신의 작업을 시작하면 블로킹이라 하고, 다른 주체의 작업과 관계없이 자신의 작업을 계속한다면 이를 논블로킹.

    동기 (Sync)에서 보았듯, 하나의 작업이 끝날 때 까지 기다린다 → Blocking되어있다.

    비동기 (Async)는 여러 작업이 동시에 일어난다. 끝날 때 까지 기다리지 않으니, Non-Blocking이 된다.

    Blocking되지 않는다는 것의 의미는, 실행되어지는 각각의 작업들은 큐에 넣거나 다른 스레드에게 해당 task를 맡기고 다른 코드 및 작업을 실행한다는 의미.

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%205.png)

    Reference: [https://deveric.tistory.com/99](https://deveric.tistory.com/99)

## 🔎 Reference

---

1. Website
    1. [https://www.outsystems.com/blog/posts/asynchronous-vs-synchronous-programming/](https://www.outsystems.com/blog/posts/asynchronous-vs-synchronous-programming/)
    2. [https://evan-moon.github.io/2019/09/19/sync-async-blocking-non-blocking/](https://evan-moon.github.io/2019/09/19/sync-async-blocking-non-blocking/)
    3. [https://juyeop.tistory.com/22](https://juyeop.tistory.com/22)
    4. [https://private.tistory.com/24#:~:text=동기와 비동기는 어떤,있고%2C 동시에 이루어지지도 않습니다](https://private.tistory.com/24#:~:text=%EB%8F%99%EA%B8%B0%EC%99%80%20%EB%B9%84%EB%8F%99%EA%B8%B0%EB%8A%94%20%EC%96%B4%EB%96%A4,%EC%9E%88%EA%B3%A0%2C%20%EB%8F%99%EC%8B%9C%EC%97%90%20%EC%9D%B4%EB%A3%A8%EC%96%B4%EC%A7%80%EC%A7%80%EB%8F%84%20%EC%95%8A%EC%8A%B5%EB%8B%88%EB%8B%A4).
    5. [https://www.youtube.com/watch?v=m0icCqHY39U](https://www.youtube.com/watch?v=m0icCqHY39U)
    6. [https://www.youtube.com/watch?v=U42qWURR6Gw](https://www.youtube.com/watch?v=U42qWURR6Gw)
    7. [https://www.inflearn.com/course/sync-async-개념-이해/lecture/33682?tab=curriculum](https://www.inflearn.com/course/sync-async-%EA%B0%9C%EB%85%90-%EC%9D%B4%ED%95%B4/lecture/33682?tab=curriculum)
    8. [https://www.youtube.com/watch?v=IdpkfygWIMk](https://www.youtube.com/watch?v=IdpkfygWIMk)
    9. [https://deveric.tistory.com/99?category=387263](https://deveric.tistory.com/99?category=387263)
    10. [https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s](https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s)