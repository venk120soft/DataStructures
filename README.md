# DataStructures

### What is Datastructure?
Different ways of storing data in computer. A data structure is a particular way of organizing data in a computer so that it can be used effectively

## Types of Datastructures
- Array
- Linked List
- HashTable
- HashMap
- Heap
- Stack
- Queue
- Tree
- Graph

## Array vs ArrayList vs List vs LinkedList in C#

- Array: Fixed in size, it is strongly typed. retrive will be O(1) and add/remove needs to shift all the elements
```javascript
int[] evenNums = new int[5];
evenNums[0] = 2;
evenNums[1] = 4;
//evenNums[6] = 12;  //Throws run-time exception IndexOutOfRange

Console.WriteLine(evenNums[0]);  //prints 2
Console.WriteLine(evenNums[1]);  //prints 4
// short syntax
int[] evenNums = { 2, 4, 6, 8, 10}; 
var cities = new string[]{ "Mumbai", "London", "New York" }; 
string[] cities = new string[3]{ "Mumbai", "London", "New York" };
```
- ArrayList: Grow in size by currentSize*1.5(ex: 10 becomes 10 * 1.5=15), it's dynamic so every element treated as an object. retrive will be O(1) and add/remove needs to shift all the elements.
any type elements can be added. on retrival typeCasting (boxing and unboxing) is required
```javascript
// Creates and initializes a new ArrayList.
ArrayList myAL = new ArrayList();
myAL.Add("Hello");
myAL.Add(2.5);
myAL.Add(123);
Console.WriteLine((string)myAL[0]); // 'Hello'
var arlist = new ArrayList(){ 1, "Bill", 300, 4.5f };

//Access individual item using indexer
int firstElement = (int) arlist[0]; //returns 1
string secondElement = (string) arlist[1]; //returns "Bill"
}
```
- List: is implemented on top of the ArrayList. it is strongly typed objects so, on retrival typecasting is not required.  retrive will be O(1) and add/remove needs to shift all the elements.
```javascript
List<int> numbers = new List<int>() { 1, 2, 5, 7, 8, 10 };
Console.WriteLine(numbers[0]); // prints 1
Console.WriteLine(numbers[1]); // prints 2
```
- LinkedList: is having Data, previous pointer and next pointer for the Next element. it is a doubly linked list. and it is strongly typed Add/Remove will be easy O(1). but retrival takes long time as it has to go through all the elements
```javascript
LinkedList<string> sentence = new LinkedList<string>(words);
sentence.AddFirst("today");
```
