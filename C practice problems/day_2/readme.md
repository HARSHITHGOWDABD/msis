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
# 2. Write a program to reverse the number. For E.g. If int number = 12345; then the output reverse = 54321;
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
            
            result =result *10 + digit ;  // 10 we need to increase the unit
            
            n=n/10; // to remove the last digit
        }
        
        printf(" the result is % d", result);
       
       
  }
```
## Output 
  ```
enter a five digit number12345
 the result is  54321
```
# 3. Write a program to count the occurrences of a digit in a number.
```
# include<stdio.h>
 int main()
 {  
     int n,r, count=0;
     int digit, temp;
      printf (" enter the number ");
      scanf("%d",&n);
      
      printf(" enter the number which need to count  ");
      scanf("%d",&r);
      
       
      temp =n;
      while(temp!=0)
      {
           digit = temp%10;
           
           if (digit == r){
            count++;}
            temp=temp/10;
      }   
      
      printf(" the counte value is %d", count);
 }
```
### Output 

```
enter the number 222
 enter the number which need to count  2
 the counte value is 3
```
# 4. WAP to check if a given number is a palindrome. For e.g. 12321, 56788765;
```
# include<stdio.h>
 int main()
 {  
      int n,temp,digit,reverse=0;
      printf (" enter the number ");
      scanf("%d",&n);
      
     temp = n;
      
      while(temp!=0)
      {
          digit =temp %10;
          reverse= reverse*10 +digit;
           temp=temp/10;
          
      }
      printf(" the reverse nummber is %d\n", reverse);
      
      if (reverse== n)
      {
          printf(" the number is pallendrome");
          
      }
     else  
      printf(" it is not a pallendrome");
      
 }
```
### Output 

```
enter the number 1234
 the reverse nummber is 4321
 it is not a pallendrome
```



