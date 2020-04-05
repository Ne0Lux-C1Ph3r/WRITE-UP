
<h1 align="center">Script</h1>


<h3>2xPAD 100 points</h3>

The latest and greatest encryption scheme, “two-time pad” is twice as secure as one time pads. Check it out!

Download the files below: encrypted_one.png and encrypted_two.png

<p align="center"><img src="../Files/encrypted_one.png"></img></p>

<p align="center"><img src="../Files/encrypted_two.png"></img></p>

<p align="center"><img src="../Files/flag_xor.png"></img></p>

``` shell
For this challenge, i use convert of imagemagick.
convert encrypted_one.png encrypted_two.png -fx "((255-u)&v)|(u&(255-v))" flag_xor.png

Flag: LLS{dont_reuse_your_keys}
```

<p align="left"><a href="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/VirSecCon CTF/index.md">Return to the main menu</a></p>


