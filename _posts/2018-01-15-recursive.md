---
Layout: 
Title: "Recursive Method"
Date: 2018-01-15 13:00
Categories:
---

# Recursive Method

Recursive is an iteration over an operation by having a function call itself repeatedly until it arrives at a result.

Recursion is best applied when you need to call the same function repeatedly with different parameters from within a loop. While it can be used in many situations, it is most effective for solving problems such as sorting. Recursive is the most direct way to solve complex promblems

 ## Example of Recursive function

The classic example of a function where recursion can be applied is the factorial. This is a function that returns the value of multiplying a number again and again by each preceding integer, all the way down to one.

  Factorial of 5!

   5 =|_ factorial (4) 
    4 =|_ factorial (3) 
        3 =|_ factorial (2) 
            2 =|_ factorial (1) 
                1 =|_ factorial (0) 

function factorial(n){
    if(n < 1){
        return 1;
    }else{
        return n * factorial(n - 1);
    }
}

## Conclusion

Recursive function it is a good way to solve all the complex problems you facing also sorting out any letter or numbers which are big and uncounterble but with recursive you able to get it quick and I got to understand how each an every iteration is calculated more especially with the factorial example and there was a an excise where were given on freecodecamp it was about permutaion and I was very stuck but after I used recursive function it really helped and I got to understand.