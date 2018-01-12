
Layout: 
Title: "No Repeats Please"
Date: "2018-01-10 12:13"
Categories:

# No Repeats Please

The excise I was given on freecodecamp was a difficult one and I used an if statement and use .push  but it didn't work and also tried to use .pop so that I can be able to arrage the string I was given and they all didn't work. I got to understand it better after I read about heap's algorithm. 

## Problem

Return the number of total permutations of the provided string that don't have repeated consecutive letters. Assume that all characters in the provided string are each unique.

For example, aab should return 2 because it has 6 total permutations (aab, aab, aba, aba, baa, baa), but only 2 of them (aba and aba) don't have the same letter (in this case a) repeating.

## Approach

I fistly splited the string to give an array, I then had a regex which matches all the characters which will match the first value and the ones which follow. An if statement to chack if the regex matches and if not should return null and return 0 if str contains same character.

A function to swap variables' content, then generate arrays of permutations using the algorithm and make sure to join the characters as we create the permutation arrays. Lastly filter the array of repeated permutations and return how many have no repetitions.

