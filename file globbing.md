# challenge 1 (matching with *)

## flag 
```sh
pwn.college{IdNDwKHs6Dtm5zYthjrtd0ouMN3.QXxIDO0wSOyAzNzEzW}
```

# challenge 2 (matching with ?)

## flag 
```sh
```

# Challenge 3 (matching with [])

## flag
```sh
pwn.college{sQ1HHHUoVcc9RHoYDTmBVNp9l_B.QXzIDO0wSOyAzNzEzW}
```

# challenge 4 (matching paths with [])
Globbing happens on a path basis, so you can expand entire paths with your globbed arguments.

## solution 
we've placed a bunch of files in /challenge/files. Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files

```sh
/challenge/run /challenge/files/file_[absh]
You got it! Here is your flag
```

## flag
```sh
pwn.college{AnxsXIySu8Gd7Ln2i1K-XpDDaAj.QX0IDO0wSOyAzNzEzW}
```

# challenge 5 
Bash supports the expansion of multiple globs in a single word.

## solution 
We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.

```sh
cd /challenge/files
/challenge/run *p*
You got it! Here is your flag!
```

## flag
```sh
pwn.college{U3GH1DLd1u1pFC-wKZOzfKQhFMZ.0lM3kjNxwSOyAzNzEzW}
```
