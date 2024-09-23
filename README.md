# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];             // This line tests if the argument 'a' is a single element, if it is it returns the first/only element.
    var foo = mystery(a.slice(1, a.length))    // This recursive step "loops" until there is only one element in 'a' (the last element of the original 'a'), which is assigned to foo.
    if(foo > a[0]) return foo;                 // This line compares the current foo value to a new element, if foo is the larger value it returns foo.
    else return a[0];                          // If foo was less or equal to 'a' then 'a' is returned.
}

var arr = [1, 9, 3, -2, 27, 0, 15, -30];
arr = mystery(arr);
console.log(arr);

// This function recursively iterates through a given array (or string) until the last element is reached. At which point it returns the last element
// of the initial 'a' to the prior recursion as 'foo', which then compares 'foo' (the last element) to the first element of the prior 'a'.
// This cycle repeats until the largest value in the array/string is found.
```
