# 4. Inline Variable

> But sometimes, the name doesn't really communicate more than the expression itself. 

1. Check that the right-hand side of the assignment is free of side effects.
2. If the variable isn't already declared immutable, do so and test.
3. Find the first reference to the variable and replace it with the right-hand side of the assignment.
4. Test.
5. Repeat replacing references to the variables until you've replaced all of them.
6. Remove the declaration and assignment of the variable.
7. Test.

- 추출한 변수가 해당 표현식에 이름을 붙였다 수준 이상의 의미를 갖지 못하면 차라리 다시 인라이닝하는 게 나을 수도 있다.