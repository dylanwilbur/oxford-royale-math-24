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

```