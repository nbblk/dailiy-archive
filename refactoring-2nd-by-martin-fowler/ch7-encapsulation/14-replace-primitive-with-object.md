# 14. Replace Primitive with Object

> At first, such a class does little more than wrap the primitive-but once I have that class, I have a place to put behavior specific to its needs. These little values start very humble, but once nurtured they can grow into useful tools. They may not look like much, but I find their effects on a code base can be surprisingly large. Indeed many experienced developers consider this to be one of the most valuable refactorins in the toolkit-even though it often seems counterintuitive to a new programmer.

1. Apply *Encapsulate Variable* if it isn't already.
2. Create a simple value class for the value. It should take the existing value in its constructor and provide a getter for that value.
3. Run static checks.
4. Change the setter to create a new instance of the value class and store that in the field, changing the type of the field if prsent.
5. Chnage the getter to return the result of invoking the getter of the new class.
6. Test.
7. Consider using *Rename Function* on the original accessors to better reflect what they do.
8. Consider clarifying the role of the new object as a value or reference object by applying *Change Reference to Value* or *Change Value to Reference*.

- primitives를 위한 클래스를 만들고, 특정 데이터의 유효성 검사나 비교를 위한 메소드를 추가하는 게 과연 유용할까?? 읽으면서도 별로 와닿지 않음 