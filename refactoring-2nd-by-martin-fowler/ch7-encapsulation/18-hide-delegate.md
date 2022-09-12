# 18. Hide Delegate

1. For each method on the delegate, create a simple delegating method on the server.
2. Adjust the client to call the server. Test after each change.
3. If no client needs to access the delegate anymore, remove the server's accessor for the delegate.
4. Test.

- 위임 메소드를 두는 캡슐화의 장점: 내부 코드의 변화가 생겨도 호출하는 입장에서는 신경쓰지 않아도 된다.
- 예를 들어 부서에 대한 정보를 aPerson.department.manager 를 통해 얻을 것 같으면, department이라는 클래스 인스턴스에서 manager를 갖고있다는 게 노출되므로, Person 클래스에서 manager를 대신 반환하는 위임 메소드인 get manager()를 정의하면 aPerson.manager로 외부에서 호출하기만 하면 되고. 결합도도 낮출 수 있음.
