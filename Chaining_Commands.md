# CHAINING COMMANDS

## Chaining with Semicolon 

We chain `/challenge/pwn` and `/challenge/college` using `;` the required command to get the flag is : `challenge/pwn; /challenge/college`

Flag : `pwn.college{8RZC24OT5hjRdN_fG--z6JAJqdI.dVTN4QDLwgTN0czW}`

## Building on Success

AND operator &&  is used such that the second program runs only if the first one succeeds.
` /challenge/first-success`
`/challenge/first-success && /challenge/second`

Flag : `pwn.college{cM8qIQsDocOUiQfV6sDjP9QVrG0.QXyQzM4EDLwgTN0czW}`


## Handling Failure

OR operator ||: run the second command only if the first command fails.
`/challenge/first-failure || /challenge/second`

Flag: ` pwn.college{U1vPU9IhdpEAw8xSBH1TsUNsIur.QXzQzM4EDLwgTN0czW}`


## Your First Shell Script

First we create `x.sh` using `nano` command like so , `nano x.sh` then run the command : `/challenge/pwn` and `/challenge/college` and then run `bash x.sh` to get the flag 

Flag : `pwn.college{waVKfWADgPRGfCnqdHH4w73bimN.dFzN4QDLwgTN0czW}`


## Redirecting Script Output

Th output of `x.sh` is piped into ` /challenge/solve` which can be done by the command , `bash x.sh | /challenge/solve` 

Flag : `pwn.college{IhoPPJy1TA9uL1gGl5KB12Q3iOi.dhTM5QDLwgTN0czW}`


## Eexecutable Shell Scripts

We create a script called `script.sh` using `nano`in which we enter the command `/challenge/solve` after saving we enter `chmod +x script.sh` and run it using ` ./script.sh` 

Flag : `pwn.college{4oAMh8eBbdzIBbhn6MTN-NL08pZ.dRzNyUDLwgTN0czW}`


## Understanding Shebangs

A shebang (#!) at the very first line of a file tells the kernel which interpreter should run the file (for example #!/bin/bash for bash). For this challenge I created `/home/hacker/solve.sh `with `#!/bin/bash` as the first line and a single output line echo "hack the planet". I made the file executable with `chmod +x` s

Flag:`pwn.college{ocVgap2XJIXg0QIT_adK0TR0l5c.QX5MzM4EDLwgTN0czW}`


## Scripting With Arguments 

When you run a shell script with words after its name, those words become positional parameters inside the script: $1 is the first argument, $2 the second, etc.
The challenge required a script /home/hacker/solve.sh that takes two arguments and prints them in reverse order (second then first).
Minimal solution (place this in /home/hacker/solve.sh with #!/bin/bash as the first line and make it executable):

Flag : `pwn.college{sDJvmiV_Ma488SZCnt2vYRUVTa5.QX1MzM4EDLwgTN0czW}`


## Scripting With Conditionals

Create `/home/hacker/solve.sh` which takes one argument. If the argument equals pwn the script prints college; for any other input it prints nothing.

Flag:`pwn.college{cT8piBAVS-sgOjsBx1tt5wTxI9P.QX2MzM4EDLwgTN0czW}`


## Scripting with Default Cases

The script reads the first command-line argument ($1) and uses a bash if ... else conditional to compare it to the string pwn. If the comparison succeeds the script prints college; otherwise the else branch prints nope

Flag:`pwn.college{4fOjIx55v1fgeHureesflmeIfCl.QX3MzM4EDLwgTN0czW}`

## Scripting with Multiple Conditions

It reads the first command-line argument ($1) and checks it against three possible values: `hack`, `pwn`, and `learn`. Depending on the match the script prints the corresponding response: `the planet` for hack, `college` for pwn, and `linux` for learn using `if` ,`else` and `elif`.

Flag:`pwn.college{QkxR15Fqw5A3D9LoUU9-AqY_9qz.QX4MzM4EDLwgTN0czW}`

## Reading Shell Scripts

We first run `cat /challenge/run` from which we can figure out the password is `hack the PLANET` after which we run `echo 'hack the PLANET' | /challenge/run`

Flag : `pwn.college{YQfiCo9K0QtrjU8svqTIDE2vtT7.QXyADO4EDLwgTN0czW}`





