


<h1 align="center">Reverse Engineering</h1>


<h3>vault-door-training - Points: 50</h3>
Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility. The source code for the training vault is here: VaultDoorTraining.java.

``` shell

import java.util.*;

class VaultDoorTraining {
    public static void main(String args[]) {
        VaultDoorTraining vaultDoor = new VaultDoorTraining();
        Scanner scanner = new Scanner(System.in); 
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
	String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
	if (vaultDoor.checkPassword(input)) {
	    System.out.println("Access granted.");
	} else {
	    System.out.println("Access denied!");
	}
   }

    // The password is below. Is it safe to put the password in the source code?
    // What if somebody stole our source code? Then they would know what our
    // password is. Hmm... I will think of some ways to improve the security
    // on the other doors.
    //
    // -Minion #9567
    public boolean checkPassword(String password) {
        return password.equals("w4rm1ng_Up_w1tH_jAv4_f2dd1ba95aa");
    }
}

Flag: picoCTF{w4rm1ng_Up_w1tH_jAv4_f2dd1ba95aa}
```


<h3>vault-door-1 - Points: 100</h3>
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: VaultDoor1.java.

``` shell

import java.util.*;

class VaultDoor1 {
    public static void main(String args[]) {
        VaultDoor1 vaultDoor = new VaultDoor1();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
	String userInput = scanner.next();
	String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
	if (vaultDoor.checkPassword(input)) {
	    System.out.println("Access granted.");
	} else {
	    System.out.println("Access denied!");
	}
    }

    // I came up with a more secure way to check the password without putting
    // the password itself in the source code. I think this is going to be
    // UNHACKABLE!! I hope Dr. Evil agrees...
    //
    // -Minion #8728
    public boolean checkPassword(String password) {
        return password.length() == 32 &&
               password.charAt(0)  == 'd' &&
               password.charAt(29) == '7' &&
               password.charAt(4)  == 'r' &&
               password.charAt(2)  == '5' &&
               password.charAt(23) == 'r' &&
               password.charAt(3)  == 'c' &&
               password.charAt(17) == '4' &&
               password.charAt(1)  == '3' &&
               password.charAt(7)  == 'b' &&
               password.charAt(10) == '_' &&
               password.charAt(5)  == '4' &&
               password.charAt(9)  == '3' &&
               password.charAt(11) == 't' &&
               password.charAt(15) == 'c' &&
               password.charAt(8)  == 'l' &&
               password.charAt(12) == 'H' &&
               password.charAt(20) == 'c' &&
               password.charAt(14) == '_' &&
               password.charAt(6)  == 'm' &&
               password.charAt(24) == '5' &&
               password.charAt(18) == 'r' &&
               password.charAt(13) == '3' &&
               password.charAt(19) == '4' &&
               password.charAt(21) == 'T' &&
               password.charAt(16) == 'H' &&
               password.charAt(27) == '5' &&
               password.charAt(30) == '0' &&
               password.charAt(25) == '_' &&
               password.charAt(22) == '3' &&
               password.charAt(28) == '8' &&
               password.charAt(26) == '5' &&
               password.charAt(31) == 'd';
    }
}

Flag: picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_55870d}
```


<h3>asm1 - Points: 200</h3>
What does asm1(0x610) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. Source located in the directory at /problems/asm1_1_95494d904d73b330976420bc1cd763ec.

``` shell
Flag: picoCTF{}
```


<h3>vault-door-3 - Points: 200</h3>
This vault uses for-loops and byte arrays. The source code for this vault is here: VaultDoor3.java.

``` shell
Flag: picoCTF{}
```


<h3>asm2 - Points: 250</h3>
What does asm2(0xd,0x1e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. Source located in the directory at /problems/asm2_5_19a47cfa109e75480bcd052744a7a816.

``` shell
Flag: picoCTF{}
```


<h3>vault-door-4 - Points: 250</h3>
This vault uses ASCII encoding for the password. The source code for this vault is here: VaultDoor4.java.

``` shell
Flag: picoCTF{}
```


<h3>Tapping - Points: 200</h3>
Theres tapping coming in from the wires. What's it saying nc 2019shell1.picoctf.com 49914.

``` shell
Flag: picoCTF{}
```


<h3>asm3 - Points: 300</h3>
What does asm3(0xd46c9935,0xdfe28722,0xb335450f) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. Source located in the directory at /problems/asm3_2_376e88472c6a9317470a12cc31d506a4.

``` shell
Flag: picoCTF{}
```


<h3>vault-door-5 - Points: 300</h3>
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: VaultDoor5.java.

``` shell
Flag: picoCTF{}
```


<h3>vault-door-6 - Points: 350</h3>
This vault uses an XOR encryption scheme. The source code for this vault is here: VaultDoor6.java.

``` shell
Flag: picoCTF{}
```


<h3>vault-door-7 - Points: 400</h3>
This vault uses bit shifts to convert a password string into an array of integers. Hurry, agent, we are running out of time to stop Dr. Evil's nefarious plans! The source code for this vault is here: VaultDoor7.java.

``` shell
Flag: picoCTF{}
```
