# PRACTICING PIPING 


## Redirecting Output

In this challenge we learn about the "echo" command and adding a " > " after the echo command will redirect the output of the echo command to the file mentioned after the " > " symbol 
We run : `echo PWN > COLLEGE ` which basically redirectes the output "PWN" to the file "COLLEGE" 
Flag: `pwn.college{YTqg_i0f3cGFLvJqu4IwgV0HIVi.dRjN1QDLwgTN0czW}`

## Redircting more Output

To redirect the output of `/challenge/run` to `myfile`  , we use the following code `/challenge/run > myflag`  , after which we `cat myflag` 
Flag : `pwn.college{obd0qhi_eiEA6ocoMoCTu3vrmCY.dVjN1QDLwgTN0czW}`


## Appending Output

To redirect the output of  `/challenge/run` to `~/the-flag` in append mode we run the following code : `/challenge/run >> ~/the-flag `  , after which you `cat  the-flag` to get  the flag , 
Flag : ` pwn.college{gaiBP0O3FJcDG9cqPj5F7_xKA-6.ddDM5QDLwgTN0czW}`


## Redirecting Errors

In this challenge we learn about File Descriptors (FD) which is a number that describes a communication channel in Linux and we are also enligtened about how to redirect multiple files 
and so on 
The command `/challenge/run > myflag 2> instructions` is run after which we use the cat command and get the flag 
Flag : `pwn.college{ULDFaVpFG0CJBWlZYxSjcnCSKym.ddjN1QDLwgTN0czW}`


## Redirecting Input

As the name of the challenge suggest we require to "PWN" file to have value "COLLEGE" in it which will be redirected to ` /challenge/run`
To do the following we run the following lines of code : ` /challenge/run < PWN`
Flag : `pwn.college{wL3bjcPv5Ttg3Ejj7KwUgMYf-XA.dBzN1QDLwgTN0czW}`


## Grepping Stored Reuslt 

We will be using a command known as "grep" which we have learned before to complete this challenge :
First we redirect output of `/challenge/run` to `/tmp/data.txt.` after which we use the said grep command to obtain the flag 
`grep pwn.college /tmp/data.txt`
Flag : `pwn.college{8AIgXGn3_29aiuGCmsTeRov-x4V.dhTM4QDLwgTN0czW}`


## Grepping Live Output 

We got introduced to an important operator called pipe(|) , which makes searching for required data amongst pool of unwanted text much easier 
In this challenge we are asked to search for the key in `/challenge/run` by using " | " operator we get the required flag right away 
Command : `/challenge/run|grep pwn.college` 
Flag : `pwn.college{8j2F4LoZlBWH2eW-7-22lKY1GFX.dlTM4QDLwgTN0czW}`


## Grepping Errors 

Every operator has its own functions , but when joined together it makes magic . In this challenge we learn about " >& " operator , which redirects a file descriptor to 
another file descriptor.
We use the above mentioned operator along with pipe(|) operator to obtain the flag , the code is as follows : 
`/challenge/run 2>& 1 | grep pwn.college` 
Flag : `pwn.college{k3RX-phRe_RObb8Y8eZAvTVR_jh.dVDM5QDLwgTN0czW}`


## Filtreing with grep -v

Use grep -v to remove lines that contain a pattern. In this challenge, /challenge/run prints one real flag plus 1000+ decoy lines that include the word DECOY; pipe the program through grep -v 'DECOY' to filter out the decoys and reveal the real flag.
` /challenge/run | grep -v "DECOY"`
Flag:`pwn.college{4c2UmgvS6-zyzamEpaIFaFlDE-j.QX4ETM3EDLwgTN0czW}`


## Duplicating Piped Data with Tee

We learn about 'tee' command in this challenge , it duplicates data flowing through your pipes to any number of files provided on the command line.
The commands required for this challenge is as follows : 
`/challenge/pwn | tee find | /challenge/college` where `find` is the command output 
`cat find`  which gives us the output :
`/challenge/pwn --secret [SECRET_ARG]`
`SECRET_ARG should be "A9Pkspou"`
After which : `/challenge/pwn --secret A9Pkspou | /challenge/college` .
Flag : `pwn.college{A9Pkspou7yjFMJ0hfM3dx-oB9JL.dFjM5QDLwgTN0czW}`


## Process Substitution for Input

Process substitution (<(command)) lets you use the output of a command as if it were a file. 
That means you don’t have to save things into temporary files before comparing them.
`diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)`
Flag:`pwn.college{sICtjxNWupnHwJc9PVOnv51ch-0.QX2AzM4EDLwgTN0czW}`

## Writing to Multiple Programs

According to the challenge given , the output from `/challenge/hack` must be piped to the 2 commands `/challenge/planet` and `/challenge/the` where `/challenge/the` is the command output
On running : `/challenge/hack | tee >(/challenge/the) | /challenge/planet` we get a flag which marks the successfull completion of the the challenge 
Flag : `pwn.college{UYL1FVfq-eLlZSsauhDBi7QDt_n.dBDO0UDLwgTN0czW}`


## Split-Piping Stderr  And Stdout

Initially, I utilized `2>` combined with `>(/challenge/the`) to direct standard error to the `/challenge/the` program.Later we use pipe(|) to stdout to `/challenge/planet`
The command is as follows : `/challenge/hack 2> >(/challenge/the) | /challenge/planet`
Flag : `pwn.college{UH1UBoKi0khlhTm9DhWvGVy5Bw7.dFDNwYDLwgTN0czW}`

## Named Pipes 

`mkfifo /tmp/flag_fifo` Creates a named pipe (FIFO) then you use cat command to read the file , `/challenge/run > /tmp/flag_fifo` redirects the standard output to FIFO
Flag: `pwn.college{M0eVvAKVg7P0z-BK-30poAvDewK.QXzMzM4EDLwgTN0czW}`








