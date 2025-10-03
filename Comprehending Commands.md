# Challenge 1 (cat: not the pet, the command)
One of the most critical Linux commands is cat. cat is most often used for reading out files.
cat can concatenate multiple files if provided multiple arguments. 

```sh 
hacker@dojo:~$ cat myfile
This is my file!
hacker@dojo:~$ cat yourfile
This is your file!
hacker@dojo:~$ cat myfile yourfile
This is my file!
This is your file!
```

## solution 

```sh 
/home
bash: /home: Is a directory
cat flag
pwn.college{4Ttd54pJKnFBv2v_V7xbGksT9Uc.QXxcTN0wSOyAzNzEzW}

## Flag
```sh
pwn.college{4Ttd54pJKnFBv2v_V7xbGksT9Uc.QXxcTN0wSOyAzNzEzW}
```

# Challenge 2(catting absolute paths)
In the last level, you did cat flag to read the flag out of your home directory! You can, of course, specify cat's arguments as absolute paths:


## solution 
this time the flag isn't available at the home directory.

```sh
cat /flag
pwn.college{YX4tHBKKBs1oM66nm4bpYDAxm-C.QX5ETO0wSOyAzNzEzW}
```

# Challenge 3 (comparing files)
When looking for changes between similar files, eyeballing them might not be the most efficient approach! This is where the diff command becomes invaluable.

diff compares two files line by line and shows you exactly what's different between them. For example:

```sh
hacker@dojo:~$ cat file1
hello
world
hacker@dojo:~$ cat file2
hello
universe
hacker@dojo:~$ diff file1 file2
2c2
< world
---
> universe
```

## solution 
compare the two files /challenge/decoys_only.txt
/challenge/decoys_and_real.txt using diff

```sh
diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
97a98
> pwn.college{Uj_PwpB5GvSjpiDIrcySN2hxZwW.01MwMDOxwSOyAzNzEzW}
```

## flag:

```
pwn.college{Uj_PwpB5GvSjpiDIrcySN2hxZwW.01MwMDOxwSOyAzNzEzW}
```

# Challenge 4 (listing files)
directories can have lots of files (and other directories) inside them, we can read or list those files using ls command.

## solution 
```sh
ls /challenge
29989-renamed-run-22030  DESCRIPTION.md
/challenge/29989-renamed-run-22030
Yahaha, you found me! Here is your flag:
```

## flag 
```sh
pwn.college{IMD-R1ddXjz3Oba02aflEnpP8aW.QX4IDO0wSOyAzNzEzW}
```

# Challenge 5 (touching files)

## flag:
pwn.college{0iz9LzTNk08NfxDB-Wu1NUVnx4f.QXwMDO0wSOyAzNzEzW}


# Challenge 6 (removing files)



## flag:
pwn.college{Q4cjU-5iOA6oZEqa_cxLH0dI8oL.QX2kDM1wSOyAzNzEzW}


# challenge 7 (moving files)
We can also move files around with the mv command.

## solution 
This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

```sh
 mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
/challenge/check 
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
```

## flag 
```sh
pwn.college{cCaMtn52poJFspC-pyfELvTSk0C.0VOxEzNxwSOyAzNzEzW}
```

# challenge 8 (hidden files)
Interestingly, ls doesn't list all the files by default. Linux has a convention where files that start with a . don't show up by default in ls and in a few other contexts. To view them with ls, you need to invoke ls with the -a flag.

## solution 
the flag hidden as a dot-prepended file in /.

```sh
cd /
ls -a
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-5063944529588  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
cat /.flag-5063944529588
```

## flag 
```
pwn.college{Mu2iBueGf0qpYXP6_sl_PLNWwui.QXwUDO0wSOyAzNzEzW}
```

# challenge 9 (epic filesystem quest)


