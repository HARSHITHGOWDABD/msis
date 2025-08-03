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
# 5.Generate the first 'N' prime numbers. For Eg. If N=5 then 2,3,5,7,11
```
#include <stdio.h>

int main() {
    int n, count = 0, num = 2, i, isPrime;

    printf("Enter the value of N: ");
    scanf("%d", &n);

       printf("First %d prime numbers are:",n); 
    while (count < n) {
        isPrime = 1; // Assume num is prime

        // Check if num is prime
        for (i = 2; i <= num / 2; i++) {
            if (num % i == 0) {
                isPrime = 0;
                break;
            }
        }

        if (isPrime) {
            printf("%d ", num);
            count++;
        }

        num++; // Move to the next number
    }



   
}
```
### Output 

```
Enter the value of N: 5
First 5 prime numbers are:2 3 5 7 11
```
# 6.Write a C program to display and find the sum of the series 1+11+111+....111 up to n. 
For eg. if n=4, the series is: 1+11+111+1111. Take the value of 'n' as input from the 
user
```
#include <stdio.h>

int main() {
    int n, i;
    long term = 0, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    printf("The series is: ");

    for (i = 1; i <= n; i++) {
        term = term * 10 + 1;     // Generate term like 1, 11, 111, ...
        printf("%ld", term);

        if (i < n)
            printf(" + ");        // Print '+' between terms

        sum += term;              // Add term to sum
    }

    printf("\nSum of the series: %ld\n", sum);

    return 0;
}#include <stdio.h>

int main() {
    int n, i;
    long term = 0, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    printf("The series is: ");

    for (i = 1; i <= n; i++) {
        term = term * 10 + 1;     // Generate term like 1, 11, 111, ...
        printf("%ld", term);

        if (i < n)
            printf(" + ");        // Print '+' between terms

        sum += term;              // Add term to sum
    }

    printf("\nSum of the series: %ld\n", sum);

    return 0;
}
```
### Output 

```
Enter the value of n: 3
The series is: 1 + 11 + 111
Sum of the series: 123

```
# 7.A number is called an Armstrong number if the sum of the cubes of the digits of the 
number is equal to the number. For example 153 = 1^3 + 5^3 + 3^3. Write a C 
program that asks the user to enter a number and returns if it is Armstrong or not.

```
#include <stdio.h>

int main() {
    int num, temp, digit, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    temp = num; // Store original number

    // Calculate sum of cubes of digits
    while (temp != 0) {
        digit = temp % 10;        // Extract last digit
        sum = sum+ digit * digit * digit; // Cube and add
        temp = temp / 10;         // Remove last digit
    }

    // Check if Armstrong
    if (sum == num)
        printf("%d is an Armstrong number.\n", num);
    else
        printf("%d is not an Armstrong number.\n", num);

    return 0;
}
```
### Output 
```
Enter a number: 153
153 is an Armstrong number.
```
# 8.Amicable numbers are found in pairs. A given pair of numbers is Amicable if the sum 
of the proper divisors (not including itself) of one number is equal to the other number 
and vice – versa.  
For example 220 & 284 are amicable numbers. First we find the proper divisors of 
220:  
220:1, 2, 4, 5, 10, 11, 20, 22, 44, 55, 110; 1+ 2 + 4 + 5 + 10 + 11 + 20 + 22 + 44 + 55 
+ 110 = 284 
Now, 284: 1, 2, 4, 71, 142; 1 + 2 + 4 + 71 + 142 = 220  
Write a C program to check that the input pair of numbers is amicable
```
#include <stdio.h>

int main() {
    int num1, num2, sum1 = 0, sum2 = 0;

    // Input two numbers
    printf("Enter the first number: ");
    scanf("%d", &num1);
    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Find sum of proper divisors of num1
    for (int i = 1; i <= num1 / 2; i++) {
        if (num1 % i == 0) {
            sum1 =sum1+i;
           
        }
    }

    // Find sum of proper divisors of num2
    for (int i = 1; i <= num2 / 2; i++) {
        if (num2 % i == 0) {
            sum2= sum2+i;
        }
    }

    // Check if they are amicable
    if (sum1 == num2 && sum2 == num1) {
        printf("%d and %d are amicable numbers.\n", num1, num2);
    } else {
        printf("%d and %d are not amicable numbers.\n", num1, num2);
    }

    return 0;
}
```
### Output
```
Enter the first number: 220
Enter the second number: 284
220 and 284 are amicable numbers.
```
# 9.Write a menu driven program to read two integers & find their sum, difference & 
product. 
```
#include<stdio.h>
 int main()
 {   
     int num1,num2, choice,result;
     printf(" enter the two number ");
     scanf("%d %d",&num1,&num2);

 
 do{
     printf("\n MENUE\n");
     printf("1. add\n");
     printf(" 2.sub\n");
     printf(" 3.mul\n");
     printf(" 4.exit\n");
     printf("enter the coice ");
     scanf("%d",&choice);
     
     switch(choice)
     {
         case 1:
         result= num1+num2;
         printf(" result is %d\n", result);
         break;
         
         case 2:
         result = num1-num2;
         printf(" result is %d", result);
         break;
         
         case 3:
         result = num1*num2;
         printf(" result is %d", result);
         break;
         
         case 4:
                printf("Exiting the program.\n");
                break;

            default:
                printf("Invalid choice! Please try again.\n");
                
         
        
        }
     
 }
 while(choice!=4);
 
  return 0;
 }
```
### Output 
```
Enter two integers: 1
4

Menu:
1. Find Sum
2. Find Difference
3. Find Product
4. Exit
Enter your choice: 2
Difference = -3

Menu:
1. Find Sum
2. Find Difference
3. Find Product
4. Exit
Enter your choice: 
```
# 10.Write a C program to calculate the volume of the following shapes: Cube, Cuboid, 
Sphere, Cylinder and Cone. Ask the user which one s/he wants to calculate, and take 
the appropriate required inputs. Then print the result. The input should be taken in the 
main function and calculations for every solid should be done in a separate function 
by passing appropriate arguments. 
Example: If the user chooses the option for cube, only one input is required i.e., the 
side. The volume is then calculated and printed.  
If the user chooses the option for cuboid, only three inputs are required i.e., length, 
breadth and height. The volume is then calculated and printed. 
```




