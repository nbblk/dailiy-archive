# 9. Combine Functions into Class

1. Apply _Encapsulate Record_ to the common data record that the functions share or use _Introduce Parameter Object_ to create a record to group functions and record structure.
2. Take each function that uses the common record and use _Move FUnction_ to move it into the new class.
3. Each bit of logic that manipulates the data can be extracted with _Extracted Function_ and the nmoved into the new class.

- 미래에 데이터 변경 가능성이 조금이라도 있다면 데이터와 관련 함수를 클래스로 묶어버리는 게 낫다.
