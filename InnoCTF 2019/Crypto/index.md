<h1 align="center">Crypto</h1>

<h3>RF - Point: 161</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/crypt1.PNG"></p>


I was walking on rails when suddenly i found this on wooden fence: I3_nase7ncamсo_r1сCt_t4T07_}Fnhs{1


For this task, I use https://www.dcode.fr/chiffre-rail-fence

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/rf.PNG" height="50%" width="50%"></p>


```
Flag: InnoCTF{n0t_ca3sar_7h1s_t1me_7сс4}
```

-----------------------------------------------------------------------------------------------------------------------------------

<h3>Bird mail - Point: 415</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/crypt2.PNG"></p>


<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/cryptobirds.png" height="50%" width="50%"></p>


For this task, I use https://www.geocachingtoolbox.com/index.php?lang=en&page=codeTables&id=birdsOnAWire.

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/birdsOnAWire.png" height="50%" width="50%"></p>


```
do not be mad
you found answer
here some words for
decoding and
flag is
only birds everywhere

Flag: InnoCTF{only_birds_everywhere}
```

-----------------------------------------------------------------------------------------------------------------------------------

<h3>One hundred times RSA - Point: 484</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/crypt3.PNG"></p>

We had intercepted message(823987601539551928252661654437667295378450335918666145079851234798343062080579451801129289418220555) 
and modulus(1522605027922533360535618378132637429718068114961380688657908494580122963258952897654000350692006139). 
Not that we needed all that for the dercrypting, but once you started to break crypto systems, 
the tendency is to push it as far as you can.


For this task, I use http://factordb.com/ and python.

``` python

#!/usr/bin/env python

import libnum
import gmpy

n=1522605027922533360535618378132637429718068114961380688657908494580122963258952897654000350692006139

# P and Q found on http://factordb.com/

p=37975227936943673922808872755445627854565536638199
q=40094690950920881030683735292761468389214899724061

c=823987601539551928252661654437667295378450335918666145079851234798343062080579451801129289418220555

phi=(p-1)*(q-1)

# We search e

for e in range(1,65537):
	d= gmpy.invert(e,phi)
	M = pow(c, d, n)
	if "InnoCTF{" in libnum.n2s(M):
		print libnum.n2s(M)
		print e
		break
    
"""
InnoCTF{cr4ck_rs4_4g41n_5ca2}
53971
"""    

Flag: InnoCTF{cr4ck_rs4_4g41n_5ca2}
```

-----------------------------------------------------------------------------------------------------------------------------------

<h3>Librarian skill - Point: 484</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/crypt4.PNG"></p>


<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/cipher.jpg" height="50%" width="50%"></p>


For this task, I use a pen.

We have 4 files:

File 1984.txt:

His mind slid away into(5) the labyrinthine world of doublethink(10). To know and not to know, to be conscious of(20) complete truthfulness while telling carefully constructed lies(27), to hold simultaneously two opinions which cancelled out, knowing them to be contradictory(40) and believing in both of them, to use logic against logic, to repudiate(53) morality while laying claim to it, to(60) believe that democracy was impossible and that the Party was the guardian of democracy, to forget(76), whatever it was necessary to forget, then to draw(85) it back into memory(89) again at the moment when it was needed, and then promptly(100) to forget it again(104), and above all, to apply the same process to the process itself that was the ultimate(120) subtlety; consciously to induce unconsciousness, and then, once again, to become unconscious of the act of hypnosis(137) you had just(140) performed. Even to understand the word 'doublethink' involved the use of doublethink(152).

File The Catcher in the Rye.txt:

I went over to my window and opened it and(10) packed a snowball with my(15) bare hands. The snow was very good for packing. I didn't throw it at anything(30), though. I started to throw it. At a car that was parked across the street. But I changed my mind(50). The car looked so nice(55) and white. Then I started to throw(62) it at a hydrant, but that looked too nice and white(73), too. Finally I didn't throw it at anything. All I did was close the window and walk around(91) the room with the snowball, packing it harder. A little while later, I still had(106) it with me when I and Brossard(113) and Ackley got on the bus. The bus driver opened the doors(125) and made me throw it out. I told him I wasn't going to chuck it at anybody, but he wouldn't believe me(147). People never believe you(151).

File Animal Farm.txt:

Now, comrades(2), what is the nature of this life of(10) ours? Let us face it: our lives are miserable, laborious, and short. We are born, we are given just so much food as will keep the breath in our bodies(40), and those of us who(45) are capable of it are forced to work to the(55) last atom(57) of our strength; and the very instant that our usefulness has(68) come to an end we are slaughtered(75) with hideous cruelty. No animal in England knows the meaning of happiness or leisure(89) after he is a year(94) old. No animal in England is free. The life of an animal(106) is misery and slavery: that is the plain truth(115).


We know that the file cipher.jpg that it's the photo of Jean Lafitte
and the cipher is:

We deduce that the numbers correspond to the first letter of each word in each paragraph.

1 48 53 53 138  ===> Hurry

13 69 123 2 103 151 ===> slowly

4 6 1 13 26 75 102  ===> inNuwsT


```
Flag: InnoCTF{Hurry_slowly_inNuwsT}
```
