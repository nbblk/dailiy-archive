# Inline Class

1. In the target class, create functions for all the public functions of the source class. These functions should just delegate to the source class.
2. Change all references to source class methods so they use the target class's delegators instead. Test after each change.
3. Move all the functions and data from the source class into the target, testing after each move, until the source class is empty.
4. Delete the source class and hold a short, simple funeral service.

- 새로 만든 클래스가 너무 없다시피 한 책임을 지고 있다던지, 리팩토링하려는 두 클래스에서 서로 다른 기능을 갖고 있다면 한 클래스로 합친 다음 새롭게 추출하는 게 빠를 수도 있으므로, 클래스로 추출했던 걸 다시 원래 있던 자리로 되돌린다.
-
-
