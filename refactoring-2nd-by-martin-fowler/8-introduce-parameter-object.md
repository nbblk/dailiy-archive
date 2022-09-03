# 8. Introduce Parameter Object

1. If there isn't a suitable structure already, create one. (value object or class)
2. Test
3. Use _Change Function Declaration_ to add a parameter for the new structure.
4. Test.
5. Adjust each caller to pass the correct instance of the new structure.
6. Replace the use of the original parameter with the element of the structure. Remove the parameter and test.

- 파라미터가 세 개 이상이면 하나의 파라미터 객체를 만드는 것을 고려. 그냥 객체보다는 값을 초기화하고 내부 변수에 대한 접근 제어 메소드만 있는 Value Object로서의 클래스를 처음에 만들고, 점진적으로 필요한 메소드를 추가하는 것을 권장.
