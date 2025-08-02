# 1. Enter a 5 digit number and find the sum of its digits. For E.g. if int number = 12345 ,then sum = 15;
```
#include<stdio.h>
  int main()
  {      
      int n,i,result=0,digit;
       printf("enter a five digit number");
       scanf("%d",&n);
       
       for( i=0; i<5 ;i++)
       
        { 
            digit = n%10 ; // to get the last value 
            
            result =result + digit ;
            
            n=n/10; // to remove the last digit
        }
        
        printf(" the result is % d", result);
       
       
  }
```
## output 
```
enter a five digit number12345
 the result is  15
```
