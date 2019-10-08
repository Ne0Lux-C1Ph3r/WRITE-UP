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



BUG GITHUB FOR IMAGE kitters.jpg, page blank !!!!!      
BUG GITHUB FOR IMAGE cattos.jpg, page blank !!!!!
IMPOSSIBLE OF UPLOAD IMAGES ??????????

``` shell
Work with diff or HxD or .....
Tested with xor on two images but no, test differences on both images !!!

70 69 63 6f 43 54 46 7b 74 68 33 79 72 33 5f 61 35 5f 64 31 66 66 33 72 33 6e 74 5f 34 73 5f 62 75 37 37 33 72 5f 34 6e 64 5f 6a 33 31 31 79 5f 61 73 6c 6b 6a 66 64 73 61 6c 6b 66 73 6c 6b 66 6c 6b 6a 64 73 66 64 73 7a 6d 7a 31 30 35 34 38 7d

Flag: picoCTF{th3yr3_a5_d1ff3r3nt_4s_bu773r_4nd_j311y_aslkjfdsalkfslkflkjdsfdszmz10548}
```

<h3>where-is-the-file - Points: 200</h3>
I've used a super secret mind trick to hide this file. Maybe something lies in /problems/where-is-the-file_3_19c1a7766ac2747c446eb9666a9b4fb4.

``` shell
c1ph3r3d@pico-2019-shell1:~$ cd /problems/where-is-the-file_3_19c1a7766ac2747c446eb9666a9b4fb4
c1ph3r3d@pico-2019-shell1:/problems/where-is-the-file_3_19c1a7766ac2747c446eb9666a9b4fb4$ ls -la
total 80
drwxr-xr-x   2 root       root        4096 Sep 28 22:05 .
drwxr-x--x 684 root       root       69632 Oct  3 00:56 ..
-rw-rw-r--   1 hacksports hacksports    39 Sep 28 22:05 .cant_see_me
c1ph3r3d@pico-2019-shell1:/problems/where-is-the-file_3_19c1a7766ac2747c446eb9666a9b4fb4$ cat .cant_see_me
picoCTF{w3ll_that_d1dnt_w0RK_f28cde66}

Flag: picoCTF{w3ll_that_d1dnt_w0RK_f28cde66}
```

<h3>flag_shop - Points: 300</h3>
There's a flag shop selling stuff, can you buy a flag? Source. Connect with nc 2019shell1.picoctf.com 14937.

``` shell
root@Bl4st3r:/media/sf_D_DRIVE/picoctf19/general# nc 2019shell1.picoctf.com 14937
Welcome to the flag exchange
We sell flags

1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
10000000000000000

The final cost is: -494665728
Your current balance after transaction: 494666828

Welcome to the flag exchange
We sell flags

1. Check Account Balance
2. Buy Flags
3. Exit
 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_e062f0fd}

Flag: picoCTF{m0n3y_bag5_e062f0fd}
```

<h3>mus1c - Points: 300</h3>
I wrote you a song. Put it in the picoCTF{} flag format.

``` shell
Pico's a CTFFFFFFF
my mind is waitin
It's waitin
Put my mind of Pico into This
my flag is not found
put This into my flag
put my flag into Pico
shout Pico
shout Pico
shout Pico
My song's something
put Pico into This
Knock This down, down, down
put This into CTF
shout CTF
my lyric is nothing
Put This without my song into my lyric
Knock my lyric down, down, down
shout my lyric
Put my lyric into This
Put my song with This into my lyric
Knock my lyric down
shout my lyric
Build my lyric up, up ,up
shout my lyric
shout Pico
shout It
Pico CTF is fun
security is important
Fun is fun
Put security with fun into Pico CTF
Build Fun up
shout fun times Pico CTF
put fun times Pico CTF into my song
build it up
shout it
shout it
build it up, up
shout it
shout Pico
```

``` shell
Esotoric language ===> Rockstar

https://codewithrockstar.com/online

114
114
114
111
99
107
110
114
110
48
49
49
51
114

Flag: picoCTF{rrrocknrn0113r}

```


<h3>1_wanna_b3_a_r0ck5tar - Points: 350</h3>
I wrote you another song. Put the flag in the picoCTF{} flag format.

``` shell
Rocknroll is right              
Silence is wrong                
A guitar is a six-string        
Tommy's been down               
Music is a billboard-burning razzmatazz!
Listen to the music             
If the music is a guitar                  
Say "Keep on rocking!"                
Listen to the rhythm
If the rhythm without Music is nothing
Tommy is rockin guitar
Shout Tommy!                    
Music is amazing sensation 
Jamming is awesome presence
Scream Music!                   
Scream Jamming!                 
Tommy is playing rock           
Scream Tommy!       
They are dazzled audiences                  
Shout it!
Rock is electric heaven                     
Scream it!
Tommy is jukebox god            
Say it!                                     
Break it down
Shout "Bring on the rock!"
Else Whisper "That ain't it, Chief"                 
Break it down
```

``` shell
Idem that of "mus1c - Points: 300" unless with javascript, big problem !!!

https://github.com/yanorestes/rockstar-py

Convert the file to .rock and run rockstar-py

Rocknroll = True
Silence = False
a_guitar = 19
Tommy = 44
Music = 160
the_music = input()
if the_music == a_guitar:
    print("Keep on rocking!")
    the_rhythm = input()
    if the_rhythm - Music == False:
        Tommy = 66
        print(Tommy!)
        Music = 79
        Jamming = 78
        print(Music!)
        print(Jamming!)
        Tommy = 74
        print(Tommy!)
        They are dazzled audiences
        print(it!)
        Rock = 86
        print(it!)
        Tommy = 73
        print(it!)
        break
        print("Bring on the rock!")
        Else print("That ain't it, Chief")
        break
        
66 79 78 74 79 86 73

Flag: picoCTF{BONJOVI}

```
