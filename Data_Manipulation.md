# DATA MANIPULATION 


## Translating Characters

tr is a filter that translates characters from stdin to stdout. 
Give it two sets of characters and it replaces each character from the first set with the corresponding one in the second set.
`/challenge/run | tr 'A-Za-z' 'a-zA-Z'`
Flag:`pwn.college{oqQjwckDsKKb2Fx_hGxhi87qOre.QXzETM3EDLwgTN0czW}`


## Deleting Characters

tr can also translate characters to nothing (i.e., delete them). This is done via a -d flag and an argument of what characters to delete:
`/challenge/run | tr -d '^%'`
Flag : `pwn.college{oy0tT0J2t-Vm8tYgu_nCF7es7Cl.QX0ETM3EDLwgTN0czW}`


## Deleting New Lines

Newlines are represented with \n, but because \ is an escape character you must quote it so the shell passes \n to tr (not an actual line break)
`/challenge/run | tr -d '\n'`
Flag:`pwn.college{IJzWFTNHSLKdn_AZuzND1daNexg.QX1ETM3EDLwgTN0czW}`


## Extracting First Lines With Head

It teaches you how to take the first few lines of a program’s output and feed those lines into another program. The concrete goal in the challenge: run /challenge/pwn, keep the first 7 lines of its output, and pipe those 7 lines as input to /challenge/college. If the lines are what /challenge/college expects, it will output the flag.
`/challenge/pwn | head -n 7 | /challenge/college`
Flag:`pwn.college{gFWblgJshdu-0ZJnFVl45Eu3q4y.QX2ETM3EDLwgTN0czW}`

## Extracting Specific Sections of the text

Use cut to pick the column that contains the flag characters, then tr -d '\n' to join them into one line.
`/challenge/run | cut -d ' ' -f 2 | tr -d '\n'` , the flag elements are present in the second column.
Flag : `pwn.college{IrNpeJJ5ngj8czVV1fkUEZUYM5P.QX3ETM3EDLwg}`

## Sorting Data

`sort` by default sorts alphabetically (A→Z) ;
-r reverse (Z→A)
-n numeric sort
-u remove duplicates
-R randomize
After sorting alphabetically, the real flag will be at the end  ; `sort -r /challenge/flags.txt | head -n 1`
Flag :`pwn.college{gQglyV3UkM_3-yXgPXZQnPl5HEV.QXwQzM4EDLwgTN0czW}`






