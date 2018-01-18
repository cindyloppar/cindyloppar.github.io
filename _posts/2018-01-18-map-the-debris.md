---
Layout:
Title: "Map the Debris"
Date: 2018-01-18 11:14
Categories:
---

# Map the Debris

Return a new array that transforms the element's average altitude into their orbital periods.

The array will contain objects in the format {name: 'name', avgAlt: avgAlt}.

The radius of the earth is 6367.4447 kilometers, and the GM value of earth is 398600.4418 km3s-2.

## How I solved the problem

For me to understand and be able to solve the exercise I needed to read understand more about Orbital period and to get the formula.

Orbital period
The orbital period is the time a given astronomical object takes to complete one orbit around another object, and applies in astronomy usually to planets or asteroids orbiting the Sun, moons orbiting planets, exoplanets orbiting other stars, or binary stars.

I first harded coded it then I got it correct but the problem with hard coding if it happens they change the object or add more of these object it would give me a problem, that is what I also learned. 

I had an orbitalPeriod Function was also give few variables and their values. I declared a variable called emptyArray which on the later stage I was going to store all the new values I got and the other variable I declared was equal to zero. A for loop which will iterate through the array containing an object.

In my for loop I used the variable I declared at the top which was equal to zero and added the avgAlt inside the object and the earthRadius, declared another variable so that I can get the power of 3 from the value I have added at the top. I calculated the pie and rounded off the final answer after the whole steps with the pie. The last step was to push the new object to the emptyArray I declared at the top. 

The steps of calculations

 adding = averageAltitude[i].avgAlt + earthRadius ;
        var toThePowerOfThree = Math.pow(adding,3) /graditudeMass;
        var square = Math.sqrt(toThePowerOfThree);   
        var pie = 2 * Math.PI;
        var answer = Math.round(pie * square);


## Conclusion

In this exercise a learned more about the ojects and arrays and how to calculate using javascript code though I struggled a little bit but I got to understand and also the formula and calculating it normally before writting code was very helpful. 