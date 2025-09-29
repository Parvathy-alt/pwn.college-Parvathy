# DIGESTING DOCUMENTATION 

## LEARNING FROM DOCUMENTATION 

The challenge shows us how command-line arguments (like -a for ls) change a program’s behavior.
To complete the following task it is required to run the command `/challenge/challenge` alongside the command `--giveflag` to obtain the flag 
Flag : `pwn.college{Ir6ASnSgR1SDR-zBYX3S8zD6Qlr.dRjM5QDLwgTN0czW}`


## Learning Complex Usage 


## READING MANUALS

In this challenge we learn how to use the man command which is used to read manuals . On running `man challenge` we recieve multiple descriptions out of which the one which is required 
to attain the flag is 
` --hxibcn NUM
print the flag if NUM is 031`
According the the following description we run the command "/challenge/challenge --hxibcn 031" to get the flag 
Flag :  `pwn.college{0hxib3JcT1npV_Wwkogyawd3e8B.dRTM4QDLwgTN0czW}`

## Searching Manuals

We run `man challenge` to find the location of the flag amongst the manuals , specifically to filter out the flag we use `/flag` which leads us to a command `--vtds This argument will give you the flag` is found 
After which we type the command : 
`/challenge/challenge   --vtds` which gives us the flag , which is 
Flag : ` pwn.college{U56U6Tnk7za02WSFBFJz6AFTq_X.dVTM4QDLwgTN0czW}`

## Searching for Manuals

When  the comand `man -k flag` . The following output is obtained :

dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
fiubkatmhe (1)       - print the flag!
i386 (8)             - change reported architecture in new program environment and/or set personality flags
ioctl_iflags (2)     - ioctl() operations for inode flags
linux32 (1)          - change reported architecture in new program environment and/or set personality flags
linux64 (1)          - change reported architecture in new program environment and/or set personality flags
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of valid...
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of ...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of vali...
setarch (1)          - change reported architecture in new program environment and/or set personality flags
setarch (8)          - change reported architecture in new program environment and/or set personality flags
x86_64 (8)           - change reported architecture in new program environment and/or set personality flags

Out of which we can observe that "fiubkatmhe" command will obtain us the flag 
To get the required flag : `/challenge/challenge  --fiubka 646` is printed 
Flag :`pwn.college{MfYiubkEXO6Z4UQGVaHtm6h0eOI.dZTM4QDLwgTN0czW}`

## Helpful Programs

We run the command `/challenge/challenge --help` which provides us a list of optional arguments eg : -h,--help and -p, --print-value
After which we type the command : "/challenge/challenge -p" which  provides us with a secret value ie 278 . Once we recive that value we execute the command : `/challenge/challenge -g 278`.
Flag : `pwn.college{EM2oLW7jmi8Q1DU0_M2nIQUacdY.ddjM4QDLwgTN0czW}`

## Help For Builtins.

In this challenge we learned about builtins and where they can be used . Built-in commands are executed like regular commands, but the shell processes them internally 
rather than starting external programs.
We execute the command `help challenge` after which we recieve a secret command and execute it as well `challenge --secret Qt9oB8rk`
Flag : `pwn.college{Qt9oB8rkN6NUlRbdOXNEy0htKSV.dRTM5QDLwgTN0czW}`
