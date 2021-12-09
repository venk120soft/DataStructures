# DataStructures
- Javascript all methods will start with small letter ex: 'Hello'.length
- C# all mthods will start with capital letter ex: 'Hello'.Length

### What is Datastructure?
Different ways of storing data in computer. A data structure is a particular way of organizing data in a computer so that it can be used effectively

## Types of Datastructures
- Array
- Linked List
- HashTable
- HashMap
- Heap
- Stack (LIFO)
- Queue (FIFO)
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
- LinkedList: LinkedList will be formed with the list of nodes. Each node have Data, address of previous node and adrress of next next node. it is a doubly linked list. and it is strongly typed Add/Remove will be easy O(1). but retrival takes long time as it has to go through all the elements
```javascript
LinkedList<string> sentence = new LinkedList<string>(words);
sentence.AddFirst("today");
```

## Stack(LIFO) and Queue(FIFO) can be easily implemented using the Arrays

Arrays have below operations:
- push => add new element to end of an array
- pop => delete element from an end of an array
- shift => delete element from start of an array. which first element

=> Stack is Last In First Out (LIFO) => last element is the first to pop out. we can use push and pop operations

Best example is: stacking the plates one on other. ex2: reverse string, ex3: Balanced paranthesis

=> Queue is First in First Out (FIFO) => first element is the first to pop out. we can use push and shift operations

Best example is: queue line infront of shopping mall, ex2: find binary value of a given number
