# 6. Encapsulate Variable

> So if I want to move widely accessed data, often the best approach is to first encapsulate it by routing all its access through functions. That way, I turn the difficult task of reorganizing data into the simpler task of reorganizing functions. ... It is my habit to make all mutable data encapsulated like this and only accessed through functions if its scope is greater than a single function. The greater the scope of the data, the more important it is to encapsulate. ... Taking a copy maby be superfluous most of the time, but copies in these cases usually have a negligible effect on performance; on the other hand, if I don't do them, there is a risk of a long and difficult bout of debugging in the future.

1. Create encapsulating functions to access and update the variable.
2. Run static checks
3. Replace each references with a call to the encapsulating function.
4. Test after each replacement.
5. Restrict the visibility of the variable.
6. Test.
7. If the value is a record, consider _Encapsulate Record_.

- 변수 캡슐화는 접근제어자로 하고, 그 변수에 담긴 가변 데이터의 불변화는...
- Object.assign(), consturctor method, spread operator, JSON methods(JSON.stringify() & JSON.parse())로 시도해볼 수 있다.
- 하지만 이들은 속성값이 원시타입 뿐인 플랫한 객체는 깊이 복사하지만, 중첩객체처럼 속성값이 참조타입이라면 최상위 객체를 제외하고는 원본을 그대로 가리키는 얕은 복사가 이루어지거나
- JSON methods의 경우 중첩객체도 한 번에 깊은 복사가 가능한듯 보이지만, 그럼에도 stringify를 통해 직렬화하기 애매한 타입 혹은 값(Date, undefined, Infinity)이 있으므로 주의를 요함.
