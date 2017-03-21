Challenge: RSA 2 
----------------------------------------
Category: Cryptography 
----------------------------------------
80 points 
----------------------------------------

```
Description:

Written by neptunia
Some more RSA! This time, there's no P and Q... this.

Hint: It's like RSA 1 but harder. Have fun!

File = ciphertest2.txt

n: 266965481915457805187702917726550329693157
e: 65537
c: 78670065603555615007383828728708393504251
```

```python
#!/usr/bin/env python
import libnum

"""
C:\Users\Ne0Lux-C1Ph3r\Downloads\yafu-1.34>yafu-Win32.exe factor(266965481915457805187702917726550329693157)


fac: factoring 266965481915457805187702917726550329693157
fac: using pretesting plan: normal
fac: no tune info: using qs/gnfs crossover of 95 digits
div: primes less than 10000
rho: x^2 + 3, starting 1000 iterations on C42
rho: x^2 + 2, starting 1000 iterations on C42
rho: x^2 + 1, starting 1000 iterations on C42
pm1: starting B1 = 150K, B2 = gmp-ecm default on C42
ecm: 30/30 curves on C42, B1=2K, B2=gmp-ecm default

starting SIQS on c42: 266965481915457805187702917726550329693157

==== sieving in progress (1 thread):     848 relations needed ====
====           Press ctrl-c to abort and save state           ====
702 rels found: 420 full + 282 from 2810 partial, (11777.70 rels/sec)

SIQS elapsed time = 0.3393 seconds.
Total factoring time = 0.9532 seconds


***factors found***

P21 = 458070420083487550883
P21 = 582804455845022449879

ans = 1
"""

n = 266965481915457805187702917726550329693157
p = 458070420083487550883
q = 582804455845022449879
e = 65537
c = 78670065603555615007383828728708393504251

n=p*q
phi=(p-1)*(q-1)
d = libnum.modular.invmod(e, phi)
print libnum.n2s(pow(c, d, n))

#flag{l0w_n_0eb6}
```

