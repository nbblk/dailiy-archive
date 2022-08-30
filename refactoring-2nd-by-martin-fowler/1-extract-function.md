# 1. Extract Function

> The argument that makes most sense to me, however, is the separation between intention and implementation. **If you have to spend effort looking at a fragment of code and figuring out _what_ it's doing**, then you should extract it into a function and name the function after the "what." Then, when you read it again, the purpose of the function leaps right out at you, and most of the time you won't need to care about how the function fulfills its purpose (which is the body of the function).

1. Create a new function and name it by what it does, not by how it does.
2. Copy the extracted code from the source function into the new target function.
3. Scan the extracted code whether any variables are in the scope for the extracted function. If not so, pass the variables as parameters.
4. Compile
5. Replace the extracted code with a call to the target function.
6. Replace the duplicate code with the new function call.

- 함수 이름이 그 자체로 자기설명적(무엇을)이어서, 구현부(어떻게)를 들여다보지 않아도 뭘 하는 함수인지 알 수 있어야 한다.
- 추출한 코드가 원래 있던 자리 기준 지역 변수를 참조할 경우, 파라미터로 그 변수를 전달받을 수 있게 해주어야 한다.
- 함수 반환값을 변수에 재할당해야 하는 경우, 헷갈리지 않도록 함수 내부적으로 쓰는 변수명과 바깥(재할당할) 변수명은 다르게 쓴다.
