# COMPREHENDING COMMANDS

##  Cat Command

We learn about a very crucial command known as "cat" , it is used read out the files but more importantly  to concatenate . To obtain the flag we use the cat command to
concatenate the flag file in the home directory ;`cat flag` 

Flag : `pwn.college{Y6pw3DtCARn5wQoanxHFMGXbkK_.dFzN1QDLwgTN0czW}`


## Catting Absolute Paths

We use the cat command to concatenate the flag file from its absolute path like so : `cat /flag` to obtain the flag which marks the successful compeltion of the challenege 

Flag : `pwn.college{8Bx1vgHmuBQaN6KiQdalgR6dHti.dlTM5QDLwgTN0czW}`


## More Catting Practice

In this challenge we learn how to retrieve the flag when it is in a different directory using cat command ; `cat /lib/ispell/flag`

Flag : `pwn.college{0nj_U2So9CSVqtB6tx2jogxJ5--.dBjM5QDLwgTN0czW}`


## Grepping

When the files we obtain out of concatenating become too complex we can use the grep command . 
The format for the grep command is as follows : `hacker@dojo:~$ grep SEARCH_STRING /path/to/file"`
The flag is in the path  `/challenge/data.txt` and the flag always starts `pwn.college` 
The line of code is `grep pwn.college /challenge/data.txt"`

Flag : `pwn.college{Y-hCItgkclHTcCsnWpoC9Axjr_c.ddTM4QDLwgTN0czW}`


## Comparing Files 

`diff` compares two files line by line and shows you exactly what's different between them . 
We are given two files `/challenge/decoys_only.txt` contains 100 fake flags and `/challenge/decoys_and_real.txt` contains all 100 fake flags plus the one real flag. 
We use diff command to find the flag ` diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt`

Flag :`pwn.college{0EKVkpARam9Y1vaialRtsDGIB3L.QXzAzM4EDLwgTN0czW}`

## Listing Files

We learn about "ls" command which allows us to list the files present in our desktop , We were asked to list files present in a specific directory called "challenge" ,
on opening that files we will recieve the file location for the `/challenge/run` file . Which is `11381-renamed-run-24925`
` cd /challenge`
` ls`
`./11381-renamed-run-24925`

Flag : `pwn.college{UaDTnPL-qLnlLu2aIR2GpCO6dZ7.dhjM4QDLwgTN0czW}`

## Touching Files

To create blank files of our own we use the "touch" command .  In this level, we create two files: `/tmp/pwn` and `/tmp/college`, and run `/challenge/run` to get the flag 

Flag: `pwn.college{I4drQUrzL6X0S0ElwUW95oULoU2.dBzM4QDLwgTN0czW}`

## Removing Files

As important it is to create a file , it is to delete it ,for that `rm` command is used . In this challenge , we create a file called
`delete_me` using touch command which we learned previosuly and then proceed to delete it using "rm" command . Later , run `/challenge/check`
to check whether the file has been successfully deleted or not . 

Flag : `pwn.college{cDjL-XQdAsw1JLjF8jh0Ci-VqaD.dZTOwUDLwgTN0czW}`

## Moving Files 

In this challege , we learned how to move one file to another . To get the flag ,we move the `/fla`g file into `/tmp/hack-the-planet` and run `/challenge/check` to obtain the flag

Flag :`pwn.college{obVXvYn9SCx14Vfzp5sKBK4hQjb.QX5ETM3EDLwgTN0czW}`

## Hidden Files

We us the `ls -a` command to access the "hidden files" in the system , after running which we get a flag address ie `.flag-130802970017550`
Therefore the run the following lines of command to get the flag 
`cd /
ls -a
cat .flag-130802970017550`

Flag : `pwn.college{oHR6b2C4e3rIZX69lVnMPl-Q2Sh.dBTN4QDLwgTN0czW}`

## Filesystem Quest

In this challenge we learn how to use the commands `ls-a` , `cat` , `cd` etc effectively to obtain the flag , below given screenshots represnt the same 

Flag :`pwn.college{UmcNQI9iibhVYdJRZBI6GqoV2GK.dljM4QDLwgTN0czW}`


`<img width="1317" height="720" alt="Screenshot 2025-09-29 at 11 56 08 am" src="https://github.com/user-attachments/assets/329874fd-bdf0-4440-ac1c-696b9db2b10b" />

<img width="951" height="505" alt="Screenshot 2025-09-29 at 11 55 56 am" src="https://github.com/user-attachments/assets/f027a6d3-92d8-4ab2-bdea-9e54efbeb699" />

##  Making Directories

We learn about a command called "mkdir" to make directories . In this challlenge we make a directory called `/tmp/pwn` in which we make a file called `college` and later run the code`/challenge/run` to check whether the file has been created succesfully and on completion we receive a flag .

Flag : `pwn.college{cYcGI1mTV-BA3yNlSUsSL8IRzDo.dFzM4QDLwgTN0czW}`

## Finding Files 

To find a file in the provided system we use `find` command . On running the command , `find / -name flag` , many files appear on the 
screen out of which we use `cat` commmand to find out which has the required flag 
In the given case the flag was found in the `/usr/lib/python3/dist-packages/sage/modules/__pycache__/flag` file 

Flag : `pwn.college{wBFUcuFlmeYW2tQqIzDe0BJetqB.dJzM4QDLwgTN0czW}`

## Linking Files

In this challenge we are taught to link files to one another . Executing the follwing code will retrive us the flag which marks the successful completion of this challenge : 
`ln -s /flag not-the-flag`
`/challenge/catflag`

Flag : `pwn.college{kDfFXk0uRLO-3dbrgexuZ_IoiU9.dlTM1UDLwgTN0czW}`






