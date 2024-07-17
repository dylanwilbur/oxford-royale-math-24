---
layout: home
---

## Day 1
Intro, Reasoning, and Proofs

[**Day 1 Notes**](static_files/materials/Proofs1.pdf)

## Day 2
Number Theory, Graph Theory, Binomial Coefficients

[**Day 2 Notes**](static_files/materials/Day%202.pdf)

Videos:
[**3Blue1Brown Calculus**](https://www.youtube.com/watch?v=WUvTyaaNkzM&list=PL0-GT3co4r2wlh6UHTUeQsrf3mlS2lk6x)

## Day 3
Python Day + Calculus and Probability

### Materials
[Lec 1 code](static_files/materials/lec1.py)

[Lec 2 code](static_files/materials/lec2.py)

[Lec 3 code](static_files/materials/lec3.py)

[Lec 1 pdf](static_files/materials/lec3.pdf)

[Lec 2 pdf](static_files/materials/Lec2.pdf)

[Lec 3 pdf](static_files/materials/lec3.pdf)

[Assignment 1](static_files/materials/ps0.pdf)

[Assignment 2](static_files/materials/ps1.pdf)



### In Class Questions
**Shell vs. Editor**

You run the code below from the editor.

```python
type(5)
print(3.0-1)
What’s printed?
```


1. `int`
2. `2.0`
3. `int then 2.0`
4. `nothing`
   

**Python vs. Math**

Which is allowed in Python?


1. `x + y = 2`
2. `x*x = 2`
3. `2 = x`
4. `xy = 2`
5. `None of the Above`
   

**Bindings**

You run the code below from the file editor.

```python
usa_gold = 46
uk_gold = 27
romania_gold = 1

total_gold = usa_gold + uk_gold + romania_gold
print(total_gold)

romania_gold += 1
print(total_gold)
```

What’s printed?


1. 74 then 74
2. 74 then 75
3. 74
4. 75

## Section 2

#### Strings

What is the value of variable `u` from the code below?

```python
once = "umbr"
repeat = "ella"
u = once + (repeat+" ")*4
```

1. umbrella ella ella ella
2. umbrellaellaellaella
3. umbrella
4. umbrella4
Comparisons


What does the code below print?

```python
pset_time = 15
sleep_time = 8
print(sleep_time > pset_time)
derive = True
drink = False
both = drink and derive
print(both)
```

1. alse then False
2. False then True
3. True then False
4. True then True

   
#### Branching

What’s printed when x = 0 and y = 5?

```python
x = float(input("Enter a number for x: "))
y = float(input("Enter a number for y: "))
if x == y:
 if y != 0:
 print("x / y is", x/y)
elif x < y:
 print("x is smaller")
else:
 print("y is smaller")
 ```

1. x is smaller
2. y is smaller
3. x / y is 0.0

#### While Loops

In the code below from Lecture 2, what is printed when you type “Right”?

```
n = input("You're in the Lost Forest. Go left or right? ")
while n == "right":
 n = input("You're in the Lost Forest. Go left or right? ")
print("You got out of the Lost Forest!")
```

You’re in the Lost Forest. Go left or right?
You got out of the Lost Forest!
   
#### For Loops

What is printed when the below code is run?

```python
mysum = 0
for i in range(5, 11, 2):
 mysum += i
 if mysum == 5:
  break
  mysum += 1
print(mysum)
```

1. `5`
2. `6`
3. `21`
4. `24`