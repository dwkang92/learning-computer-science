# CS Interview Preparation

# Synchronous & Asynchronous Processing

---

## β½οΈ Goal

---

1.  Understand the exact definition of Syn & Async Processing with proper examples.
2. Can explain the differences with "Blocking" & "Non-Blocking".
3. Reference should be mentioned.

## π Contents

---

1. Why these concepts sare important?
2. Definition and example
3. Reference

## 1. Why these are important?

---

ν¨μ¨μ±, νμ λ μμμμμ μ΅κ³ μ ν¨μ¨μ λ½μλ΄λ κ².

## 2. Definition and Example

---

- μ΄λ―Έμ§λ₯Ό ν΅ν μμ

    Sync vs. Async

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled.png)

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%201.png)

- Thread?
    1. μ) 4μ½μ΄ 8μ°λ λ: 4κ°μ μ½μ΄λ‘ μ΄λ£¨μ΄μ Έμκ³ , μΌνλ λμμ΄ 8κ°κ° μλ€.
    2. μ°μ°μ²λ¦¬λ₯Ό μννλ μΉκ΅¬λ€.

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%202.png)

    [https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s](https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s)

    c. λ§μ½, Task 3μ μλ¬΄λμ΄ μμ²­λλ€λ©΄? μ¬κΈ°μ λκΈ°, λΉλκΈ°μ κ°λμ΄ λμ΄.

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%203.png)

    [https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s](https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s)

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%204.png)

- Sync vs. Async

    λκΈ°μ λΉλκΈ°λ μμμ μννλ μ£Όμ²΄κ° 2κ°μ΄μμ΄ νμ ν©λλ€.

    νκ΅­μ΄, μμ΄, μΌλ³Έμ΄ ν κ²μμ΄ μ΄ κ°λμ λν΄μ  μλ§μ μ€λͺμλ£λ€μ΄ λ§μ΄μμ΅λλ€.

    κ°μ λ μμλ³΄μκ³  μΆμΌμ  λΆλΆμ΄ μμΌλ©΄ κ·Έ λΆλΆμ κ°μ μ°Ύμλ³΄μκΈΈ λ°λλλ€.

    **λκΈ°**λ λ§κ·Έλλ‘ "μμ²­" κ³Ό " κ²°κ³Ό" κ° "λμμ" μΌμ΄λλ€λ λ»μλλ€. 

    μμμ μκ° (μμ, μ’λ£ λ±) μ μλ‘ κ°μ νμ΄λ°μ λ§μΆλ κ²μ λκΈ°λΌκ³  λΆλ¦λλ€.

    νλμ μμ²­μ λν μμμ΄ λͺ¨λ λ€ λλλ©΄, λ§¨ μ²μμ λ°μλ μμ²­ + κ·Έμ λν κ²°κ³Όλ₯Ό μ μΆν λ€, κ·Έ λ€μ μμμ μ€ννκ³ , λ ν΄λΉ μμμ΄ λλλ©΄ κ·Έ λ€μ μμμΌλ‘ λμ΄κ°λκ²μ μμν΄λ³΄λ©΄ λ λ― ν©λλ€. 

    μμ€ν μ€κ³κ° κ°λ¨νκ² μ£ ? λ°©ν΄λ°λ κ²λ μκ³ , μμλλ‘λ§ μ μ§νλλ©΄ λ νλκΉμ. μ§κ΄μ μ΄κ³  κ°λ¨ν μ€κ³λ°©μμ΄ μ₯μ μ΄μ§λ§, νλμ μλ¬΄μ λν κ²°κ³Όκ° μ£Όμ΄μ§ λ κΉμ§ λκΈ°ν΄μΌνλ λ¨μ μ΄ μμ΅λλ€.

    **λΉλκΈ°**λ λ§ κ·Έλλ‘ "μμ²­" κ³Ό "κ²°κ³Ό" κ° "λμμ μΌμ΄λμ§ μλλ€" λ λ»μλλ€.

    μλ‘μ μμμκ°μ΄ κ΄κ³ μλ€λ©΄ μ΄λ₯Ό λΉλκΈ°λΌκ³  λΆλ¦λλ€.

    λ°μ μμΉ¨μΆκ·Ό μ€λΉλ₯Ό μκ°νλ©΄ λ©λλ€. μ€μνλ©΄μ μμΉνκ³ , μλ³΅ μμΌλ©΄μ μμΉ¨ κ°λ¨νκ² λ¨Ήλ κ±°λ λΉμ·ν λλμ΄μ§μ. νλμ μμμ λλ €λκ³ , κ·Έ μ¬μ΄μ λ€λ₯Έ μμλ μ€νν΄λλ λ©ν°νμ€νΉμ μκ°ν΄λ³΄λ©΄ μ΄ν΄νκΈ° μ½μ΅λλ€.

    μμΉ¨ μΆκ·Όμ μκ°νλ€λ©΄, λΉλκΈ°μ μμ€ν μ€κ³λ μ μ§ λͺ¨λ₯΄κ² λ³΅μ‘ν  κ² κ°μ΅λλ€. λμμ μ¬λ¬κ°μ§ μ²λ¦¬κ° νμνλκΉμ. κ²°κ³Όκ° μ£Όμ΄μ§λλ° μκ°μ΄ κ±Έλ¦¬λλΌλ, κ·Έ μ¬μ΄μ μκ°μ΄ μΌλ§ κ±Έλ¦¬μ§ μλ λ€λ₯Έ μμμ ν  μ μμΌλ―λ‘, νμ λ μμμ ν¨μ¨μ μΌλ‘ μ¬μ©ν  μ μμ κ²λλ€.

- Blocking vs. Non-blocking

    λ€λ₯Έ μμμ μννλ μ£Όμ²΄λ₯Ό μ΄λ»κ² μλνλμ§κ° μ€μν©λλ€. 

    μμ μ μμμ νλ€κ° λ€λ₯Έ μμ μ£Όμ²΄κ° νλ μμμ μμλΆν° λκΉμ§ κΈ°λ€λ Έλ€κ°, λ€μ μμ μ μμμ μμνλ©΄ λΈλ‘νΉμ΄λΌ νκ³ , λ€λ₯Έ μ£Όμ²΄μ μμκ³Ό κ΄κ³μμ΄ μμ μ μμμ κ³μνλ€λ©΄ μ΄λ₯Ό λΌλΈλ‘νΉ.

    λκΈ° (Sync)μμ λ³΄μλ―, νλμ μμμ΄ λλ  λ κΉμ§ κΈ°λ€λ¦°λ€ β Blockingλμ΄μλ€.

    λΉλκΈ° (Async)λ μ¬λ¬ μμμ΄ λμμ μΌμ΄λλ€. λλ  λ κΉμ§ κΈ°λ€λ¦¬μ§ μμΌλ, Non-Blockingμ΄ λλ€.

    Blockingλμ§ μλλ€λ κ²μ μλ―Έλ, μ€νλμ΄μ§λ κ°κ°μ μμλ€μ νμ λ£κ±°λ λ€λ₯Έ μ€λ λμκ² ν΄λΉ taskλ₯Ό λ§‘κΈ°κ³  λ€λ₯Έ μ½λ λ° μμμ μ€ννλ€λ μλ―Έ.

    ![Untitled](CS%20Interview%20Preparation%2051175a268e744a6dab12bbc6e257055b/Untitled%205.png)

    Reference: [https://deveric.tistory.com/99](https://deveric.tistory.com/99)

## π Reference

---

1. Website
    1. [https://www.outsystems.com/blog/posts/asynchronous-vs-synchronous-programming/](https://www.outsystems.com/blog/posts/asynchronous-vs-synchronous-programming/)
    2. [https://evan-moon.github.io/2019/09/19/sync-async-blocking-non-blocking/](https://evan-moon.github.io/2019/09/19/sync-async-blocking-non-blocking/)
    3. [https://juyeop.tistory.com/22](https://juyeop.tistory.com/22)
    4. [https://private.tistory.com/24#:~:text=λκΈ°μ λΉλκΈ°λ μ΄λ€,μκ³ %2C λμμ μ΄λ£¨μ΄μ§μ§λ μμ΅λλ€](https://private.tistory.com/24#:~:text=%EB%8F%99%EA%B8%B0%EC%99%80%20%EB%B9%84%EB%8F%99%EA%B8%B0%EB%8A%94%20%EC%96%B4%EB%96%A4,%EC%9E%88%EA%B3%A0%2C%20%EB%8F%99%EC%8B%9C%EC%97%90%20%EC%9D%B4%EB%A3%A8%EC%96%B4%EC%A7%80%EC%A7%80%EB%8F%84%20%EC%95%8A%EC%8A%B5%EB%8B%88%EB%8B%A4).
    5. [https://www.youtube.com/watch?v=m0icCqHY39U](https://www.youtube.com/watch?v=m0icCqHY39U)
    6. [https://www.youtube.com/watch?v=U42qWURR6Gw](https://www.youtube.com/watch?v=U42qWURR6Gw)
    7. [https://www.inflearn.com/course/sync-async-κ°λ-μ΄ν΄/lecture/33682?tab=curriculum](https://www.inflearn.com/course/sync-async-%EA%B0%9C%EB%85%90-%EC%9D%B4%ED%95%B4/lecture/33682?tab=curriculum)
    8. [https://www.youtube.com/watch?v=IdpkfygWIMk](https://www.youtube.com/watch?v=IdpkfygWIMk)
    9. [https://deveric.tistory.com/99?category=387263](https://deveric.tistory.com/99?category=387263)
    10. [https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s](https://www.youtube.com/watch?v=zRJOte7TaPw&t=155s)