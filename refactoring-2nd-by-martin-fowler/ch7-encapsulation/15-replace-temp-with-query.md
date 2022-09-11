# 15. Replace Temp with Query

1. Check that the variable is determined entirely before it's used, and the code that calculates it does not yield a different value whenver it is used.
2. If the variable isn't read-only, and can be made read-only, do so.
3. Test.
4. Extract the assignment of the variable into a function. (use const)
5. Test.
6. Use *Inline Variable* to remove the temp.

- 표현식 결과를 저장하기 위한 임시 변수를 함수로 만든다. 
- 즉 결과를 반환하는 함수로 변환했을 때의 장점은 코드 재사용이 가능하다는 점 + 임시 변수일 때보다 추출 로직과 함수의 경계가 더욱 명확해져서 불필요한 의존성이나 side effects를 빨리 찾을 수 있다. 
- 하지만 임시 변수를 죄다 함수화할 필요는 없다. 한 번 쓰이는 표현식은 변수를 사용하는 게 낫고, 그래서 주로 클래스 메소드 정의 시 이 방법이 자주 쓰임.
