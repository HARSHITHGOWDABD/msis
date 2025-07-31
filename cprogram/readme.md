# COMMANDS IN LINUX TO EXEGUTE THE CODE 

- pwd ----> refers to print the working directory 
- mkdir ---> To create the new directory (make directory )
- cd -------> chanage directory or to get into the file
- gedit -----> to open the greaphical test editor 
- gcc -------> after writing  the code to compile we can use this grahicial compiler 
- ./a.out ---> it will runs the exegutable file .

# EXAMPLE 
 - mkdir 251100630027_harshith  ------>      creates the new directory with the file name  251100630027_harshith
 - cd 251100630027_harshith     ------->     now we will get into this currecnt directory
 - pwd                         --------->    now we are in the currecnt working directory that we created
 - gedit program1.c           ----------->   it will open the editor file with the file name as program1.c
 - gcc program1.c            ------------>   graphical compiler will just compile the file and shows if their is any error in it
 - ./a.out                  -------------->   will runs the exegutable file 

# File handlling in  c 
- Console  is a screen where the output will be displayed
- Basically whenever we write a  code by taking a inputs it will store in RAM since it is a volatile memeory after the exegution the data will be erased but by storing this data in the harddisk we can retrive it , the process of storing the data in the harddisk is called file handling 
- File ? it is a sequence of bytes (memory ), where we can store the data permanantionly.
- Why we need ---> 1) After the termination also if we want to use the previous data then we can use this
              ---> 2) In some cases we need to provide the large amout of data , in this case we can just include that file and perfom the required operation
             ----> 3) Since the size of  the RAM is also very small , in many sictuatin its necessary

- Files are of two types  1) text[.txt] 2) binary[.bin]
- text file are less secured than the binary file 
- operations   -->create , read, write ,close .

-  file pointer ---> pointer is a variable used to store the address of another variable ,
-    eg : int ^ptr ; --> it will store the address of the variable whose datatype is int
-   fopen ---> to open the function (in stdio.h)
-   fopen(" filename ","mode")
-   mode r-----> just to read something
- .       w------> just to write something
- .       a------> append somethig
- 
   
