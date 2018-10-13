<h1 align="center">Cryptography</h1>


<h3>Crypto Warmup 1 - Points: 75</h3>
Crpyto can often be done by hand, here's a message you got from a friend, llkjmlmpadkkc with the key of thisisalilkey. Can you use this table to solve it?.

``` shell
Flag: picoCTF{SECRETMESSAGE}
```

<h3>Crypto Warmup 2 - Points: 75</h3>
Cryptography doesn't have to be complicated, have you ever heard of something called rot13? cvpbPGS{guvf_vf_pelcgb!} 

``` shell
Flag: picoCTF{this_is_crypto!}
```

<h3>HEEEEEEERE'S Johnny! - Points: 100</h3>
Okay, so we found some important looking files on a linux computer. Maybe they can be used to get a password to the process. Connect with nc 2018shell2.picoctf.com 5221. Files can be found here: passwd shadow. 

``` shell
Flag: Use john the ripper
D:\Securite-Informatique\john180j1w\run>unshadow.exe D:\picoctf\crypto\passwd D:\picoctf\crypto\shadow > D:\picoctf\crypto\flag_passwd_shadow

D:\picoctf>nc 2018shell2.picoctf.com 5221
Username: root
Password: kissme
picoCTF{J0hn_1$_R1pp3d_289677b5}

```

<h3>caesar cipher 1 - Points: 150</h3>
This is one of the older ciphers in the books, can you decrypt the message? You can find the ciphertext in /problems/caesar-cipher-1_1_6fbf7a9ce0aac23bab1c37836cc20c3b on the shell server. 

``` shell
Flag: picoCTF{vgefmsaapaxpomqemdoubtqdxoaxypeo}
picoCTF{justagoodoldcaesarcipherlcolmdsc}
```

<h3>hertz - Points: 150</h3>
Here's another simple cipher for you where we made a bunch of substitutions. Can you decrypt it? Connect with nc 2018shell2.picoctf.com 43324.  

``` shell
Flag: quipqiup - cryptoquip and cryptogram solver
congrats here is your flag - substitution_ciphers_are_solvable_fuosdblgwv ------------------------------------------------------------------------------- call me ishmael. some years ago-never mind how long precisely-having little or no money in my purse, and nothing particular to interest me on shore, i thought i would sail about a little and see the watery part of the world. it is a way i have of driving off the spleen and regulating the circulation. whenever i find myself growing grim about the mouth; whenever it is a damp, dri??ly november in my soul; whenever i find myself involuntarily pausing before coffin warehouses, and bringing up the rear of every funeral i meet; and especially whenever my hypos get such an upper hand of me, that it re?uires a strong moral principle to prevent me from deliberately stepping into the street, and methodically ?noc?ing people's hats off-then, i account it high time to get to sea as soon as i can. this is my substitute for pistol and ball. with a philosophical flourish cato throws himself upon his sword; i ?uietly ta?e to the ship. there is nothing surprising in this. if they but ?new it, almost all men in their degree, some time or other, cherish very nearly the same feelings towards the ocean with me. there now is your insular city of the manhattoes, belted round by wharves as indian isles by coral reefs-commerce surrounds it with her surf. right and left, the streets ta?e you waterward. its extreme downtown is the battery, where that noble mole is washed by waves, and cooled by bree?es, which a few hours previous were out of sight of land. loo? at the crowds of water-ga?ers there. circumambulate the city of a dreamy sabbath afternoon. go from corlears hoo? to coenties slip, and from thence, by whitehall, northward. what do you see?-posted li?e silent sentinels all around the town, stand thousands upon thousands of mortal men fixed in ocean reveries. some leaning against the spiles; some seated upon the pier-heads; some loo?ing over the bulwar?s of ships from china; some high aloft in the rigging, as if striving to get a still better seaward peep. but these are all landsmen; of wee? days pent up in lath and plaster-tied to counters, nailed to benches, clinched to des?s. how then is this? are the green fields gone? what do they here? but loo?! here come more crowds, pacing straight for the water, and seemingly bound for a dive. strange! nothing will content them but the extremest limit of the land; loitering under the shady lee of yonder warehouses will not suffice. no. they must get ?ust as nigh the water as they possibly can without falling in. and there they stand-miles of them-leagues. inlanders all, they come from lanes and alleys, streets and avenues-north, east, south, and west. yet here they all unite. tell me, does the magnetic virtue of the needles of the compasses of all those ships attract them thither?

picoCTF{substitution_ciphers_are_solvable_fuosdblgwv}
```

<h3>blaise's cipher - Points: 200</h3>
My buddy Blaise told me he learned about this cool cipher invented by a guy also named Blaise! Can you figure out what it says? Connect with nc 2018shell2.picoctf.com 11281. 

``` shell
Flag: dCode - Solveurs, Crypto, Maths, Décodage, Outils en ligne
The first well-documented description of a polyalphabetic cipher was formulated by Leon Battista Alberti around 1467 and used a metal cipher disc to switch between cipher alphabets. Alberti's system only switched alphabets after several words, and switches were indicated by writing the letter of the corresponding alphabet in the ciphertext. Later, in 1508, Johannes Trithemius, in his work Poligraphia, invented the tabula recta, a critical component of the Vigenere cipher. The Trithemius cipher, however, only provided a progressive, rigid, and predictable system for switching between cipher alphabets.

What is now known as the Vigenere cipher was originally described by Giovan Battista Bellaso in his 1553 book La cifra del. Sig. Giovan Battista Bellaso. He built upon the tabula recta of Trithemius, but added a repeating "countersign" (a key) to switch cipher alphabets every letter. Whereas Alberti and Trithemius used a fixed pattern of substitutions, Bellaso's scheme meant the pattern of substitutions could be easily changed simply by selecting a new key. Keys were typically single words or short phrases, known to both parties in advance, or transmitted "out of band" along with the message. Bellaso's method thus required strong security for only the key. As it is relatively easy to secure a short key phrase, say by a previous private conversation, Bellaso's system was considerably more secure.

Blaise de Vigenere published his description of a similar but stronger autokey cipher before the court of Henry III of France, in 1586. Later, in the 19th century, the invention of Bellaso's cipher was misattributed to Vigenere. David Kahn in his book The Codebreakers lamented the misattribution by saying that history had "ignored this important contribution and instead named a regressive and elementary cipher for him [Vigenere] though he had nothing to do with it". picoCTF{v1gn3r3_c1ph3rs_ar3n7_bad_5352bf72}

The Vigenere cipher gained a reputation for being exceptionally strong. Noted author and mathematician Charles Lutwidge Dodgson (Lewis Carroll) called the Vigenere cipher unbreakable in his 1868 piece "The Alphabet Cipher" in a children's magazine. In 1917, Scientific American described the Vigenere cipher as "impossible of translation". This reputation was not deserved. Charles Babbage is known to have broken a variant of the cipher as early as 1854; however, he didn't publish his work. Kasiski entirely broke the cipher and published the technique in the 19th century. Even before this, though, some skilled cryptanalysts could occasionally break the cipher in the 16th century.

Cryptographic slide rule used as a calculation aid by the Swiss Army between 1914 and 1940.
The Vigenere cipher is simple enough to be a field cipher if it is used in conjunction with cipher disks. The Confederate States of America, for example, used a brass cipher disk to implement the Vigenere cipher during the American Civil War. The Confederacy's messages were far from secret and the Union regularly cracked their messages. Throughout the war, the Confederate leadership primarily relied upon three key phrases, "Manchester Bluff", "Complete Victory" and, as the war came to a close, "Come Retribution".

Gilbert Vernam tried to repair the broken cipher (creating the VernamDCiBxmdttxd ixvgkg om 1918), hjz, mu bgsztx vnpz gk soc, zwk boendx lgr yiokr kakttxzhak su rxxvigmgaeroh. Bdxcgl'y luqq, wuvkkkq, kkkmzjgkrn rdj iu snt umk-iolk egc, g indugksorgkrn amhgkzqphkk roontx.
```

<h3>hertz 2 - Points: 200</h3>
This flag has been encrypted with some kind of cipher, can you decrypt it? Connect with nc 2018shell2.picoctf.com 39961. 

``` shell
Flag: picoCTF{substitution_ciphers_are_too_easy_npaebrehlt}
```

<h3>caesar cipher 2 - Points: 250</h3>
Can you help us decrypt this message? We believe it is a form of a caesar cipher. You can find the ciphertext in /problems/caesar-cipher-2_4_23c82ed24f4436e96acc1f9f22dc8799 on the shell server. 

``` shell
Flag: #!usr/bin/python
message = "d]Wc7H:oW5YgUFS7]D\9fGS^iGHSUF9bHSg9WIf9q"
LETTERS = r"!\"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~"

for key in range(len(LETTERS)):
	translated = ''
	for symbol in message:
		if symbol in LETTERS:
			num = LETTERS.find(symbol)
			num = num - key
			if num < 0:
				num = num + len(LETTERS)
				# add number's symbol at the end of translated
				translated = translated + LETTERS[num]
			else:
				translated = translated + symbol
	if "picoCTF{" in translated:
		print('Key #%s: %s' % (key, translated))
    
D:\picoctf>python 2-cesar.py
Key #83: picoCTF{cAesaR_CiPhErS_juST_aREnT_sEcUrE}
```

<h3>rsa-madlibs - Points: 250</h3>
We ran into some weird puzzles we think may mean something, can you help me solve one? Connect with nc 2018shell2.picoctf.com 36859

``` shell
Flag: C:\Users\Ne0Lux-C1Ph3r>ncat 2018shell2.picoctf.com 36859
0x7069636f4354467b64305f755f6b6e30775f7468335f7740795f325f5253405f39646337356431327dL <type 'long'>
Hello, Welcome to RSA Madlibs
Keeping young children entertained, since, well, nev3r
Tell us how to fill in the blanks, or if it's even possible to do so
Everything, input and output, is decimal, not hex
#### NEW MADLIB ####
q : 93187
p : 94603
##### WE'RE GONNA NEED THE FOLLOWING ####
n
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y
#### TIME TO FILL IN THE MADLIB! ###
n: 8815769761
YAHHH! That one was a great madlib!!!


#### NEW MADLIB ####
p : 81203
n : 6315400919
##### WE'RE GONNA NEED THE FOLLOWING ####
q
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y
#### TIME TO FILL IN THE MADLIB! ###
q: 77773
YAHHH! That one was a great madlib!!!


#### NEW MADLIB ####
e : 3
n : 12738162802910546503821920886905393316386362759567480839428456525224226445173031635306683726182522494910808518920409019414034814409330094245825749680913204566832337704700165993198897029795786969124232138869784626202501366135975223827287812326250577148625360887698930625504334325804587329905617936581116392784684334664204309771430814449606147221349888320403451637882447709796221706470239625292297988766493746209684880843111138170600039888112404411310974758532603998608057008811836384597579147244737606088756299939654265086899096359070667266167754944587948695842171915048619846282873769413489072243477764350071787327913
##### WE'RE GONNA NEED THE FOLLOWING ####
q
p
IS THIS POSSIBLE and FEASIBLE? (Y/N):N

print int('0x7069636f4354467b64305f755f6b6e30775f7468335f7740795f325f5253405f39646337356431327d',16)
240109877286251840533272915662757983981706320845661471802585807564915966910384375649897669765182077

picoCTF{d0_u_kn0w_th3_w@y_2_RS@_9dc75d12}
```

<h3>Safe RSA - Points: 250</h3>
Now that you know about RSA can you help us decrypt this ciphertext? We don't have the decryption key but something about those values looks funky.. 

``` shell
Flag: N: 374159235470172130988938196520880526947952521620932362050308663243595788308583992120881359365258949723819911758198013202644666489247987314025169670926273213367237020188587742716017314320191350666762541039238241984934473188656610615918474673963331992408750047451253205158436452814354564283003696666945950908549197175404580533132142111356931324330631843602412540295482841975783884766801266552337129105407869020730226041538750535628619717708838029286366761470986056335230171148734027536820544543251801093230809186222940806718221638845816521738601843083746103374974120575519418797642878012234163709518203946599836959811
e: 3
ciphertext (c): 2205316413931134031046440767620541984801091216351222789180967130585669043554866325905770867150377611820746759815247778516899403229047066700396787852388511389893043279713280998235746440322483431305358901578692935378439077796777060321410661 

#!usr/bin/python

import gmpy


n = 374159235470172130988938196520880526947952521620932362050308663243595788308583992120881359365258949723819911758198013202644666489247987314025169670926273213367237020188587742716017314320191350666762541039238241984934473188656610615918474673963331992408750047451253205158436452814354564283003696666945950908549197175404580533132142111356931324330631843602412540295482841975783884766801266552337129105407869020730226041538750535628619717708838029286366761470986056335230171148734027536820544543251801093230809186222940806718221638845816521738601843083746103374974120575519418797642878012234163709518203946599836959811
e = 3
cipher_str = 2205316413931134031046440767620541984801091216351222789180967130585669043554866325905770867150377611820746759815247778516899403229047066700396787852388511389893043279713280998235746440322483431305358901578692935378439077796777060321410661


gs = gmpy.mpz(cipher_str)
gm = gmpy.mpz(n)
g3 = gmpy.mpz(3)
 
mask = gmpy.mpz(0x8080808080808080808080808080808080808080808080808080808080808080808080808080808080808080808080808080808080808080808080808000)
test = 0
while True:
  if test == 0:
   gs = gs
  else:
   gs += gm
  root,exact = gs.root(g3)
  if (root & mask).bit_length() < 8:
    print root
    break

print '\n',hex(int(root))[2:-1].decode('hex')
13016382529449106065839070830454998857466392684017754632234663461760173202301821
# picoCTF{e_w4y_t00_sm411_a5b5aaac}
```

<h3>Super Safe RSA - Points: 350</h3>
Dr. Xernon made the mistake of rolling his own crypto.. Can you find the bug and decrypt the message? Connect with nc 2018shell2.picoctf.com 59208. 

``` shell
Flag: c= 2331424592639591144662174353831345536059345899183922101799549219078340493648239
n= 20083201645142857999117650741944029547566051492731829328375468250564592690184683
e= 65537

D:\Securite-Informatique\yafu-1.34>yafu-Win32.exe factor(20083201645142857999117650741944029547566051492731829328375468250564592690184683)


fac: factoring 20083201645142857999117650741944029547566051492731829328375468250564592690184683
fac: using pretesting plan: normal
fac: no tune info: using qs/gnfs crossover of 95 digits
div: primes less than 10000
rho: x^2 + 3, starting 1000 iterations on C80
rho: x^2 + 2, starting 1000 iterations on C80
rho: x^2 + 1, starting 1000 iterations on C80
pm1: starting B1 = 150K, B2 = gmp-ecm default on C80
ecm: 30/30 curves on C80, B1=2K, B2=gmp-ecm default
ecm: 74/74 curves on C80, B1=11K, B2=gmp-ecm default
ecm: 188/188 curves on C80, B1=50K, B2=gmp-ecm default, ETA: 1 sec

starting SIQS on c80: 20083201645142857999117650741944029547566051492731829328375468250564592690184683

==== sieving in progress (1 thread):   46016 relations needed ====
====           Press ctrl-c to abort and save state           ====
45951 rels found: 23817 full + 22134 from 236052 partial, (426.64 rels/sec)

SIQS elapsed time = 614.7211 seconds.
Total factoring time = 763.3670 seconds


***factors found***

P42 = 141477750372613211120886391888139850358957
P39 = 141953074545285510013526911085477398519

ans = 1

#!usr/bin/python

import libnum

c= 2331424592639591144662174353831345536059345899183922101799549219078340493648239
n= 20083201645142857999117650741944029547566051492731829328375468250564592690184683
e= 65537
p=141477750372613211120886391888139850358957
q=141953074545285510013526911085477398519

n=p*q
phi=(p-1)*(q-1)
d = libnum.modular.invmod(e, phi)
print libnum.n2s(pow(c, d, n))

# picoCTF{us3_l@rg3r_pr1m3$_6791}
```

<h3>Super Safe RSA 2 - Points: 450</h3>
Wow, he made the exponent really large so the encryption MUST be safe, right?! Connect with nc 2018shell2.picoctf.com 29483. 

``` shell
Flag: import math
import random

############################
## Wiener's Attack module ##
############################

# Calculates bitlength
def bitlength(x):
  assert x >= 0
  n = 0
  while x > 0:
    n = n+1
    x = x>>1
  return n
  
# Squareroots an integer
def isqrt(n):
  if n < 0:
    raise ValueError('square root not defined for negative numbers')  
  if n == 0:
    return 0
  a, b = divmod(bitlength(n), 2)
  x = 2**(a+b)
  while True:
    y = (x + n//x)//2
    if y >= x:
      return x
    x = y

# Checks if an integer has a perfect square
def is_perfect_square(n):
  h = n & 0xF; #last hexadecimal "digit"    
  if h > 9:
    return -1 # return immediately in 6 cases out of 16.
  # Take advantage of Boolean short-circuit evaluation
  if ( h != 2 and h != 3 and h != 5 and h != 6 and h != 7 and h != 8 ):
    # take square root if you must
    t = isqrt(n)
    if t*t == n:
      return t
    else:
      return -1    
  return -1

# Calculate a sequence of continued fractions
def partial_quotiens(x, y):
  partials = []
  while x != 1:
    partials.append(x // y)
    a = y
    b = x % y
    x = a
    y = b
  #print partials
  return partials

# Helper function for convergents
def indexed_convergent(sequence):
  i = len(sequence) - 1
  num = sequence[i]
  denom = 1
  while i > 0:
    i -= 1
    a = (sequence[i] * num) + denom
    b = num
    num = a
    denom = b
  #print (num, denom)
  return (num, denom)

# Calculate convergents of a  sequence of continued fractions
def convergents(sequence):
  c = []
  for i in range(1, len(sequence)):
    c.append(indexed_convergent(sequence[0:i]))
  #print c
  return c

# Calculate `phi(N)` from `e`, `d` and `k`
def phiN(e, d, k):
  return ((e * d) - 1) / k

# Wiener's attack, see http://en.wikipedia.org/wiki/Wiener%27s_attack for more information
def wiener_attack(N,e):
  (p,q,d) = (0,0,0)
  conv=convergents(partial_quotiens(e,N))
  for frac in conv:
    (k,d)=frac
    if k == 0:
      continue
    y = -(N - phiN(e, d, k) + 1)
    discr = y*y - 4*N
    if(discr>=0):
      # since we need an integer for our roots we need a perfect squared discriminant
      sqr_discr = is_perfect_square(discr)
      # test if discr is positive and the roots are integers
      if sqr_discr!=-1 and (-y+sqr_discr)%2==0:
        p = ((-y+sqr_discr)/2)
        q = ((-y-sqr_discr)/2)
        return p, q, d
  return p, q, d

################################
## End Wiener's Attack module ##
################################


c= 63717210435459810077746045343723329526127753556862139937763499557651394445773564892814620584050288640832682612940161229610049970244332107405753068492076963756316925198367864118180394117507148773923850891081452175235733168095611156720688288669198701490027264384256603617167877055049171150605800787128733275422
N= 97415105619097000978980968727210795403611033307543922188423738383106467864333131029750634962932984582117909797604219133038335921330033381255806052425550990019839870815744717647217172477244605824335737356990363674647998131941101838355191189279415706787020390906175907041106642546436603726404305308194818905331
e= 35346921763616379804998206148176949123363449227968849194206577944524036892348472708355129154806389876905624227337661641266027254973956601709920623871699987176929329561430748497203261087477473467831669981265791176197024441224717238422995226528289511256327088344551457301071020578764718258534208980642097717633


print "start attack!"
print wiener_attack(N,e)


D:\picoctf\crypto>python wiener.py
start attack!
(12553769548920978433463143671687173488500088588623978826992590869343469650568068384521796589611461589932121513804044680339386721981196344812817482132478179L, 7759829048914636470716402763957017661535294913427619772329053579974150833370601027098055386663062776615688073841552343398379626172550683695435862343360689L, 65537L)


import libnum

c= 63717210435459810077746045343723329526127753556862139937763499557651394445773564892814620584050288640832682612940161229610049970244332107405753068492076963756316925198367864118180394117507148773923850891081452175235733168095611156720688288669198701490027264384256603617167877055049171150605800787128733275422
n= 97415105619097000978980968727210795403611033307543922188423738383106467864333131029750634962932984582117909797604219133038335921330033381255806052425550990019839870815744717647217172477244605824335737356990363674647998131941101838355191189279415706787020390906175907041106642546436603726404305308194818905331
e= 35346921763616379804998206148176949123363449227968849194206577944524036892348472708355129154806389876905624227337661641266027254973956601709920623871699987176929329561430748497203261087477473467831669981265791176197024441224717238422995226528289511256327088344551457301071020578764718258534208980642097717633

p=12553769548920978433463143671687173488500088588623978826992590869343469650568068384521796589611461589932121513804044680339386721981196344812817482132478179
q=7759829048914636470716402763957017661535294913427619772329053579974150833370601027098055386663062776615688073841552343398379626172550683695435862343360689

n=p*q
phi=(p-1)*(q-1)
d = libnum.modular.invmod(e, phi)
print libnum.n2s(pow(c, d, n))

#picoCTF{w@tch_y0ur_Xp0n3nt$_c@r3fu11y_3620762}
```
