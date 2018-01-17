---
Layout:
Title: "Permutations using for loop"
Date: 2018-01-16 08:58
Categories:
---

# Permutations using for loop

I had a function which takes two parameters and in the paremeters one of them I made it as a default. Assigned results and c as empty arrays, whenever a new array is created should be placed in these empty arrays.

A for loop which will iterate through each an every character and variable c at index i should be 0, assigned i to be zero and followed by a while loop which checks if i is less than n(is our lenght of the given string). An If statement to check if c at index i is less than i and if i is even and strickly equal to zero, if thats the case I created a variable called splitted so that I split the string and I swapped the characters. If they are not even it should swap the other ones which are not even.

 }if (i % 2 === 0) {
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

After it has pushed the new array which is swapped it will then append one 1 else if c index i is equal to 0 that it will append 1 on i which is equal to one(1). 

A function which checks for the matching letters then filtering the ones which will check for repeating and filter them them out, using regex and return the length of the letters.

     var permutation = results.filter(function(letters){
     return !letters.match(/(.)\1+/g);
  });
                                        
                                         
return permutation.length
  



## Conclusion

 What I have learned about the exices is that when even you stuck take it slow and read through the algorithm as many times as possible and compare the algorithm with your code. Because I made a lot of mistakes on my code which was very simple but because I didn't keep on checking the algorithm that is why I made those mistakes.
