# 5. Change Function Declaration

1) Simple Mechanics
- Check if a parameter is not being used in the body of the function.
- Change the method declaration to the desired one.
- Find all references and update them to the new one.
- Test

2) Migration Mechanics
- Refactor the body of the function first.
- Extract function to create a new function.
- If the extracted function needs additional parameters, use the simple mechanics to add them.
- Test.
- Inline function to the old function.
- Change function declaration again if you used a temporary name.

- Migration Mechanics에서 함수 선언부(함수명, 파라미터)를 바꾸는 단계를 이렇게까지 복잡하게 쪼개야되는지..? 의문이었다.
-  예시 중 기존 함수의 파라미터(객체)를 그 객체의 특정 속성으로 변경하는 게 있었는데, 어떤 식으로 고치냐면,
- 일단 파라미터로 넘기는 객체의 속성을 구현부에서 변수로 추출 함.
- 그리고 구현부에서 그 변수가 쓰이는 부분을 새로운 함수로 추출을 하고 다시 돌아와서 찾기 쉬운 이름을 짓는다. (원래대로 되돌려야 하니까)
- 추출한 함수에 들어가던 파라미터 변수를 다시 인라이닝함.
- 함수 호출부를 다 새 함수 선언부로 교체
- 선언부에서 파라미터만 남기고 원래 함수명으로 교체.
- 이 때 파라미터는 이미 객체가 아닌 객체 속성을 받는 것으로 바뀐 상태.
- 끝! 뭔 소린지 이해하는 데 한 시간 걸렸다. 과연 이 방식을 쓸 일이 있을까