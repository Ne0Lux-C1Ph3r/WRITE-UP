<h1 align="center">Rev</h1>

<h3>Call me - Point: 157</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/rev1.PNG"></p>

For this task, I use Ida Pro for decompile the code and disassemble the function flag.

``` shell
//----- (0000000000001159) ----------------------------------------------------
int __cdecl flag()
{
  void *v0; // rsp
  __int64 v2; // [rsp+0h] [rbp-160h]
  size_t k; // [rsp+8h] [rbp-158h]
  __int64 v4; // [rsp+10h] [rbp-150h]
  char (*p_flag)[]; // [rsp+18h] [rbp-148h]
  int flag_part_1[36]; // [rsp+20h] [rbp-140h]
  int flag_part_2[36]; // [rsp+B0h] [rbp-B0h]
  unsigned __int64 v8; // [rsp+148h] [rbp-18h]

  v8 = __readfsqword(0x28u);
  flag_part_1[0] = 41;
  flag_part_1[1] = 12;
  flag_part_1[2] = 37;
  flag_part_1[3] = 101;
  flag_part_1[4] = 5;
  flag_part_1[5] = 51;
  flag_part_1[6] = 4;
  flag_part_1[7] = 79;
  flag_part_1[8] = 45;
  flag_part_1[9] = 79;
  flag_part_1[10] = 59;
  flag_part_1[11] = 63;
  flag_part_1[12] = 43;
  flag_part_1[13] = 6;
  flag_part_1[14] = 45;
  flag_part_1[15] = 21;
  flag_part_1[16] = 71;
  flag_part_1[17] = 9;
  flag_part_1[18] = 79;
  flag_part_1[19] = 15;
  flag_part_1[20] = 2;
  flag_part_1[21] = 47;
  flag_part_1[22] = 67;
  flag_part_1[23] = 59;
  flag_part_1[24] = 65;
  flag_part_1[25] = 43;
  flag_part_1[26] = 23;
  flag_part_1[27] = 15;
  flag_part_1[28] = 34;
  flag_part_1[29] = 8;
  flag_part_1[30] = 39;
  flag_part_1[31] = 4;
  flag_part_1[32] = 55;
  flag_part_1[33] = 27;
  flag_part_1[34] = 79;
  flag_part_1[35] = 55;
  flag_part_2[0] = 32;
  flag_part_2[1] = 98;
  flag_part_2[2] = 73;
  flag_part_2[3] = 10;
  flag_part_2[4] = 62;
  flag_part_2[5] = 33;
  flag_part_2[6] = 66;
  flag_part_2[7] = 44;
  flag_part_2[8] = 27;
  flag_part_2[9] = 32;
  flag_part_2[10] = 60;
  flag_part_2[11] = 32;
  flag_part_2[12] = 57;
  flag_part_2[13] = 43;
  flag_part_2[14] = 55;
  flag_part_2[15] = 74;
  flag_part_2[16] = 50;
  flag_part_2[17] = 39;
  flag_part_2[18] = 38;
  flag_part_2[19] = 80;
  flag_part_2[20] = 100;
  flag_part_2[21] = 2;
  flag_part_2[22] = 43;
  flag_part_2[23] = 41;
  flag_part_2[24] = 30;
  flag_part_2[25] = 66;
  flag_part_2[26] = 28;
  flag_part_2[27] = 80;
  flag_part_2[28] = 23;
  flag_part_2[29] = 48;
  flag_part_2[30] = 16;
  flag_part_2[31] = 50;
  flag_part_2[32] = 42;
  flag_part_2[33] = 71;
  flag_part_2[34] = 20;
  flag_part_2[35] = 70;
  k = 36LL;
  v4 = 35LL;
  v0 = alloca(48LL);
  p_flag = (char (*)[])&v2;
  HIDWORD(v2) = 0;
  while ( k > SHIDWORD(v2) )
  {
    *((_BYTE *)p_flag + SHIDWORD(v2)) = LOBYTE(flag_part_1[SHIDWORD(v2)]) + LOBYTE(flag_part_2[SHIDWORD(v2)]);
    ++HIDWORD(v2);
  }
  puts("\nYour flag:");
  return puts((const char *)p_flag);
}

//----- (00000000000014F3) ----------------------------------------------------
int __cdecl main(int argc, const char **argv, const char **envp)
{
  printf("\nThere is nothing...\nBye!", argv, envp, argv);
  return 0;
}
```

I added the codes together: flag_part_1 and flag_part_2.

73 110 110 111 67 84 70 123 72 111 119 95 100 49 100 95 121 48 117 95 102 49 110 100 95 109 51 95 57 56 55 54 97 98 99 125

```
Flag: InnoCTF{How_d1d_y0u_f1nd_m3_9876abc}
```

-----------------------------------------------------------------------------------------------------------------------------------

<h3>Quick peek - Point: 220</h3>

<p align="center"><img src="https://github.com/Ne0Lux-C1Ph3r/WRITE-UP/blob/master/InnoCTF%202019/Files/rev2.PNG"></p>

For this task, I use .NET Reflector for decompile the code.

The first function to see is Nothing_interesting_here for the flag.

``` shell

public static bool Nothing_interesting_here(string str)
{
    string[] textArray1 = new string[] { youDefenitelyShouldNotGoHere.prettyGoodFunction(), justBoringClass.whyYouDidNotBelieveMe(false), hackerMark().ToString(), spaceIsBroken.infinity().ToString(), scaryThing.boo(true), spaceIsBroken.infinity().ToString(), youDefenitelyShouldNotGoHere.helloWorld(), justBoringClass.whyYouDidNotBelieveMe(true) };
    string str2 = string.Concat(textArray1);
    return (str == str2);
}


public static string prettyGoodFunction() => 
    "InnoCTF";


public static string whyYouDidNotBelieveMe(bool why)
{
    if (why)
    {
        return "}";
    }
    return "{";
}

 
private static int hackerMark() => 
    0x539; ===> 1337
 
 
public static char infinity() => 
    '_';
    
    
public static string boo(bool answer)
{
    if (answer)
    {
        return "SPAgh377i";
    }
    Console.WriteLine("Can you spell it?");
    string str = "";
    while (true)
    {
        str = str + Console.ReadLine();
        if (str == "InnoCTF{N0T_50_345y}")
        {
            return "Sorry, it is not a flag!";
        }
        if (str.Length == 0x15)
        {
            Console.WriteLine("Sorry, I forgor the first ones, can you repeat?");
            str = "";
        }
    }
}


public static char infinity() => 
    '_';


public static string helloWorld()
{
    int num = 9;
    int num2 = 2;
    num2 = num;
    while (num2 < justBoringClass.aLittleLessThanInfinity)
    {
        Console.WriteLine("Waaaaait a minute");
        num2++;
    }
    byte[] bytes = new byte[] { (byte) num2 };
    char ch = (char) ((num * 7) + 5);
    return (Convert.ToChar(0x43).ToString() + Encoding.ASCII.GetString(bytes) + ch.ToString() + "3");
}


public static string whyYouDidNotBelieveMe(bool why)
{
    if (why)
    {
        return "}";
    }
    return "{";
}

```

After reassembling all the functions for the flag.

```
Flag: InnoCTF{1337_SPAgh377i_CoD3}
```


