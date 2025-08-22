# 1. Write a program that converts upper case to lower. 
```
// Program to convert upper case to lower case 
#include <stdio.h>

int lower(char ch1)
{
    if(ch1>'A' && ch1<'Z')
    {
        printf(" the lower case letter is given by");
         
       return printf(" %c", ch1+32);
        
    }
}

int main() {
    
    char ch5;
    
    printf("enter the upper case letter ");
    scanf("%c",&ch5);
    
   lower(  ch5);
    
}

    
    
```

#### output
```
enter the upper case letter H
 the lower case letter is given by h


```
```
#include<stdio.h>
int main()
{
    int i;
    char ch[100];
    char ch2;
    printf( " enter the upper case letters\t");
    scanf(" %s",&ch);
    
    
    for (i=0; i< ch[i]!='\0' ; i++)
    {
    if( ch[i]>='A' && ch[i] <='Z' ){
        
       
        
        ch[i]= ch[i]+32;
        
       }  
     
    }
    
    printf(" the lower case element is %s",ch);
```
# 2. Write a program to calculate the area of Circle. 
```
// Online C compiler to run C program online
#include <stdio.h>
#define pi 3.14

int area(int r)
{
    
    printf(" the area of the circle is ");
 return  printf("%f",pi*r*r);
    
}
int main() {
    
    float r;
    printf("enter the radius of the circle ");
    scanf("%f",&r);
    
    area(r);
    
   
    
    
    
    

    return 0;
}
  ```
### output 
```
enter the radius of the circle 1
 the area of the circle is 3.140000

```

# 3. Given two character inputs, find number of characters between them. For example, if 
input is ‘A’ and ‘E’ the output is 3. 
```


#include<stdio.h>
#include <stdlib.h>

 
 int find(char ch1 , char ch2)
 {
     int result;
      result=  abs(ch1-ch2)-1;
      printf("the result is %d",result);
     
 }
 int main()
 {
     char ch1,ch2;
     int result ;
     printf("enter the firt character ");
     scanf(" %c",&ch1);
     
     printf("enter the second  character ");
     scanf(" %c",&ch2);
     
    find (ch1,ch2);
     
     
 }

 ```
### OUTPUT 
```
enter the firt character A
enter the second  character E
the result is 3

```
# 4.Write a program to convert temperature from Celsius to Fahrenheit 
```
#include<stdio.h>

int faran(float celcius)
{
    float  faranheat;
    faranheat = (celcius *9/5)+32;
      
      printf(" the teperature in faranheat is %f",faranheat);
}

int main()
 {
     float celcius ;
      
      printf(" enter the temperature in celcius ");
      scanf("%f",&celcius);
      
      faran(celcius);
      
     
     
 }
 ```
### OUTPUT 
```
enter the temperature in celcius 8
 the teperature in faranheat is 46.400002
```

# 5.Check if entered number is even or odd. 
```
#include<stdio.h>

int oddeven(int num)
{
     if( num%2==0)
        {
            printf(" the number is even ");
            
        }
        
        else
            printf(" the number is odd");
    
}
 int main()
  {
      int n;
       
      printf("enter the number ");
      scanf("%d",&n);
      
      oddeven(n);
     
  }
```
### Output 
```
enter the number 6
 the number is even
```
# 6. Check if entered year is leap year or not.
```
Note : Leap year is year in which it should divisible by 4 , but if it centurium year it will divisible by 100 also then we need to check with 400 only if it is divisible by 400 then it is leap year.
```
```

#include<stdio.h>
 int main()
  {
      int year ;
       
      printf("enter the year  ");
      scanf("%d",&year);
      
      if(year%400==0)
          printf("%d is a leapyear",year);
      
      else if(year%100==0) 
          printf(" %d is not a leapyear",year);
          
      else if(year%4==0)
          printf("%d is  a leapyear", year );
       
     else 
          printf(" it is not a leapyear");
    
      
      
      
  }
```
### Output
```
enter the year  1900
 1900 is not a leapyear
```
# 7.WAP to find power of 2^N using left shift operator.
```
Note : left shift will multiply 2 by n time , but right shift will divide by divide by 2
```
```
#include<stdio.h>
 int main()
  {
      
      int n,result;
      printf(" enter the value of n\t");
      scanf(" %d",&n);
      
      result=1<<n;
      
      printf("the vale of left shift %d",result);
      
    
    }
```
###  Output 
```
enter the value of n	4
the vale of left shift 16
```

# 8.Check if given input is a character or integer. (Use integer input within the range 0-9)
```
#include<stdio.h>
 int main()
 
 {  
     
     char input;
     printf("enter the inputs as a character or a integer ");
     scanf("%c",&input );
     
     if(input>='0' && input<='9')
         
         printf("the input is a integer ");
         
   
     
     else if( input>='A'   && input<='z')
         printf("the input is a character ");
         
         else 
          printf("it is either character or integer ");
 }
```
### Output
```
enter the inputs as a character or a integer f
f the input is a character
```
# 9.Generate two random numbers and find its sum (Hint: use rand() from stdlib.h) 
```
#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main(){
    int num1,num2,sum;
    srand(time(0));
    num1=rand()%100;
    num2=rand()%100;
    sum=num1+num2;
    printf("the frist number:%d\n",num1);
    printf("the second number:%d\n",num2);
    printf("the sum of two number is:%d\n",sum);
    return 0;   
}
```


