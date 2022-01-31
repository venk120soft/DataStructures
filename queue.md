# Queue (FIFO)
Queue is a data structure of type First In First Out Model Ex: Queue line in restuarent. Who ever comes first, that customer will be served first 

```javascript
function Queue(){
  this.elements=[]
}

Queue.prototype.enqueue=(e)=>{
  this.elements.push(e); // Adding elements to end of an array
}

Queue.prototype.dequeue=()=>{
  this.elements.shift(); // Removing first element from an array
}

Queue.prototype.length=()=>{
  return this.elements.length; 
}

Queue.prototype.isempty=()=>{
  return this.elements.length===0; 
}

Queue.prototype.peek=()=>{
  return !this.isempty?this.elements[0]:undefined;  // get the current item at the front of the queue
}

let q= new Queue();
// Adding elements to queue
for(let i=0;i<=5;i++){
  q.enqueue(i);
}

// For getting the first element in the queue
console.log('First person in Queue', q.peek());

// Printing Queue members
while(!q.isEmpty){
  console.log(q.dequeue());
}
```
