---
type: day
title: "Day 5: Limits, Derivatives, Riemann Sums"
tldr: "Day 1 with stuff"
layout: day
permalink: /day5/
lecture_pdfs:
  - static_files/materials/pset1calculus.pdf
  - static_files/materials/pset2calculus.pdf
  - static_files/materials/exam1calculus.pdf
links:
  - link: https://tutorial.math.lamar.edu
    name: "Paul's Online Math Notes"
---

Today, we studied various ideas from calculus, namely limits, derivatives, and Riemann sums.
In addition, we implemented a simple algorithm to calculate the derivative at a point numerically, building up from the definition of the derivative, as follows:

```python
import math

def derivative(function, x):
    h = 1
    guess = 74
    old_guess = 1
    epsilon = 0.001
    num_guesses = 0
    while abs(old_guess - guess) >= epsilon:
        old_guess = guess
        guess = (function(x+h)-function(x))/h
        # print(guess)
        num_guesses += 1
        h = h/10

    print("Number of guesses:", num_guesses)
    return guess

def func(x):
    return math.e**(math.sin(x)*x**2)

print("Derivative of x^2 at 2:", derivative(func, 2))
```

As an extension activity, students were given the task of implementing the Riemann sum in a similar way, which relies more directly on convergent sequences(for those curious, in this case we specifically want [Cauchy Sequences](https://en.wikipedia.org/wiki/Cauchy_sequence))

Note that Paul's Online Math Notes, attached below, is in my opinion the best online resource for learning or reviewing calculus. We referenced this page in class for discussions on infinite sequences, series, derivatives, limits, and many other topics.