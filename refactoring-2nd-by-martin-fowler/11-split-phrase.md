# 11. Split Phrase

1. Extract the second phase code into its own function.
2. Test.
3. Introduce an intermediate data structre as an additional argument to the extracted function.
4. Test.
5. Examine each parameter of the extracted second phase. If it is used by first phase, move it to the intermediate data structure. Test after each move.
6. Apply *Extract Function* on the first-phase code, returning the intermediate data structure.

- 코드 구현부가 지나치게 길고 복잡해지는 것을 막기 위해, 의미단위로 봤을 때 독립적으로 떼어내도 되는 과정의 코드는 함수로 분리하여 연결한다.
- 분리한 함수의 파라미터 개수를 줄이기 위해 최대한 자료구조를 사용한다. 