Challenge: Crypto Question 2 |
----------------------------------------
Category: Cryptography |
----------------------------------------
350 points |
----------------------------------------


```
Description:

Breaking Bad Key Exchange
Hint 1 : in the range (1 to g*q), there are couple of pairs yielding common secrete as 399.
Hint 2 : 'a' and 'b' both are less than 1000.
Flag Format: flag{a,b}
```

<img src="./files/cryptopuzzle2.png">

My code is naughty !!!!!

```python
#!/usr/bin/env python

q=541
g=10

a=[]
b=[]

for x in range(1000):
    if g**x % q == 298:
        a.append(x)
for y in range(1000):
    if g**y % q == 330:
        b.append(y)

print "flag{"+str(a)+","+str(b)+"}"

# flag{[170, 710],[268, 808]}


Combination of the code on the site to get the flag.

flag{170,808}

```
