Challenge: Crypto Question 3 |
----------------------------------------
Category: Cryptography |
----------------------------------------
200 points |
----------------------------------------

```
Description:

Breaking Brands!
```

<img src="./image.png">


I used ssh_priv_key tool !

<img src="./AES_crack.png">

```
Now we have the key !!!


root@Ne0Lux-C1Ph3r:/media/sf_hackim/crypto# openssl rsa -in HackIM.key 		
Enter pass phrase for HackIM.key: 141525

writing RSA key
-----BEGIN RSA PRIVATE KEY-----
MIIEpQIBAAKCAQEAy5QUCCa10WJ4ZwTPjsr9jM6zjuscyqEEQlft3cItkv0Qy2N9
pR7G2RbE9Vw9cZ8a0OyzOjMIuZe54G3qVArGLybAo3HDMTPHqDlgYq6MPoIYCrno
q9IPfhfme/+ImUORUL4LaIXSsm1bsf0dfXYR6S0r8CNTpZOmWi7RGhv3hJUKC8Rm
VAb2gBavAW9Cs0XoU75vkBFuSfd7fMpEwnmmWz78SRsFceNDwxshMV64O3K9aSbY
4F5MlI8eCQnEekhtSp2p2jYnsj7xWfAaM91p4wXpD6B4YuqxXTLaE2YaJYqRzJpa
4wkOLn0gPk7PmM/xigwctUs4YFPlmK7CfbfEAwIDAQABAoIBAQC/C2GZHKq3qk8P
bmZRvJEg2MGMt3s3dM+Iavfgid8296IRHHbGxBEbnNCM6VkIDaWetuKjFU10zbwz
rzKeV9YQXa+eMp5YyBzv85hOQzt9VZy2RCzjQagkTs2PRAiuu8fdG9uc5SkLJLFO
YRiRqoG4bxmyq5RN6DfOnezBMcmgcogcgpUgUt0f0r1CfEijmST0XNzQio4rVbe5
DO2VndS9XcMGofSOgO6IL5X3cNKDUkqNpSI+Sdj0osR9i+xVy3fHjejkxtbfMrfQ
gLPKMA3jc5vc6K6qs6Iv2OUhClSIcaYnCvsGqkER0eePh/k0liWdWqphUCjAr4FW
YemqPGIhAoGBAO9a7Ino3d04vBDCm/r8++CDUCJP5qNS03edtjg/Wn5V0ZxJQdwH
aB/0fvmo84ddFdNG+H8BGMWEzD17yfKMlJpb2vkWAcb14BolqO+e3CKll86w0yvf
6bZ863ahlLDYxsvAqFcGqrUQDdk5WBUt4OHsVVvo6Cg65/oEhcp2lCA7AoGBANm8
PteJUmJm7lbtzxio+F50LLrNCTUEZPp+jEqjjt37iyBtt3dAjOro6pD7BDYwCRdj
W7bOR6/X6RE3zw0NqaTzJiepBlnNDir28A+0mUhslahZklXL7dIT59SwXZA3OBQq
OgzpV39wMJW+B2qnebY//7sHgARUX4QXjBf4VDbZAoGBANrPvD227Fw4aXTI899X
NsvgP3meobHdHgTT4Kk7AXdM7Pp63gJPoxjTYuDJWxf8ON+UmcdBMWwgIrZyXAOo
EJGsN1pOjAFe9SfyFaY5C/WAfG8vp10MrZNuT7N7s3qYMeRCk6I7LgOoUYCrs6Jo
9pSSgNYs7U8Zysf9KnIURQXRAoGAQQckqZCcp0Dgi9vITzAfxW3i8gNMbaYbVmi3
E4+XmpqGqa+67IW90Gaxr40Ya+qavH5zJLyk0lKki/zj/J0I/neT/KJRgD5qrdBE
UBx67xNm+vmNZ8xZAbXqNi5aMzkaqYMXBUYnWKs0B3TSmDrecdzZTo1l4WUlhbjW
oU4MMLkCgYEAkoSoqIlIxlWrlMYvNIHsZQ6ncDN29ViCAKcB1v9VG4y9ogpAjcOt
SdwrMVH+8o5xTr2gdaky3PalOkudkJ0tMM7k1FN8THcnImzm3AfeRi059yPEs1gR
ebEM/+vs+Y+9Z9N/h8PvS+/iG51q1N70k+ewDOXC60DZSnUE1ZaVVMY=
-----END RSA PRIVATE KEY-----


openssl rsautl -decrypt -inkey ssh_key.txt -in message.new -out flag.txt


flag.txt:
Now that u r here. Go 2 the digit's page No.["password u found to decrpt the key"],
out of all Logos this Brand (case sensitive) has MD5 : 8c437d9ef6c7786e9df3ac2bf223445e


I searched on google and on issuu.com

https://issuu.com/thinkdigit/docs/digit_jun_2016

I found the page 141525 and test the combination of logos for md5.

```

<img src="./141525.png">

```
clearTax == 8c437d9ef6c7786e9df3ac2bf223445e

flag{clearTax}
```




