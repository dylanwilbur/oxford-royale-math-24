---
type: day
title: "Day 8: Cryptography, Zero Knowledge Proofs"
tldr: "Day 1 with stuff"
layout: day
permalink: /day8/
lecture_pdfs:
links:
  - link: https://seeing-theory.brown.edu/basic-probability/index.html
    name: "Probability Theory"
lecture_pdfs:
---

```python
from collections import Counter
Counter("this is a test")

encrypted_message = "IQFTQBQABXQARFTQGZUFQPEFMFQEUZADPQDFARADYMYADQBQDRQOFGZUAZQEFMNXUETVGEFUOQUZEGDQPAYQEFUOFDMZCGUXUFKBDAHUPQRADFTQOAYYAZPQRQZOQBDAYAFQFTQSQZQDMXIQXRMDQMZPEQOGDQFTQNXQEEUZSEARXUNQDFKFAAGDEQXHQEMZPAGDBAEFQDUFKPAADPMUZMZPQEFMNXUETFTUEOAZEFUFGFUAZRADFTQGZUFQPEFMFQEARMYQDUOM"

vignere_message = "SMFJWTYIKWAVKBUGAVQYAAUCHTSKCPGKJNECJKRYAAUCHTSKCPGQJBUGOMNUWVQQYMNPOERUDIYNBQTJPEVVDOEQSQAIYWAHELRPYMNPZOEQSQAIOBEGJOGJEVGJAIVTSMFJWTYFANRPZWHTEAYCJLJJWBRXAZGJAKBUPUNAXMJGOPNNHNVIDBBPPPRDAIPJAAJGOPNNHNVIDBBPPPRNWVQKJOTTKCAFOERUDIYNBQTJPQAVDMSKATQUWVQKJBUGOBEGABFYAAUCHTSKCPGKJBUGDQYNOERUDIYNJMIGNAHTNMAFAZ"

def decrypt_caesar(string, key):
    crypted = ''
    for i in string:
        crypted += tochar((tonum(i) - key) % 26)
    return crypted

def decrypt_vig(string, key):
    key = clean_string(key)
    string = clean_string(string)
    crypted = ''
    j = 0
    for i in string:
        crypted += tochar((tonum(i) - tonum(key[j % len(key)])) % 26)
        j += 1
    return crypted

# Calculate key length
equal_elements = []

# print(ciphertext3)
for i in range(1, len(ciphertext3)):
    # Initialize counter
    count_equal_elements = 0
    # print(ciphertext3[-i:] + ciphertext3[:-i])

    # Check for equal values in corresponding indices
    for elem1, elem2 in zip(ciphertext3, ciphertext3[-i:] + ciphertext3[:-i]):
        if elem1 == elem2:
            count_equal_elements += 1
    equal_elements += [count_equal_elements]

print(equal_elements)

```