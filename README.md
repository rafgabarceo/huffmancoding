# Huffman Coding implementation on C
This repository is for educational purposes only. Using only the standard C library available on both Linux and Windows, this repository aims to reproduce the Huffman Coding algorithm with an output of bits to simulate Source Coding in a communications system. 

## Using the program
Because the program itself will depend on other programs, it is important to ensure that there is an input of hex codes of a message.

## How it works
The Huffman Algorithm as stated by Cormen, Leiserson, Rivest, and Stein (2009) has the following pseudocode:

``` 
HUFFMAN(C)
1. n = |C|
2. Q = C
3. for i <- 1 to n - 1, do
4.      allocate a new node z
5.      z.left <- x <- EXTRACT-MIN(Q)
6.      z.right <- y <- EXTRACT-MIN(Q)
7.      z.freq <- x.freq + y.freq
8.      INSERT(Q, z)
9. end for
10. return EXTRACT-MIN(Q) // return root of the tree 
```