Yash Divecha
*************************************************************************
PURPOSE: xv6 using QEMU
1. Add a new shell command. (proj0.c) 
2. Print a message in Kernel space.
*************************************************************************
proj0.ydivech1.zip contains below 2 files: 
1. proj0.ydivech1.patch - you can patch the base sourceline with this difference patch, compile and run to check the functionality. 

Command: 
remote06:~/DIR_XV6_BASE> patch -p1 < proj0.ydivech1.patch

SAMPLE OUTPUT:
remote06:~/DIR_XV6_BASE1> patch -p1 < ../proj0.ydivech1.patch 
patching file main.c
patching file Makefile
patching file proj0.c
patching file xv6-cs550-Makefile.patch

2. README file
************************************************************************

SAMPLE OUTPUT: 

After patching perform the following steps: 

Command: make qemu-nox
xv6...
cpu1: starting
CS550 proj0 is printing in kernel space: ydivech1 
cpu0: starting
sb: size 1000 nblocks 941 ninodes 200 nlog 30 logstart 2 inodestart 32 bmap start 58
init: starting sh

You have seen, Message in the kernel space has already been printed due to Patch. 

$ls
OUTPUT: 
.              1 1 512
..             1 1 512
README         2 2 1973
cat            2 3 13624
echo           2 4 12585
forktest       2 5 8189
grep           2 6 15532
init           2 7 13490
kill           2 8 12709
ln             2 9 12615
ls             2 10 15467
mkdir          2 11 12738
rm             2 12 12723
sh             2 13 25371
stressfs       2 14 13709
usertests      2 15 67220
wc             2 16 14230
zombie         2 17 12339
proj0          2 18 12678
console        3 19 0

SAMPLE OUTPUT: 
$ proj0 Hello World  
CS550 proj0 print in user space: Hello World
$ proj0 CS550 Operating Systems Section 4
CS550 proj0 print in user space: CS550 Operating Systems Section 4
$ proj0 
CS550 proj0 print in user space: $
**************************************************************************