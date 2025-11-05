###  1.Write a program in C to input a string and print it
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
### 2. Write a program in C to find the length of a string without using library functions.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  2. Write a program in C to find the length of a string without using library functions. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];

        int i=0,length=0;

        printf("enter a string :");
        fgets(str,sizeof(str),stdin);

         // Count characters until '\0'

        while(str[i]!='\0'){
                if (str[i] == '\n')    // ignore newline from fgets
                        break;
                length++;
                i++;

        }


        printf("Length of the string = %d\n",length);
        return 0;
}
```
### Output
```c
enter a string :bharathi
Length of the string = 8
```
### 3. Write a program in C to separate individual characters from a string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 3. Write a program in C to separate individual characters from a string. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){


        char str[100];

        int i=0;
        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        printf("Individual characters are : \n");

        while(str[i]!='\0'){
                if(str[i]=='\n')
                        break;
                printf("%c\n",str[i]);
                i++;
        }
        return 0;
}
```
### Output
```c
Enter a string : Hello world
Individual characters are :
H
e
l
l
o

w
o
r
l
d
```
###  4. Write a program in C to print individual characters of a string in reverse order.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 4. Write a program in C to print individual characters of a string in reverse order.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int length=0;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);


        while(str[length]!='\0' && str[lengt]!='\n'){
                length++;
        }
        printf("Individual chars in reverse order are \n");
         // Print characters from last to first
        for(int i=length-1;i>=0;i--){
                printf("%c\n",str[i]);
        }

        return 0;
}
```
### Output
```c
Enter a string : Raghu vardhan
Individual chars in reverse order are : nahdrav uhgaR 
```
###  5. Write a program in C to count the total number of words in a string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 5. Write a program in C to count the total number of words in a string.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char str[200];
        int i,count=0;

        printf("Enter a string : ");
        fgets(str, sizeof(str), stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i]==' ' || str[i]=='\n' || str[i]=='\t'){
                        count++;
                }
        }

        printf("Total number of words : %d\n",count);
        return 0;
}
```
### Output
```c
Enter a string : Viven Embedded
Total number of words : 2
```
###  6. Write a program in C to compare two strings without using string library functions.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 6. Write a program in C to compare two strings without using string library functions.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str1[100],str2[100];
        int i,flag=0;

        printf("Enter str1 : ");
        fgets(str1,sizeof(str1),stdin);

        printf("Enter str2 : ");
        fgets(str2,sizeof(str2),stdin);

         // Compare both strings character by character

        for(i=0;str1[i]!='\0' || str2[i]!='\0';i++){
                if(str1[i]!=str2[i]){
                        flag=1;
                        break;
                }
        }

        if(flag==0)
                printf("Both strings are equal.\n");
        else
                printf("Both are not equal.\n");
        return 0;
}
```
### Output
```c
Enter str1 : hello
Enter str2 : heloo
Both are not equal.
```
###  7.Write a c program to count total number of alphabets , digits and special characters in a string .
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 7.Write a c program to count total number of alphabets , digits and special characters in a string .  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    char str[100];
    int i, alphabets = 0, digits = 0, special = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++) {
        if ((str[i] >= 'a' && str[i] <= 'z') || (str[i] >= 'A' && str[i] <= 'Z'))
            alphabets++;
        else if (str[i] >= '0' && str[i] <= '9')
            digits++;
        else if (str[i] != '\n' && str[i] != ' ')
            special++;
    }

    printf("Alphabets: %d\n", alphabets);
    printf("Digits: %d\n", digits);
    printf("Special characters: %d\n", special);

    return 0;
}
```
### Output
```c
Enter a string: bharathi@136
Alphabets: 8
Digits: 3
Special characters: 1
```
###  8. Write a program in C to copy one string to another string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 8. Write a program in C to copy one string to another string.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str1[100],str2[100];

        int i;

        printf("Enter a string : ");
        fgets(str1,sizeof(str1),stdin);

        for(i=0;str1[i]!='\0';i++){
                str2[i]=str1[i];

        }
        str2[i]='\0';
        printf("Copied string is : %s\n",str2);

        return 0;
}

```
### Output
```c
Enter a string : viven
Copied string is : viven
```
### 9. Write a program in C to count the total number of vowels or consonants in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 9. Write a program in C to count the total number of vowels or consonants in a string  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[200];

        int i,vowels=0,consonants=0;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i] >= 'a' && str[i] <= 'z' || str[i] >='A' &&str[i] <= 'Z'){
                         if (str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u'||
                str[i]=='A'||str[i]=='E'||str[i]=='I'||str[i]=='O'||str[i]=='U')
                                 vowels++;
                         else
                                 consonants++;
                }
        }

        printf("Vowels =%d\n",vowels);
        printf("Consonants = %d\n",consonants);

        return 0;
}
```
### Output
```c
Enter a string : hemalakshmi
Vowels =4
Consonants = 7
```
### 10.find  maximum  number of characters in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 10.find  maximum  number of characters in a string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[200];
        int i=0,count=0;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i]!='\n'){
                        count++;
                }
        }
        printf("total number of characters are : %d\n ",count);
        return 0;
}
```
### Output
```c
Enter a string : hello world
total number of characters are : 11
```
###  11. Write a C program to sort a string array in ascending order.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 11. Write a C program to sort a string array in ascending order. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[200];

        int i,j,temp;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                for(j=i+1;str[j]!='\0';j++){
                        if(str[i]>str[j]){
                                temp=str[i];
                                str[i]=str[j];
                                str[j]=temp;
                        }
                }
        }

        printf("Ascending order of a string = %s",str);

        return 0;
}

```
### Output
```c
Enter a string : 321viven
Ascending order of a string = 123einvv
```
### 12. Write a program in C to read a string from the keyboard and sort it using bubble sort
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  12. Write a program in C to read a string from the keyboard and sort it using bubble sort  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    char str[100];
    int i, j;
    char temp;

    printf("Enter a string: ");
    gets(str);  // Read string (you can use fgets for safer input)

    // Bubble sort logic
    for (i = 0; str[i] != '\0'; i++) {
        for (j = i + 1; str[j] != '\0'; j++) {
            if (str[i] > str[j]) {  // Compare characters
                temp = str[i];
                str[i] = str[j];
                str[j] = temp;
            }
        }
    }
    printf("String after sorting: %s\n", str);

    return 0;
}

```
### Output
```c
Enter a string: 698embedded
String after sorting: 689bdddeeem
```
###  3. Write a program in C to extract a substring from a given string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 3. Write a program in C to extract a substring from a given string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100],sub[100];
        int start,length,i;

        printf("enter a string : ");
        fgets(str,sizeof(str),stdin);

        printf("enter starting position : ");
        scanf("%d",&start);

        printf("enter length of sub string : ");
        scanf("%d",&length);

        for(i=0;i<length;i++){
                sub[i]=str[start + i - 1];

        }
        sub[i]='\0';

        printf("Extracted substring : %s ",sub);

        return 0;
}
```
### Output
```c
enter a string : amsterdam
enter starting position : 7
enter length of sub string : 3
Extracted substring : dam
```
###  15. Write a program in C to read a sentence and replace lowercase characters with uppercase and viceversa
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 15. Write a program in C to read a sentence and replace lowercase characters with uppercase and viceversa *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
#include<string.h>
int main(){
        char str[100];
        int i;

        printf("enter a sentence : ");
        fgets(str,sizeof(str),stdin);

        str[strcspn(str,"\n")]='\0';

        for(i=0;str[i]!='\0';i++){
                if(str[i]>='a' && str[i]<='z'){
                        str[i]=str[i]-32;
                }
                else if(str[i] >= 'A' && str[i] <= 'Z'){
                        str[i]=str[i]+32;
                }
        }

        printf("Converted sentence : %s ",str);

        return 0;
}
```
### Output
```c
enter a sentence : viven embedded
Converted sentence : VIVEN EMBEDDED
```
###  16. Write a program in C to find the number of times a given word 'the' appears in the given string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 16. Write a program in C to find the number of times a given word 'the' appears in the given string.*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
#include<string.h>
int main(){
        char str[200];
        int i,j,count=0;
        char word[10];

        printf("Enter a sentence : ");
        fgets(str,sizeof(str),stdin);

        i=0;
        while(str[i]!='\0'){
                j=0;
                while (str[i] != ' ' && str[i] != '\n' && str[i] != '\0'){
                        word[j]=str[i];
                        i++;
                        j++;
                }
                word[j]='\0';

                if(strcmp(word,"the")==0 || strcmp(word,"The")==0){
                        count++;
                }

                i++;
        }

        printf("The word 'the' appears %d times\n",count);
        return 0;
}

```
### Output
```c
Enter a sentence : the greatest of the all times
The word 'the' appears 2 times
```
###  17. Write a program in C to remove characters from a string except alphabets.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 17. Write a program in C to remove characters from a string except alphabets. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    char str[200], result[200];
    int i, j = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Read string with spaces

    // Loop through each character
    for (i = 0; str[i] != '\0'; i++) {
        // Keep only alphabets (A-Z or a-z)
        if ((str[i] >= 'A' && str[i] <= 'Z') || (str[i] >= 'a' && str[i] <= 'z')) {
            result[j] = str[i];
            j++;
        }
    }

    result[j] = '\0';  // End the new string

    printf("String after removing non-alphabet characters: %s\n", result);
    return 0;
}
```
### Output
```c
Enter a string: bharathi@22
String after removing non-alphabet characters: bharathi
```
### 18. Write a program in C to find the frequency of characters.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 18. Write a program in C to find the frequency of characters. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
