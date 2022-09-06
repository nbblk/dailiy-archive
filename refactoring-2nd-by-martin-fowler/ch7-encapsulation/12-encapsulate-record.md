# 12. Encapsulate Record
=> Replace Record with Data Class

> I can have two kinds of record structures: those where I declare the legal field names and those that allow me to use whatever I like. The latter are often implemented through a library class called something like hash, map, hashmap, dictionary, or associative array. ... The downside of using them is they are not explicit about their fields. 
1. Use *Encapsulate Variable* on the variable holding the record.
2. Replace the content of the variable with a simple class that wraps the record. Define an accessor inside this class that returns the raw record. Modify the functions that encapsulate the variable to use this accessor.
3. Test.
4. Provide new functions that return the object rather than the raw record.
5. For each user of the record, replace its use of a function that returns the record with a function that returns the object. Use an accessor on the object to get at the field data, creating that accessor if needed. Test after each change.
6. Remove the class's raw data accessor and the easily searchable functions that returned the raw record.
7. Test.
8. If the fields of the record are themselves structures, consider using *Encapsulate Record* and *Encapsulate Collection* recursively.

- 클래스 설계 시 언제나 원본 대신 복사본을 반환하는 접근제어자를 사용할 것.