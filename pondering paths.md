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


# challenge 6 (implict relative paths, / from)
About relative paths
A relative path is any path that does not start at root (i.e., it does not start with /).
A relative path is interpreted relative to your current working directory (cwd).
Your cwd is the directory that your prompt is currently located at.
This means how you specify a particular file, depends on where the terminal prompt is located.

Imagine we want to access some file located at /tmp/a/b/my_file.

If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
If my cwd is /tmp, then a relative path to the file is a/b/my_file.
If my cwd is /tmp/a/b/c, then a relative path to the file is ../my_file. The .. refers to the parent directory.

## solution 
run /challenge/run using a relative path while having a current working directory of /.

```sh
cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
```

## flag 
pwn.college{gTOQyBWIQnde8n18QtubZ0BIZFQ.QX5QTN0wSOyAzNzEzW}


# challenge 7 
The previous relative path was "naked": it directly specified the directory to descend into from the current directory. Noe, we're going to explore more explicit relative paths.
In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: . and ... The first, ., refers right to the same directory, so the following absolute paths are all identical to each other:
```sh
/challenge
/challenge/.
/challenge/./././././././././
/./././challenge/././
```
The following relative paths are also all identical to each other:
```sh
challenge
./challenge
./././challenge
challenge/.
```

## solution 
```sh
cd /
./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
```

##flag
```sh
pwn.college{0GqZ7Z2WMjF-TIVKMqFZxrRXkYI.QXwUTN0wSOyAzNzEzW}
```

# challenge 8
In this level, we'll practice referring to paths using . a bit more. This challenge will need you to run it from the /challenge directory. 

## solution 
in this challenge, we'll learn how to explicitly use relative paths to launch run in this scenario. The way to do this is to tell Linux that you explicitly want to execute a program in the current directory, using . like in the previous levels.

```sh
cd /challenge
./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
```

## flag 
```
pwn.college{MXdxbzVDhqAh3bY3vMfljL4ek4X.QXxUTN0wSOyAzNzEzW}
```

# challenge 9

## solution 
In this challenge, /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:

Your argument must be an absolute path.
The path must be inside your home directory.
Before expansion, your argument must be three characters or less.
Again, you must specify your path as an argument to /challenge/run as so:

```sh
challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
```

# flag 
```sh 
pwn.college{cu_sn3ljN1aIEfknN31uzsH-zrU.QXzMDO0wSOyAzNzEzW}
```




