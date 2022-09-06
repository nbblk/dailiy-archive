# 13. Encapsulate Collection

> Modifications aren't always obvious; for example, sorting an array in JavaScript modifies the original, while many languages default to making a copy for an operation that changes a collection. Any class that's responsible for managing a collection should always give out copies - but I also get into the habit of making a copy if I do something that's liable to change a collection.

1. Apply *Encapsulate Variable* if the reference to the collection isn't already encapsulated.
2. Add functions to add and remove elements from the collection. If there's a setter for the collection, use *Remove Setting Method* if possible. If not, make it take a copy of the provided collection.
3. Run static checks.
4. Find all references to the collection. If anyone calls modifiers on the collection, change them to use the new add/remove functions. Test after each change.
5. Modify the getter for the collection to return a protected view on it, using a read-only proxy or a copy.
6. Test.