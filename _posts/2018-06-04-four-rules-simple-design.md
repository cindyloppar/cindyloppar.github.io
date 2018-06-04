---
Layout: 
Title: "Four Rules Of Simple Design"
Date: 2018-06-04 08:30
Categories:
---


# Four Rules of Simple Design 

* 1. Tests pass
* 2.Expresses Intent
* 3.No Duplication(DRY)
* 4.Small

The four rules of simple designs was written by Kent back, The important thing about these rules is that they iterate over each other.Frequently, fixing a naming issue will uncover some duplication.
Eliminating that duplication will then reveal some expressiveness that can be improved.   

## Tests Pass

It is important to verify if your system work, therefore it will determine your great design. The tests are automated. The tests pass it is about the correctness and verification, it can be a significant of making changes.

"If you have to ask how fast your test suite should be, it should be faster".

## Expresses Intent

The naming has to be effectively express their intent for one to understand and the code should be readable. If the structure gets large as we write our code, it should always be refactored.

## No Duplication (DRY)

"Do not repeat yourself"

The DRY principle states "Every piece of knowledge should have one and only one representation" 

It helps with the amount of code that we write. Remove duplication and improving names helps in reducing the liability of th code.

## Small

"Once we've applied the above rules, it is important to look back and make sure that you dont have any extraneous pieces"

One should read the code once more and ask themselves question if they have duplicate abstractions, make sure the code is refactored and check for similar characteristics, perhaps a behavior.