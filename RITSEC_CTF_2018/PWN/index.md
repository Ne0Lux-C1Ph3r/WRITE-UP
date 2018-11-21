<h1 align="center">Exploitation binary</h1>


<h3>ezpwn - Points: 100</h3>

nc fun.ritsec.club 8001

Author: hulto


File: <a href="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/edit/master/RITSEC_CTF_2018/Files/ezpwn">ezpwn</a>


-------------------------------------------------------------


Code source with IDA PRO interesting:

``` python

//----- (0000000000001195) ----------------------------------------------------
int __cdecl main(int argc, const char **argv, const char **envp)
{
  char v4; // [rsp+0h] [rbp-20h]
  FILE *stream; // [rsp+10h] [rbp-10h]
  unsigned int v6; // [rsp+18h] [rbp-8h]
  char i; // [rsp+1Fh] [rbp-1h]

  v6 = 0;
  puts("Please enter your API key");
  gets(&v4, argv);
  if ( v6 == 1 )
  {
    stream = fopen("flag.txt", "r");
    for ( i = fgetc(stream); i != -1; i = fgetc(stream) )
      putchar(i);
    fclose(stream);
  }
  printf("%d\n ", v6);
  return 0;
}

```

Interesting " if (v6 == 1) "


<img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/RITSEC_CTF_2018/Files/pwn.png">

