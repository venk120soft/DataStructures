# Recursion
Two essential parts of a recursive function!
- Base Case (A situation when the recursion should end)
- Different Input 

Ex:
```javascript
// Recursive Version
function countDown(num){
    // Base case
    if(num <= 0) {
        console.log("All done!");
        return;
    }
    console.log(num);
    num--;
    countDown(num);
}
countDown(3)

// Iterative Version
function countDown(num){
    for(var i = num; i > 0; i--){
        console.log(i);
    }
    console.log("All done!")
}
```
