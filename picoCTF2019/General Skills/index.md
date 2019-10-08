<h1 align="center">General Skills</h1>


<h3>2Warm - Points: 50</h3>
Can you convert the number 42 (base 10) to binary (base 2)?

``` shell
Flag: picoCTF{101010}
```

<h3>Lets Warm Up - Points: 50</h3>
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII? 

``` shell
Flag: picoCTF{p}
```

<h3>Warmed Up - Points: 50</h3>
What is 0x3D (base 16) in decimal (base 10). 

``` shell
Flag: picoCTF{61}
```

<h3>Bases - Points: 100</h3>
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

``` shell
Base64

Flag: picoCTF{l3arn_th3_r0p35}
```

<h3>First Grep - Points: 100</h3>
Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way. You can also find the file in /problems/first-grep_3_2e09f586a51352180a37e25913f5e5d9 on the shell server.

``` shell
root@Bl4st3r:/media/sf_D_DRIVE/picoctf19/general# strings file | grep picoCTF
picoCTF{grep_is_good_to_find_things_5f0c3d9e}

Flag: picoCTF{grep_is_good_to_find_things_5f0c3d9e}
```

<h3>Resources - Points: 100</h3>
We put together a bunch of resources to help you out on our website! If you go over there, you might even find a flag! https://picoctf.com/resources (link)

``` shell
Flag: picoCTF{r3source_pag3_f1ag}
```

<h3>strings it - Points: 100</h3>
Can you find the flag in file without running it? You can also find the file in /problems/strings-it_0_b76c77672f6285e3a39c188481cdff99 on the shell server.

``` shell
root@Bl4st3r:/media/sf_D_DRIVE/picoctf19/general# strings strings | grep picoCTF
picoCTF{5tRIng5_1T_d169bb92}

Flag: picoCTF{5tRIng5_1T_d169bb92}
```

<h3>what's a net cat? - Points: 100</h3>
Using netcat (nc) is going to be pretty important. Can you connect to 2019shell1.picoctf.com at port 37851 to get the flag?

``` shell
root@Bl4st3r:/media/sf_D_DRIVE/picoctf19/general# nc 2019shell1.picoctf.com 37851
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_628e0244}

Flag: picoCTF{nEtCat_Mast3ry_628e0244}
```

<h3>Based - Points: 200</h3>
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with nc 2019shell1.picoctf.com 25180.

``` shell
root@Bl4st3r:/media/sf_D_DRIVE/picoctf19/general# nc 2019shell1.picoctf.com 25180
Let us see how data is stored
chair
Please give the 01100011 01101000 01100001 01101001 01110010 as a word.
...
you have 45 seconds.....

Input:
chair
Please give me the  163 165 142 155 141 162 151 156 145 as a word.
Input:
submarine
Please give me the 7375626d6172696e65 as a word.
Input:
submarine
You've beaten the challenge

Flag: picoCTF{learning_about_converting_values_d57e7f86}
```

<h3>First Grep: Part II - Points: 200</h3>
Can you find the flag in /problems/first-grep--part-ii_3_b4bf3244c2886de1566a28c1b5a465ae/files on the shell server? Remember to use grep.

``` shell
c1ph3r3d@pico-2019-shell1:/problems/first-grep--part-ii_3_b4bf3244c2886de1566a28c1b5a465ae/files$ ls
files0  files1  files10  files2  files3  files4  files5  files6  files7  files8  files9
c1ph3r3d@pico-2019-shell1:/problems/first-grep--part-ii_3_b4bf3244c2886de1566a28c1b5a465ae/files$ find . -type f -print0 | xargs -0 grep "picoCTF"
./files2/file5:picoCTF{grep_r_to_find_this_3675d798}

Flag: picoCTF{grep_r_to_find_this_3675d798}
```

<h3>plumbing - Points: 200</h3>
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to 2019shell1.picoctf.com 57911.

``` shell
root@Bl4st3r:/media/sf_D_DRIVE/picoctf19/general# nc 2019shell1.picoctf.com 57911 | grep picoCTF
picoCTF{digital_plumb3r_931b2271}

Flag: picoCTF{digital_plumb3r_931b2271}
```

<h3>whats-the-difference - Points: 200</h3>
Can you spot the difference? kitters cattos. They are also available at /problems/whats-the-difference_0_00862749a2aeb45993f36cc9cf98a47a on the shell server.

<img src="../Files/kitters.jpg"></img>
          
<img src="../Files/cattos.jpg"></img>        

``` shell
Flag: picoCTF{}
```

<h3>where-is-the-file - Points: 200</h3>
I've used a super secret mind trick to hide this file. Maybe something lies in /problems/where-is-the-file_3_19c1a7766ac2747c446eb9666a9b4fb4.

``` shell
Flag: picoCTF{}
```

<h3>flag_shop - Points: 300</h3>
There's a flag shop selling stuff, can you buy a flag? Source. Connect with nc 2019shell1.picoctf.com 14937.

``` shell
Flag: picoCTF{}
```

<h3>mus1c - Points: 300</h3>
I wrote you a song. Put it in the picoCTF{} flag format.

``` shell
Flag: picoCTF{}

```


<h3>1_wanna_b3_a_r0ck5tar - Points: 350</h3>
I wrote you another song. Put the flag in the picoCTF{} flag format.

``` shell
Flag: picoCTF{}

```


