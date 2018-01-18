---
Layout:
Title: "Permutations using for loop"
Date: 2018-01-16 08:58
Categories:
---

# Permutations using for loop

The excise I was given was to return the number of total permutations of the provided string that don't have repeated consecutive letters and I should assume that all characters in the provided string are each unique.
For example, aab should return 2 because it has 6 total permutations (aab, aab, aba, aba, baa, baa), but only 2 of them (aba and aba) don't have the same letter (in this case a) repeating.

## How I solve the problem

firstly I needed to understand what is permutation inorder for me to solve this excise I was given. Permutation means each of several possible ways in which a set or number of things can be ordered or arranged in sequence. 

I followed a heap algorithm to solve this problem as it was giving me challenges and it was complex, here is a link to look up for the algorithm: https://en.m.wikipedia.org/wiki/Heap%27s_algorithm . In this algorithm it shows that there are two ways to solve this complex problem which is using recursion and you can use a for loop. I used a for loop and it worked for me and even recursion worked.

I had a function which takes two parameters and in the paremeters one of them I made it as a default. Assigned results and c as empty arrays, whenever a new array is created should be placed in these empty arrays.

A for loop which will iterate through each an every character and variable c at index i should be 0, assigned i to be zero and followed by a while loop which checks if i is less than n( n is our lenght of the given string). An If statement to check if c at index i is less than i and if i is even and strickly equal to zero, if thats the case I created a variable called splitted so that I split the string and I swapped the characters. If they are not even it should swap the other ones which are not even.

 if (i % 2 === 0) {
                var splitted = a.split('');
                const temp0 = splitted[0];
                const tempi = splitted[i];
                splitted[0] = tempi;
                splitted[i] = temp0;
                a = splitted.join('');

            } else {
                var splitted = a.split('');
                const temp0 = splitted[c[i]];
                const tempi = splitted[i];
                splitted[c[i]] = tempi;
                splitted[i] = temp0;
                a = splitted.join('');
            }
        results.push(a);
        }

After it has pushed the new array which is swapped it will then append one if c index i is equal to 0 then it will append 1 on i which is equal to zero. 

A function which checks for the matching letters then filtering the ones which are repeating, using regex and return the length of the letters.

     var permutation = results.filter(function(letters){
     return !letters.match(/(.)\1+/g);
  });
                                        
                                         
return permutation.length
  

## Conclusion

 What I have learned about the exices is that when even you stuck take it slow and read through the algorithm as many times as possible and compare the algorithm with your code. Because I made a lot of mistakes on my code which was very simple but because I didn't keep on checking the algorithm that is why I made those mistakes.
