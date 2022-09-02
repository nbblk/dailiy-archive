# 7. Rename Variable

1. If the variable is used widely, consider _Encapsulate Variable_.
2. Find all references to the varriable, and change every one.
3. Test

- 함수 내 지역 변수명을 다시 짓는 게 가장 흔하지만, 어떤 변수 scope이 너무 넓어서 온갖 종류의 값이 재할당되고 있는 경우에는, 변수 캡슐화를 먼저 한 다음 그 다음에 이름을 다시 짓는다.
- 상수나 읽기 전용 변수명 다시 짓기: 일단 원래 쓰던 상수는 냅두고 새로운 상수에 원본을 복사해서 쓰다가, 나중에 원래 상수명을 새로운 이름으로 천천히 바꿀 수도 있다.
