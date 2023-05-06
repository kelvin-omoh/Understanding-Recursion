# RECURSION

## <u> Outline</u>
1. Keypoint.
2. Introduction.
2.1 What is recursion.
2.2 Example.
2.3 Basic structure of a recursive function.
2.4 How does recursion work.
3. Illustration.
3.1 Example.
4. Exercise.
5. Conclusion.

## key Point
- **<u>Base case (stopping case):</u>** Its a part of the recursion , where the condition  evaluates the current inputs and terminates the recursive function.

- **<u> Recursive case:</u>** Its a part of the recursive function, where the function calls on itself.

## Introduction
A function in programming is an important concept that consist of  the function definition, function declaration, function body, etc. In this article, to learn about recursion, we need to understand the concept of loops (e.g For Loop ), Fuctions, Control Statements (If...else). A ==Recursive== function is a particular function that calls itself repeatedly until a certain condition is met . And we will also understand its working in details.

### What is Recursion ?
==Recursion== is a programming technique where a ***function calls itself***, either directly or indirectly, in order to solve a problem.Recursion is a common technique used in divide and conquer algorithms.Using a recursive algorithm, certain problems can be solved quite easily. Examples of such problems are Towers of Hanoi (TOH), Inorder/Preorder/Postorder Tree Traversals, DFS of Graph, etc. Recursive texts defines a problem (or the solution to a problem) in terms of (a simpler version of) itself.

### Example 1
How would you write a recursive "algorithm" for   <span style="color:blue">  finding the location of My House?</span> 
```php
  Function "Find My House":

            1) Ask Someone which way to go.  (they point "that away"),
            2) Move "that way" until you get to the street,
            3) Find My House.
```

### Basic structure of a recursive function
```js #33
Function recursion (){
     
     recursion() // recursive call

}

recursion() //function call

```

### How does recursion work

==Recursive fuction== calls it self until a base condition is true to produce the correct output. In other words,like the example i gave earlier 
```php
 Function "Find My House":

            1) Ask Someone which way to go.  (they point "that away"),
            2) Move "that way" until you get to the street,
            3) Find My House.
```

**The Problem** <u><span style='color:blue'>" Find my house" </span></u> is futher reduced to a smaller instance of the problem, and the the solutions ( "Ask Someone which way to go" ,"Move that way until you get to the street", <span style='color:blue'>" Find my house" </span>) and the solutions to the smaller instances  are used to solve the original problem. In other other words, to solve a problem ,we solve a problem that is a smaller instance of the same problem, and then use the solution to that smaller instance to solve the original problem.


## Illustration

[<img src="https://isaaccomputerscience.org/api/v3.5.0/api/images/content/computer_science/programming_fundamentals/recursion/figures/isaac_cs_prog_recurs_trace_sum.svg" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" >](https://isaaccomputerscience.org/concepts/prog_recurs_basics?examBoard=all&stage=all)

### Example 2
Find the factorial of 5 .

> **Factorial** of 5 is 5!= "1 * 2 * 3 * 4 * 5" = ***120*** .

```js #71-73


const Factorial=(x)=>{

    if (x == 1){ // This is the base case
      return 1;
    }
    
          
      else{  // This is the recursive case
          return(x * Factorial(x-1));
      } 
  
  }
  const Output= Factorial(5);
  
  console.log(Output); //Printing out the ' output ' of the recursion

```


## Exercise

<details markdown='1'>
<summary>
Write a <b><i>recursive function</i></b> that will sum all numbers from   <b><i>1 to n. </i></b><br>
<u><b>Note:</b></u> Take <b>n</b> as the argument in the function
</summary>

<u>solution :</u>
```js
Function findMin(Arr,n){

    if(n == 1){
      return Arr[0];
    }

    else{
        return min(Arr[n-1],findMin(Arr,n-1));
    }
      

}
    
 
A = [1, 4, 24, 17, -5, 10, -22] ;
n = len(A);

print(findMin(A,n));
```

</details>

## Conclusion
A control statement (if...else) should be used to terminate an infinite recursion, setting a condition ***(baseCase)***   stops the program.
