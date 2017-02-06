Challenge: CR4: Poor RSA |
----------------------------------------
Category: Cryptography |
----------------------------------------
200 points |
----------------------------------------


```

Files: flag.b64 and key.pub

flag.b64:
Ni45iH4UnXSttNuf0Oy80+G5J7tm8sBJuDNN7qfTIdEKJow4siF2cpSbP/qIWDjSi+w=

key.pub:
-----BEGIN PUBLIC KEY-----
ME0wDQYJKoZIhvcNAQEBBQADPAAwOQIyUqmeJJ7nzzwMv5Y6AJZhdyvJzfbh4/v8
bkSgel4PiURXqfgcOuEyrFaD01soulwyQkMCAwEAAQ==
-----END PUBLIC KEY-----
```
```shell
openssl rsa -noout -text -inform PEM -in key.pub -pubin

Public-Key: (399 bit)
Modulus:
    52:a9:9e:24:9e:e7:cf:3c:0c:bf:96:3a:00:96:61:
    77:2b:c9:cd:f6:e1:e3:fb:fc:6e:44:a0:7a:5e:0f:
    89:44:57:a9:f8:1c:3a:e1:32:ac:56:83:d3:5b:28:
    ba:5c:32:42:43
Exponent: 65537 (0x10001)
```
```python
python -c "print int('52a99e249ee7cf3c0cbf963a009661772bc9cdf6e1e3fbfc6e44a07a5e0f894457a9f81c3ae132ac5683d35b28ba5c324243', 16)"


n=833810193564967701912362955539789451139872863794534923259743419423089229206473091408403560311191545764221310666338878019
```
```

Search to FactorDb p and q:

p=863653476616376575308866344984576466644942572246900013156919
q=965445304326998194798282228842484732438457170595999523426901
```
```shell
python rsatool.py -p 863653476616376575308866344984576466644942572246900013156919 -q 965445304326998194798282228842484732438457170595999523426901 -o priv.key


Using (p, q) to initialise RSA instance

n =52a99e249ee7cf3c0cbf963a009661772bc9cdf6e1e3fbfc6e44a07a5e0f894457a9f81c3ae132ac5683d35b28ba5c324243
e = 65537 (0x10001)
d =33ad09ca06f50f9e90b1acae71f390d6b92f1d6d3b6614ff871181c4df08da4c5f5012457a64309405eaecd6341e43027931
p =899683060c76b9c0de581a69e0ea9d91bed1071beb1d924a37
q =99cde74aedee87adffdd684cbc478e759870b4f20692f65255
Saving PEM as priv.key
```
```
priv.key:
-----BEGIN RSA PRIVATE KEY-----
MIH5AgEAAjJSqZ4knufPPAy/ljoAlmF3K8nN9uHj+/xuRKB6Xg+JRFep+Bw64TKsVoPTWyi6XDJC
QwIDAQABAjIzrQnKBvUPnpCxrK5x85DWuS8dbTtmFP+HEYHE3wjaTF9QEkV6ZDCUBers1jQeQwJ5
MQIaAImWgwYMdrnA3lgaaeDqnZG+0Qcb6x2SSjcCGgCZzedK7e6Hrf/daEy8R451mHC08gaS9lJV
AhlmZEB1y+i/LC1L27xXycIhqKPeaoR6qVfZAhlbPhKLmhFavne/AqQbQhwaWT/rqHUL9EMtAhk5
pem+TgbW3zCYF8v7j0mjJ31NC+0sLmx5
-----END RSA PRIVATE KEY-----
```
```python

#!/usr/bin/python

def decrypt_RSA(privkey, message):
    from Crypto.PublicKey import RSA  
    from base64 import b64decode 
    key = open(privkey, "r").read() 
    rsakey = RSA.importKey(key) 
    decrypted = rsakey.decrypt(b64decode(message)) 
    return decrypted

flag = "Ni45iH4UnXSttNuf0Oy80+G5J7tm8sBJuDNN7qfTIdEKJow4siF2cpSbP/qIWDjSi+w="
print decrypt_RSA('priv.key', flag)

#ALEXCTF{SMALL_PRIMES_ARE_BAD}



```
