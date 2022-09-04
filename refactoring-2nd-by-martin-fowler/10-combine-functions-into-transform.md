# 10. Combine Functions into Transform

> Software often involves feeding data into programs that calculate various derived information from it. These derived values may be needed in several places, and those calculations are often repeated wherever the derived data is used. I prefer to bring all of these derivations together, so I have a consistent place to find and update them and avoid any duplicate logic.

1. Create a transformation function that takes the record to be transformed and returns the same values.
2. Pick some logic and move its body into the transform to create a new field in the record. Change the client code to access the new field.
3. Test
4. Repeat for the other relevant functions.

- data transformation function = 기준 함수들을 조합해서 그 때 그 때 상황에 맞는 정보가 더해진 객체를 생성하기 위한 용도의 데이터 변형용 함수. 
- 