# 19. Remove Middle Man

1. Create a getter for the delegate.
2. For each client use of a delegating method, replace the call to the delegating method by chaining through the accessor. Test after each replacement.

- 위임 메소드를 없애고 해당 데이터에 직접 접근하도록 바꾼다.
- 얼마나 캡슐화하는 게 적정한지는 코드 짜고 한 6개월 지나면 알 수 있다. 