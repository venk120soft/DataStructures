# DataStructures
- Javascript all methods will start with small letter ex: 'Hello'.length
- C# all mthods will start with capital letter ex: 'Hello'.Length

### What is Datastructure?
Different ways of storing data in computer. A data structure is a particular way of organizing data in a computer so that it can be used effectively

## Types of Datastructures
- Array
- Linked List
- Stack (LIFO)
- Queue (FIFO)
- HashTable
- HashMap
- Heap
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
- push => add new element to end of stack 
- pop => remove element from end of stack and return it
- top => return top element of a stack  after pop out the element 

Best example is: stacking the plates one on other. ex2: reverse string, ex3: Balanced paranthesis

=> Queue is First in First Out (FIFO) => first element is the first to pop out. we can use push and shift operations
- enqueue => Add new element to the end of queue
- dequeue => remove element from starting of the queue
- getFrontElement => after removal get the first element in queue

Best example is: queue line infront of shopping mall, ex2: find binary value of a given number

## Hashtable
Hashtable data structure having the key and value pair with hash function. This is similar to the Object. We can implement the Hashtable using Object in Javascript but there are some caveats with this approach like we can overwrite the default properties defined for the object hence it is not the right way of implementation

For this Reason, javacript have another [implementation](./hashtable.js) of hashTable with Map. 

A Hash Table transforms a key into an integer index using a hash function, and the index will decide where to store the key/value pair in memory:
[more info JS](https://www.freecodecamp.org/news/javascript-hash-table-associative-array-hashing-in-js/) | [more info C#](https://www.tutorialsteacher.com/csharp/csharp-hashtable)

- Hashtable is not generic hence while accessing the elements we need to do type casting
- If the key is not found in HashTable it will return undefined(in javascript) and null (in C#)

#### In Short: Its a technique to convert a range of key values into a range of indexes of an array. 

Hashfunction help us to generate the uniq index (by using ASCII values) then we convert key and value as an array and pass this as value and uniqIndex as a Key.
```javascript
const hashTable =  {
      uniqIndex:[key, vlaue],
      uniqIndex1:[key, vlaue],
      uniqIndex2:[key, vlaue]
  }
// uniqIndex will generated by using the hash function
 const _hash = (key:any) =>  {
    let hash = 0;
    for (let i = 0; i < key.length; i++) {
      hash += key.charCodeAt(i); // getting the ASCII number
    }
    
     // return hash; // we can also written the hash here but due to the JS limitation reason below
     // But since the HashTable class only has 127 buckets, this means that the _hash() method must return a number between 0 and 127.
     // To ensure that the hash value doesn't exceed the bucket size, you need to use the modulo operator as shown below:
    return hash % this.table.length;
  }
```
