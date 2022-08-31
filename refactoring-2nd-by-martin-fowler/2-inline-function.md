# 2. Inline Function

> I commonly use Inline Function when I see code that's using too much indirection-when it seems that every function does simple delegation to another function, and I get lost in all the delegation.

1. Check if the function isn't a polymorphic method which can be overrided by subclasses.
2. Find all the callers of the function.
3. Replace each call with the function's body.
4. Test after each replacement.
5. Remove the function definition.

- 함수로 추출하느니 구현부를 그냥 사용하는 게 더 의미 전달이 명확한 경우가 있다.
