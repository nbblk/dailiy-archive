# 16. Extract Class

1. Decide how to split the responsibilities of the class.
2. Create a new child class to express the split-off responsibilities. Rename the parent class if the responsibility doesn't match.
3. Create an instance of child class when constructing the parent and add a linke from parent to child.
4. Use *Move Field* on each field you wish to move. Test after each move.
5. Use *Move Function* to move methods to the new child. Start with lower-level methods. Test after each move.
6. Decide whether to expose the new child. If so, consider applying *Change Reference to Value* to the child class.

- 클래스가 커지면 그 안에서 또 다른 클래스를 추출해 책임을 분산시킬 필요가 있다.
- 언제 추출할 것인가가 문젠데, 어떤 데이터의 하위 데이터 집합들이 서로 의존하거나 같이 변하는 경우, 아니면 어떤 데이터 하위집합과 메소드의 하위 집합이 같이 붙어있는 경우에 클래스로 분리하면 좋다.
- 예시에서는 Person 클래스의 constructor에서 멤버변수 telephoneNumber를 미리 추출해둔 TelephoneNumber 클래스의 인스턴스로 초기화하고, 인스턴스를 통해 TelephoneNumber의 데이터에 접근하고 있음. 근데 정말 값만 받아오기 위한 클래스가 돼버리면 그냥 *Change Reference to Value*를 사용해서 Value Object로 바꾸는 게 낫다.