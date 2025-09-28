# Challenge 1 (The Root)
the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs, and, most importantly, flags. In this level, we've added a program right in /, called pwn, that will give you the flag.

## solution 
a program can be invoked by providing its path in the command line, the style of path, one that starts with the root directory, is referred to as an "absolute path".
hence here the the pwn program can be invoked by the absolute path like,

```sh
/pwn
```

## Flag:

```
pwn.college{0S3L5XmbbE9NFY_fu_3wXN9BCsN.QX4cTO0wSOyAzNzEzW}
```

# Chanllenge 2 (Program and absolute paths)
challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

##solution 
first excute the the absolute path and then excute the run file that is in the challenge directory.

```sh
/chanllenge/run
```

## Flag;

```
pwn.college{Yp4RctlETzKAZZkXJNODn6qfRxP.QX1QTN0wSOyAzNzEzW}
```

# Challenege 3(Position thy self)
The Linux filesystem has tons of directories with tons of files, we can navigate around the directories using the change directory(cd) and passing a path to it as an argument.


## solution
excuting /challenge/run from a specific path i.e. /home. 

```sh
/home
cd /home
/challenge/run
```

## flag

```
pwn.college{Uc6ZQ1J9K8II2ETC0v6eIndLSWz.QX2QTN0wSOyAzNzEzW}
```

# challenge 4(position elsewhere)
 navigate around directories by using the cd (change directory) command and passing a path to it as an argument.
 This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

 ## solution
 This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program.

```sh
/challenge/run
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately.
cd /usr/share/doc/fontconfig
/usr/share/doc/fontconfig$ /challenge/run
```

## flag

```
pwn.college{sJz-9zLD0FPdRLSWoBh96_u-50c.QX3QTN0wSOyAzNzEzW
```


# challenge 5 (position elsewhere)
navigate around directories by using the cd (change directory) command and passing a path to it as an argument,
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.


## solution
This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program.
look for it by first excuting /challenge/run to figure out which directory to invoke.

```sh
/challenge/run
Incorrect...
You are not currently in the /sys/kernel directory.
Please use the `cd` utility to change directory appropriately.
cd /sys/kernel
/sys/kernel$ /challenge/run
```

## flag

```
pwn.college{Izt-C7zjNYKvfKZACWx7vIWBaTO.QX4QTN0wSOyAzNzEzW}
```


# challenge 6 (implict relative paths, from)
