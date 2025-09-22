# Intro to commands
In this challenge, you will invoke your first command! When you type a command and hit enter, the command will be invoked, as so:

```

hacker@dojo:~$ whoami
hacker
hacker@dojo:~$
```
Here, the user executed the whoami command, which simply prints the username (hacker) to the terminal. When the command terminates, the shell once again displays the prompt, ready for the next command.

## solution:
once the terminal comes up, we are required to invoke the '''hello''' command, which prints the flag

#### commands run:
```sh

$hello
```

## flag:
```
pwn.college{Qbbz66Xxccz2hBhcDs-0ROxBFuN.QX3YjM1wSOyAzNzEzW}
```

### notes:


# Intro to Arguments
a command with arguments, which is what we call additional data passed to the command. When you type a line of text and hit enter, the shell actually parses your input into a command and its arguments. The first word is the command, and the subsequent words are arguments.

```sh

hacker@dojo:~$ echo Hello
Hello
hacker@dojo:~$
```

here the command was echo, the primary use of echo is to print text to the console, and the argument was Hello.

echo can be used with multiple arguments as well.
```sh

hacker@dojo:~$ echo Hello Hackers!
Hello Hackers!
hacker@dojo:~$
```

In this case, the command was echo, and Hello and Hackers! were the two arguments to echo. 

## solution:

after the termianl comes up, the user needs to invoke '''hello''' as the command for the argument '''hackers'''

#### command run:

```sh
$ hello hackers
```

## flag:
```

pwn.college{8_mHbucX3fkW4W335d3Vj4-SOo6.QX4YjM1wSOyAzNzEzW}
```

### notes:
In this challenge, to get the flag, you must run the hello command (NOT the echo command) with a single argument of hackers.

# Command History
There is a way to avoid writing everything from scratch, the shell saves a hstory of every command that has been invoked. 
We can scroll throuh those saved commands with the up/down arrow keys.

## solution:
here the flag is aready in our command histroy (immediate pervious command)

#### commands run:
```up``` arrow to scroll to the last command

## flag:

```
pwn.college{cKAyw1_4P4j45FYhMnjHKsfWOiR.0lNzEzNxwSOyAzNzEzW}
```

# notes:
At the command prompt, press the Up Arrow key. Each press will display the command executed immediately before the current one, moving further back in your command history.
If you have moved back in the history and want to see more recent commands, press the Down Arrow key. Each press will move you forward through the history, closer to the most recently executed commands.
