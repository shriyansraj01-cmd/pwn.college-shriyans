# challenge 1
One of the purposes of piping data is to modify it. Many Linux commands will help you modify data in really cool ways. One of these is tr, which translates characters it receives over standard input and prints them to standard output

## solution 
In this level, /challenge/run will print the flag but will swap the casing of all characters (e.g., A will become a and vice-versa).
using tr command to the flag accordingly 

```
/challenge/run 
Your case-swapped flag:
PWN.COLLEGE{8tPRlQvcmMPkbIdfBk8j7MMFYt4.01mXeZnXWsoYaZnZeZw}
echo PWN.COLLEGE{8tPRlQvcmMPkbIdfBk8j7MMFYt4.01mXeZnXWsoYaZnZeZw} | tr '[:lower:][:upper:]' '[:upper:][:lower:]'
pwn.college{8TprLqVCMmpKBiDFbK8J7mmfyT4.01MxEzNxwSOyAzNzEzW}
```

## flag 
```
pwn.college{8TprLqVCMmpKBiDFbK8J7mmfyT4.01MxEzNxwSOyAzNzEzW}
```

### notes 
used the command 
tr --help to obtain information about '[:lower:][:upper:] 
```
tr --help
Usage: tr [OPTION]... STRING1 [STRING2]
Translate, squeeze, and/or delete characters from standard input,
writing to standard output.  STRING1 and STRING2 specify arrays of
characters ARRAY1 and ARRAY2 that control the action.

  -c, -C, --complement    use the complement of ARRAY1
  -d, --delete            delete characters in ARRAY1, do not translate
  -s, --squeeze-repeats   replace each sequence of a repeated character
                            that is listed in the last specified ARRAY,
                            with a single occurrence of that character
  -t, --truncate-set1     first truncate ARRAY1 to length of ARRAY2
      --help        display this help and exit
      --version     output version information and exit

ARRAYs are specified as strings of characters.  Most represent themselves.
Interpreted sequences are:

  \NNN            character with octal value NNN (1 to 3 octal digits)
  \\              backslash
  \a              audible BEL
  \b              backspace
  \f              form feed
  \n              new line
  \r              return
  \t              horizontal tab
  \v              vertical tab
  CHAR1-CHAR2     all characters from CHAR1 to CHAR2 in ascending order
  [CHAR*]         in ARRAY2, copies of CHAR until length of ARRAY1
  [CHAR*REPEAT]   REPEAT copies of CHAR, REPEAT octal if starting with 0
  [:alnum:]       all letters and digits
  [:alpha:]       all letters
  [:blank:]       all horizontal whitespace
  [:cntrl:]       all control characters
  [:digit:]       all digits
  [:graph:]       all printable characters, not including space
  [:lower:]       all lower case letters
  [:print:]       all printable characters, including space
  [:punct:]       all punctuation characters
  [:space:]       all horizontal or vertical whitespace
  [:upper:]       all upper case letters
  [:xdigit:]      all hexadecimal digits
  [=CHAR=]        all characters which are equivalent to CHAR

Translation occurs if -d is not given and both STRING1 and STRING2 appear.
-t is only significant when translating.  ARRAY2 is extended to length of
ARRAY1 by repeating its last character as necessary.  Excess characters
of ARRAY2 are ignored.  Character classes expand in unspecified order;
while translating, [:lower:] and [:upper:] may be used in pairs to
specify case conversion.  Squeezing occurs after translation or deletion.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report any translation bugs to <https://translationproject.org/team/>
Full documentation <https://www.gnu.org/software/coreutils/tr>
or available locally via: info '(coreutils) tr invocation'
```

# Challenge 2
tr can also translate characters to nothing (i.e., delete them). This is done via a -d flag and an argument of what characters to delete

## solution 
```
/challenge/run
Your character-stuffed flag:
p^%w^%n^%.col^l^%e^g^%e^%{^I^lW%S%C^YP^%Hs%S^3^P^%K^D%t%u^4^o^%G^n%W^%4J%yU%1p%.^0^%F^%N%x^E^z^%N^xw%S^%O^y^%A%zN^%z%Ez^W}
echo p^%w^%n^%.col^l^%e^g^%e^%{^I^lW%S%C^YP^%Hs%S^3^P^%K^D%t%u^4^o^%G^n%W^%4J%yU%1p%.^0^%F^%N%x^E^z^%N^xw%S^%O^y^%A%zN^%z%Ez^W} | tr -d ^
p%w%n%.coll%eg%e%{IlW%S%CYP%Hs%S3P%KD%t%u4o%Gn%W%4J%yU%1p%.0%F%N%xEz%Nxw%S%Oy%A%zN%z%EzW}
echo p%w%n%.coll%eg%e%{IlW%S%CYP%Hs%S3P%KD%t%u4o%Gn%W%4J%yU%1p%.0%F%N%xEz%Nxw%S%Oy%A%zN%z%EzW} | tr -d %
pwn.college{IlWSCYPHsS3PKDtu4oGnW4JyU1p.0FNxEzNxwSOyAzNzEzW}
```

## flag 
```
pwn.college{IlWSCYPHsS3PKDtu4oGnW4JyU1p.0FNxEzNxwSOyAzNzEzW}
```
# challenge 3
A common class of characters to remove is a line separator. This happens when you have a stream of data that you want to turn into a single line for further processing. You can specify newlines almost like any other character, by escaping them:

## solution 
```
/challenge/run
Your line-split flag: 
p
w
n.
co
l
l
e
ge{
s
e
h
5
x_Bk
z
yQ
tw
bI
H
7
0x
rG
0
j
X
R
Ud
.
0V
N
x
Ez
Nx
w
S
OyA
z
NzEzW
}
```

## flag 
```
pwn. college{seh5x_BkzyQtwbIH70xrG0jXRUd.0VNxEzNxwSOyAzNzEzW}
```

# challenge 5
Sometimes, you want to grab specific columns of data, such as the first column, the third column, or the 42nd column. For this, there's the cut command.

## solution 
In this challenge, the /challenge/run program will give you a bunch of lines with random numbers and single characters (characters of the flag) as columns. Use cut to extract the flag characters, then pipe them to tr -d "\n" (like the previous level!) to join them together into a single line. Your solution will look something like /challenge/run | cut ??? | tr ???, with the ??? filled out.

```
/challenge/run 
15151 p
16639 w
17382 n
20597 .
22273 c
12376 o
6150 l
25615 l
11866 e
8754 g
5928 e
26428 {
7748 8
3833 4
4978 _
14600 g
24144 X
22554 2
9449 r
29742 X
8671 J
22016 B
6737 _
27501 u
19236 o
12374 L
3987 l
4952 4
3827 V
2484 m
16000 8
19487 r
11020 y
20734 Y
28435 g
28210 P
9907 x
16504 a
10798 1
28674 .
10118 0
24190 1
20288 N
9077 x
30299 E
28289 z
25381 N
17260 x
6463 w
5466 S
30877 O
5008 y
29180 A
32270 z
373 N
12819 z
13511 E
8876 z
28499 W
25595 }
/challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{84_gX2rXJB_uoLl4Vm8ryYgPxa1.01NxEzNxwSOyAzNzEzW}
```

## flag 
```
pwn.college{84_gX2rXJB_uoLl4Vm8ryYgPxa1.01NxEzNxwSOyAzNzEzW}
```

# challenge 6 
Files (or output lines of commands) aren't always in the order you need them! The sort command helps you organize data. It reads lines from input (or files) and outputs them in sorted order:

## solution 
In this challenge, there's a file at /challenge/flags.txt containing 100 fake flags, with the real flag mixed among them. When sorted alphabetically, the real flag will be at the end
```
sort /challenge/flags.txt
```

## flag 
```
pwn.college{M0yCh38UPGhRz3O7g4bRXHv_Ip2.0FM0MDOxwSOyAzNzEzW}
```


