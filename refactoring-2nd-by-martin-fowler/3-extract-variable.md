# Extract Variable

> If I'm considering Extract Variable, it means I want to add a name to an expression in my code. ... If it's only meaningful within the function I'm working on, then Extract Variable is a good choice-but if it makes sense in a broader context, I'll consider making the name available in in that broader context, usually as a function.

1. Ensure that the expression that you want to change into a variable does not have any side effects.
2. Declare an immutable variable and set it to a copy of the expression you want to name.
3. Replace the original expression with the new variable
4. Test

- 표현식을 적절히 변수로 추출하는 것은 가독성 향상과 더불어 같은 표현식을 거듭 사용하지 않는 데 도움을 준다.
- 변수로 추출하는 것보다, 아예 해당 표현식에 대한 값을 반환하는 명확한 이름의 함수로 만드는 게 더 적절한 경우가 있다. 예를 들어, Order라는 클래스에 (1)제품 가격에 수량을 곱한 값에서 (2)수량 할인가와 (3)배송비를 뺀 값을 반환하는 price()라는 get메소드가 있다면, (1)-(3)을 basePrice(), quantityDiscount(), shipping()이라는 get메소드로 만들면 price()를 보다 쉽고 명확하게 만들 수 있다.  