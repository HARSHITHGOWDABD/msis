# 1. Write a program that converts upper case to lower. 
```
#include<stdio.h>
int main()
{
    char ch,ch2;
    printf( " enter the upper case letters\t");
    scanf(" %c",&ch);
    
    if( ch>='A' && ch <='Z' ){
        
        printf(" the entered letter is in uppercase\n");
        
        ch2= ch+32;
        
        printf(" the lower case element is %c",ch2);
        
        
    }
    
    else{
    
    printf(" it is not a upper case letter ");
    
    }
    
}
```

#### output
```
enter the upper case letters	H
 the entered letter is in uppercasse
 the lower case element is h
```


