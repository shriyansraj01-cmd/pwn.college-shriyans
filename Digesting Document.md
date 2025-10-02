# Challenge 1 (Learning from Documentation)

## Flag:
```sh
pwn.college{k2vqVzXd5uXKjVEbVWyNjI-7-Gz.QX0ITO0wSOyAzNzEzW}
```

# Challenge 2 (Learning Complex Usage)
While using most commands is straightforward, the usage of some commands can get quite complex. For example, the arguments to commands like sed and awk, which we're definitely not getting into right now, are entire programs in an esoteric programming language! Somewhere on the spectrum between cd and awk are commands that take arguments to their arguments.

## solution 
/challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
## Flag:
```sh
pwn.college{o9CCP65oZpH7U-tG4v2UuAGeuH4.QX1ITO0wSOyAzNzEzW}
```

# Challenge 3 (reading manuals)

## solution 
man challenge
challenge/challenge --zqqsbd 054
Correct usage! Your flag:

## flag:
```sh
pwn.college{05IzJNqYE49PMJ5U4qs-Cb5F5dk.QX0EDO0wSOyAzNzEzW}
```

# challenge 4 (searching manuals)

## flag:
```sh
pwn.college{gYtTdZRFrU7ZbRuogYEU_yH89vt.QX1EDO0wSOyAzNzEzW}
```
# challenge 5 (searching for manuals)


# challenge 6 (helpful programs)

## flag:
```sh
pwn.college{IHjxJB7rGVPshlroBxRrffJCLWZ.QX3IDO0wSOyAzNzEzW}
```

# challenge 7 (help for bulitins)
Some commands, rather than being programs with man pages and help options, are built into the shell itself. These are called builtins. Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs.

## solution 
help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "AMwSh4EW".
    challenge --secret AMwSh4EW
Correct! Here is your flag!

## flag: 
```sh
pwn.college{AMwSh4EWDad_HMVcvtpsarpRCd7.QX0ETO0wSOyAzNzEzW}
```
