# **Command-Line Options for ls** 
## **1. ls -l**   
Example 1:  
```
% ls -l
total 0
drwxrwxr-x@ 4 ethanlee  staff  128 Feb 13 20:43 non-fiction
drwxrwxr-x@ 5 ethanlee  staff  160 Feb 13 20:43 travel_guides
```
Example 2:  
```
% ls -l ./non-fiction/OUP
total 0
drwxrwxr-x@ 11 ethanlee  staff  352 Feb  3 08:38 Abernathy
drwxrwxr-x@  6 ethanlee  staff  192 Feb  3 08:38 Berk
drwxrwxr-x@ 16 ethanlee  staff  512 Feb  3 08:38 Castro
drwxrwxr-x@  8 ethanlee  staff  256 Feb  3 08:38 Fletcher
drwxrwxr-x@ 11 ethanlee  staff  352 Feb  3 08:38 Kauffman
drwxrwxr-x@  5 ethanlee  staff  160 Feb  3 08:38 Rybczynski
```
`ls -l` Shows a more detailed version of `ls` where permissions, the owner, the size, and the last date which the file/directory was modified are shown alongside the files/directories. This is useful because we can learn more about each file without having to go through each one individually. I found this command option by using `man ls`.   

## **2. ls -t**   
Example 1:  
```
% ls -t ./non-fiction/OUP
Abernathy	Castro		Kauffman
Berk		Fletcher	Rybczynski
```
Example 2:  
```
% ls -t ./non-fiction/OUP/Abernathy
ch1.txt		ch15.txt	ch3.txt		ch7.txt		ch9.txt
ch14.txt	ch2.txt		ch6.txt		ch8.txt
```
`ls -t` works in a similar way to `ls`, but orders the files/directories based on the time it was last modified. This is useful because we can see the order of modification without having to compare the date last modified times. I found this command option by using `man ls`.    

## **3. ls -F**    
Example 1:  
```
% ls -F ./non-fiction/OUP
Abernathy/	Castro/		Kauffman/
Berk/		Fletcher/	Rybczynski/

```
Example 2:  
```
% ls -F ./non-Fiction/OUP/Abernathy
ch1.txt*	ch15.txt*	ch3.txt*	ch7.txt*	ch9.txt*
ch14.txt*	ch2.txt*	ch6.txt*	ch8.txt*
```
`ls -F` adds a `/` or a `*` at the end of each file/directory. The `/` represents a directory and the `*` represents a file. This is useful because we can see which element is a directory and which element is a file within the command line. I found this command option by using `man ls`.    

## **3. ls -R**  
Example 1:   
```
% ls -R ./non-fiction    
OUP

./non-fiction/OUP:
Abernathy	Castro		Kauffman
Berk		Fletcher	Rybczynski

./non-fiction/OUP/Abernathy:
ch1.txt		ch15.txt	ch3.txt		ch7.txt		ch9.txt
ch14.txt	ch2.txt		ch6.txt		ch8.txt

./non-fiction/OUP/Berk:
CH4.txt	ch1.txt	ch2.txt	ch7.txt

./non-fiction/OUP/Castro:
chA.txt	chC.txt	chM.txt	chO.txt	chQ.txt	chV.txt	chY.txt
chB.txt	chL.txt	chN.txt	chP.txt	chR.txt	chW.txt	chZ.txt

./non-fiction/OUP/Fletcher:
ch1.txt		ch2.txt		ch6.txt
ch10.txt	ch5.txt		ch9.txt

./non-fiction/OUP/Kauffman:
ch1.txt		ch3.txt		ch5.txt		ch7.txt		ch9.txt
ch10.txt	ch4.txt		ch6.txt		ch8.txt

./non-fiction/OUP/Rybczynski:
ch1.txt	ch2.txt	ch3.txt
```
Example 2:   
```
% ls -R ./non-fiction/OUP/Abernathy
ch1.txt		ch15.txt	ch3.txt		ch7.txt		ch9.txt
ch14.txt	ch2.txt		ch6.txt		ch8.txt
```

`ls -R` goes through all directories and subdirectories recursively and displays the directories/files. This is useful because we can use this instead of entering each directory to check what is inside. I found this command option by using `man ls`.    

