Challenge: Fizz Buzz
----------------------------------------
Category: Programming
----------------------------------------
50 points 
----------------------------------------

```
Description:

Written by wiresboy

Write a program that takes an integer n as input.
Output the numbers 1 through n, in increasing order, one per line.
However, replace any line that is a multiple of 3 with Fizz and any that are a multiple of 5 with Buzz. Any line that is a multiple of 3 and 5 should be written as FizzBuzz.
The input will be the number of lines to write, n, followed by a linebreak.

Sample input:

17

Sample output:

1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17

no Hint!!!!
```

```python
#!/usr/bin/env python

n = int(input(''))

for x in xrange(1, n+1):
 
    fizz = not x % 3
    buzz = not x % 5
 
    if fizz and buzz :
        print "FizzBuzz"
    elif fizz:
        print "Fizz"
    elif buzz:
        print "Buzz"
    else:
        print x
```
