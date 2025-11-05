###  1.1. Write a program in C to input a string and print it
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  1. Write a program in C to input a string and print it  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100]; 


        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);  
        printf("You entered : %s ",str);
        return 0;
}
```
### Output
```c
Enter a string : Embedded world
You entered : Embedded world
```
