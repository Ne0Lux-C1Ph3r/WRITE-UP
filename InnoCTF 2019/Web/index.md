<h1 align="center">Web</h1>

<h3>BGs - Point: 130</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/web1.PNG"></p>


Can you check if this site is hiding something? http://188.130.155.66:3333/dOROspldnYshiUjIPTqMdhSbGfXVEfTX


For this task, I see in the sources and in styles.css.

File: styles.css
```
body {
	background: url(pAyvqTLphMdDaXuHoVroqxRrfFxscmMM.png) no-repeat;
}
```

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/pAyvqTLphMdDaXuHoVroqxRrfFxscmMM.png" height="150%" width="150%"></p>

```
Flag: InnoCTF{orBOcztYaKSCHYunXfUWfBoLXOyIRflc}
```
-----------------------------------------------------------------------------------------------------------------------------------

<h3>Cool Style - Point: 156</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/web2.PNG"></p>

Look at my styled website! http://188.130.155.66:2222/SNjxkpKFztdRyMRuKDszGgdaPoMYAWdc

For this task, I see in the sources.

```
<link rel="stylesheet" href="../assets/css/IhGBxmUuWamOlfQLsgwRf.css">
<link rel="stylesheet" href="../assets/css/nFtJjCdaenlWFcrMMq.css">
<link rel="stylesheet" href="../assets/css/nYTKYJwGJjJPWNfH.css">
<link rel="stylesheet" href="../assets/css/oxvWaLvJfeBNEoBMmVDh.css">
<link rel="stylesheet" href="../assets/css/CyEXjLxxGVjLJhIl.css">
<link rel="stylesheet" href="../assets/css/TjAQMyxZfbmenVdMn.css">
<link rel="stylesheet" href="../assets/css/FrJRIwzvIHzpmNjCgH.css">
<link rel="stylesheet" href="../assets/css/{fqULxWZGVRMEBLwUSE.css">
<link rel="stylesheet" href="../assets/css/wniUEzMpgLfzVOBoq.css">
<link rel="stylesheet" href="../assets/css/ZITelKLKQicRhNtRdMpsV.css">
<link rel="stylesheet" href="../assets/css/BPnqDdJaCvlxXCuHO.css">
<link rel="stylesheet" href="../assets/css/VERrPxZxFCQGIjFDeSnou.css">
<link rel="stylesheet" href="../assets/css/JZFXHYQmTjwvZxqoJp.css">
<link rel="stylesheet" href="../assets/css/dVJAeiTReBxpIfXO.css">
<link rel="stylesheet" href="../assets/css/xZqficMpamGymeJIXPTF.css">
<link rel="stylesheet" href="../assets/css/iVtlfLzpOJEGyFXG.css">
<link rel="stylesheet" href="../assets/css/oCeCkIUoJGTYaLwnwF.css">
<link rel="stylesheet" href="../assets/css/ivtrLcpOUgQXawDl.css">
<link rel="stylesheet" href="../assets/css/dgZznUThlrrkhfRz.css">
<link rel="stylesheet" href="../assets/css/UDcPExqquxvrkwmevfQ.css">
<link rel="stylesheet" href="../assets/css/dbCIyODVNmdGNosiOHe.css">
<link rel="stylesheet" href="../assets/css/UQkczliZwleZVhQLw.css">
<link rel="stylesheet" href="../assets/css/IrWtwbRCkZYpaPHdnt.css">
<link rel="stylesheet" href="../assets/css/ZfDpJvZqKZgPBMNDKTUzj.css">
<link rel="stylesheet" href="../assets/css/DcKHRdpDtIChWpArYTo.css">
<link rel="stylesheet" href="../assets/css/fEkQjJGEfNsXeiUJbfit.css">
<link rel="stylesheet" href="../assets/css/cOMvlchOopKgtKtdFM.css">
<link rel="stylesheet" href="../assets/css/IGaEVuQaeSkiWEtSsla.css">
<link rel="stylesheet" href="../assets/css/YPDrYDMstnXiiBVe.css">
<link rel="stylesheet" href="../assets/css/nfSiaTmONOVnflyY.css">
<link rel="stylesheet" href="../assets/css/GIIOPzmnSnDtVXPNTs.css">
<link rel="stylesheet" href="../assets/css/UvkninmbMyOjDgwfH.css">
<link rel="stylesheet" href="../assets/css/srxjVyCwfTVSptpGdho.css">
<link rel="stylesheet" href="../assets/css/zVDLvZwwVzSyttxFs.css">
<link rel="stylesheet" href="../assets/css/iSubGGSARomwxTNwg.css">
<link rel="stylesheet" href="../assets/css/SXKZOQHDJNbQqqqBjle.css">
<link rel="stylesheet" href="../assets/css/CQkbJgbLcwfwMHKJd.css">
<link rel="stylesheet" href="../assets/css/AJOpAaqVPxzHNfIxHd.css">
<link rel="stylesheet" href="../assets/css/dAekHnkLCGhnKvSN.css">
<link rel="stylesheet" href="../assets/css/DxINJRqmRIvVoPKBb.css">
<link rel="stylesheet" href="../assets/css/}OeIcOVTBBDSSMfruUu.css">
```

```
Flag: InnoCTF{wZBVJdxioidUdUIZDfcIYnGUsziSCAdD}
```
-----------------------------------------------------------------------------------------------------------------------------------

<h3>Robots - Point: 179</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/web3.PNG"></p>


I need your clothes your boots and your motorcycle http://188.130.155.66:4444/UzsVbEjjzEtBqKYPhfMBlHoJaJiMrfMW


For this task, I see in the sources and in robots.txt.

File: robots.txt
Disallow: /*/super-secret-admin-panel

Check on the page and see the sources, page login.php with 2 forms: username and password.

http://188.130.155.66:4444/UzsVbEjjzEtBqKYPhfMBlHoJaJiMrfMW/super-secret-admin-panel/login.php

I use Sqli in two forms: 1' OR 'x'='x'#;

```
Flag: InnoCTF{UNCFZXnQKRahBEAvOeTWeoFaGHHUuqsP}
```
-----------------------------------------------------------------------------------------------------------------------------------

<h3>Back in time - Point: 250</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/web4.PNG"></p>


That's why you need to study history http://188.130.155.66:1111/HlPTFdUftMmSJKUkZwIJrjyAgDeoAVPd


For this task, I see the word history and I think to test .git.
http://188.130.155.66:1111/HlPTFdUftMmSJKUkZwIJrjyAgDeoAVPd/.git

After i use gitdumper.sh for download the repo .git.

``` shell
bash gitdumper.sh http://188.130.155.66:1111/HlPTFdUftMmSJKUkZwIJrjyAgDeoAVPd/.git/ repo

root@Bl4st3r:/media/sf_D_DRIVE/innoctf/web/repo# git status
Sur la branche master
Modifications qui ne seront pas validées :
  (utilisez "git add/rm <fichier>..." pour mettre à jour ce qui sera validé)
  (utilisez "git checkout -- <fichier>..." pour annuler les modifications dans la copie de travail)

	supprimé :        index.php

aucune modification n'a été ajoutée à la validation (utilisez "git add" ou "git commit -a")
root@Bl4st3r:/media/sf_D_DRIVE/innoctf/web/repo# git --no-pager log -p | grep InnoCTF{
-InnoCTF{uxAShQDFJAniSnjZzUzCgaYQztTIMgPP}
+InnoCTF{uxAShQDFJAniSnjZzUzCgaYQztTIMgPP}

```

```
Flag: InnoCTF{uxAShQDFJAniSnjZzUzCgaYQztTIMgPP}
```


