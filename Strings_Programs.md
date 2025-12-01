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
#include <stdio.h>
int main() {
    char str[100];
    int i, j, count;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Read input string

    printf("\nCharacter frequencies:\n");

    for (i = 0; str[i] != '\0'; i++) {
        count = 1;

        // Skip if the character is already counted
        if (str[i] == ' ' || str[i] == '\n' || str[i] == '\0')
            continue;

        // Check if this character appeared before
        for (j = 0; j < i; j++) {
            if (str[i] == str[j])
                break;
        }

        // If not found before, count how many times it appears
        if (i == j) {
            for (j = i + 1; str[j] != '\0'; j++) {
                if (str[i] == str[j])
                    count++;
            }
            printf("%c = %d\n", str[i], count);
        }
    }

    return 0;
}
```
### Output
```c
Enter a string: VivenEmbedded
Character frequencies:
V = 1
i = 1
v = 1
e = 3
n = 1
E = 1
m = 1
b = 1
d = 3
```
### 19.Write a program in C to combine two strings manually
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 19.Write a program in C to combine two strings manually *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    char str1[100], str2[100];
    int i, j;

    printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);

    printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);

    // Remove newline characters (if any) from fgets
    for (i = 0; str1[i] != '\0'; i++) {
        if (str1[i] == '\n') {
            str1[i] = '\0';
            break;
        }
    }

    // Find the end of the first string
    for (i = 0; str1[i] != '\0'; i++);

    // Copy characters of second string to first
    for (j = 0; str2[j] != '\0'; j++) {
        str1[i + j] = str2[j];
    }

    str1[i + j] = '\0'; // End the combined string

    printf("\nCombined string: %s\n", str1);
    return 0;
}
```
### Output
```c
Enter first string: Viven-
Enter second string: Embedded
Combined string: Viven-Embedded
```
### 20. Write a program in C to find the largest and smallest words in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *20. Write a program in C to find the largest and smallest words in a string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[200];
        char word[50],smallest[50],largest[50];
        int i=0,j=0,k,length,min=0,max=0;


        printf("Enter a string with two words : ");
        fgets(str,sizeof(str),stdin);

        while(1){
                if(str[i]!= ' ' && str[i]!= '\0')
                        word[j++]=str[i];
                else{
                        word[j]='\0';
                        length=j;

                        if(min==0 || length<min){
                                min=length;
                                for(int k=0;k<=length;k++)
                                        smallest[k]=word[k];
                        }
                       if(length>max){
                                max=length;
                                for(int k=0;k<=length;k++)
                                        largest[k]=word[k];
                        }
                       j=0;
                       if(str[i]=='\0')
                               break;
                   }
                   i++;
        }

         printf("\nSmallest word: %s", smallest);
         printf("\nLargest word: %s\n", largest);
         return 0;
}
```
### Output
```c
Enter a string with two words : Practice world
Smallest word: world
Largest word: Practice
```
###  21.Write a program in C to convert a string to uppercase.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 21.Write a program in C to convert a string to uppercase.*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i] >= 'a' && str[i] <= 'z')  // check lowercase letters
                        str[i]= str[i]-32; // convert to uppercase (ASCII logic)
        }

        printf("String in uppercase : %s",str);
        return 0;
}
```
### Output
```c
Enter a string : jaisriram
String in uppercase : JAISRIRAM
```
### 22. Write a program in C to convert a string to lowercase.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 22. Write a program in C to convert a string to lowercase. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i;

        printf("enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i] >= 'A' && str[i] <= 'Z'){
                        str[i]=str[i]+32;
                }
        }

        printf("String in lowercase : %s ",str);
        return 0;
}
```
### Output
```c
enter a string : JAISRIKRISHNA
String in lowercase : jaisrikrishna
```
###  23. Write a program in C to check whether a character is a Hexadecimal Digit or not
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 23. Write a program in C to check whether a character is a Hexadecimal Digit or not *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char ch;

        printf("Enter a character : ");
        scanf("%c",&ch);

        if((ch >='0' && ch <='9') ||
                        (ch >= 'A' && ch<='F') ||
                        (ch >= 'a' && ch<='f')){
                printf("%c is a Hexadecimal digit\n",ch);
        }else{
                printf("%c is not a Hexadecimal digit\n",ch);
        }

        return 0;
}

```
### Output
```c
Enter a character : 9
9 is a Hexadecimal digit
```
### 24. Write a program in C to check whether a letter is uppercase or not.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 24. Write a program in C to check whether a letter is uppercase or not. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
         char ch;

         printf("Enter a character : ");
         scanf("%c",&ch);

         if(ch >= 'A' && ch <= 'Z')
                 printf("%c is an uppercase letter\n",ch);
         else
                 printf("%c is not an uppercase letter\n",ch);

        return 0;
}
```
### Output
```c
Enter a character : U
U is an uppercase letter
```
###  25. Write a program in C to replace the spaces in a string with a specific character.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 25. Write a program in C to replace the spaces in a string with a specific character. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char str[100],ch;

        int i;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        printf("enter the character to replace space : ");
        scanf("%c",&ch);

        for(i=0;str[i]!='\0';i++){
                if(str[i]== ' ')
                        str[i]=ch;
        }
        printf("String after replacing spaces : %s ",str);

        return 0;
}

```
### Output
```c
Enter a string : Quest Global
enter the character to replace space : -
String after replacing spaces : Quest-Global
```
###  26. Write a program in C to print only the string before the new line character.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 26. Write a program in C to print only the string before the new line character. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char str[100];
        int i;

        printf("enter a string : ");
        fgets(str,sizeof(str),stdin);

        printf("string before newline : ");

        for(i=0;str[i]!='\0';i++){
                if(str[i] == '\n')
                        break;
                printf("%c",str[i]); //printf character
        }

        return 0;
}
```
### Output
```c
enter a string : str
string before newline : str
```
### 27. Write a program in C to count the number of punctuation characters present in a string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 27. Write a program in C to count the number of punctuation characters present in a string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    char str[200];
    int i, count = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // read string with spaces

    for (i = 0; str[i] != '\0'; i++) {
        // Check if character is punctuation
        if (str[i] == '.' || str[i] == ',' || str[i] == ';' || str[i] == ':' ||
            str[i] == '!' || str[i] == '?' || str[i] == '\'' || str[i] == '\"' ||
            str[i] == '-' || str[i] == '(' || str[i] == ')' || str[i] == '[' ||
            str[i] == ']' || str[i] == '{' || str[i] == '}')
            count++;
    }

    printf("Total number of punctuation characters: %d\n", count);
    return 0;
}
```
### Output
```c
Enter a string: hi...this-is,bharu
Total number of punctuation characters: 5
```
### 28. Write a program in C to check whether a string lower case or not
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *28. Write a program in C to check whether a string lower case or not *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char ch;

        printf("Enter a character  : ");
        scanf("%c",&ch);

        if(ch >= 'a' && ch <='z')
                printf("%c is lowercase letter\n ",ch );
        else
                printf("%c is not lowercase\n ",ch);
        return 0;
}

```
### Output
```c
Enter a character  : i
i is lowercase letter
```
### 30. Write a program in C to check whether a character is a digit or not.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *30. Write a program in C to check whether a character is a digit or not. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char ch;

        printf("Enter a character : ");
        scanf("%c",&ch);

        if( ch >= '0' && ch <= '9')
                printf("%c is a digit \n",ch);
        else
                printf("%c is not a digit\n",ch);
        return 0;
}
```
### Output
```c
Enter a character : 8
8 is a digit
```
###  31. Write a program in C to split strings by space into words.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 31. Write a program in C to split strings by space into words. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i;

        printf("Enter a sentence : ");
        fgets(str,sizeof(str),stdin);

        printf("Words are : \n");
        for(i=0;str[i]!='\0';i++){
                if(str[i] == ' ')
                        printf("\n");
                else if (str[i] != '\n')
                        printf("%c",str[i]);
        }

        return 0 ;
}
```
### Output
```c
Enter a sentence : i am kind
Words are :
i
am
kind
```
###  32. Write a C program to find the repeated character in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 32. Write a C program to find the repeated character in a string. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i,j;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        printf("Repeated characters :");
        for(i=0;str[i]!='\0';i++){
                if(str[i] == ' ' || str[i] == '\n' )
                        continue;
                for(j=i+1;str[j]!='\0';j++){
                        if(str[i] == str[j]){
                                printf("%c",str[i]);

                                str[j] = ' '; //mark as counted

                                break;
                        }
                }
        }

        return 0;
}
```
### Output
```c
Enter a string : helloworld
Repeated characters :lo
```
### 33. Write a C program to count each character in a given string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 33. Write a C program to count each character in a given string.*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i,j,count;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        printf("characters count = \n");

        for(i=0;str[i]!='\0';i++){
                count =1;
                if(str[i] == ' ' || str[i] == '\n')
                        continue;
                for(j=i+1;str[j]!='\0';j++){
                        if(str[i] == str[j]){
                                count++;

                                str[j] = ' '; //mark counted
                        }
                }

                if (str[i]!= ' ' )
                        printf("%c = %d\n",str[i],count);
        }

        return 0 ;
}
```
### Output
```c
Enter a string : madam
characters count =
m = 2
a = 2
d = 1
```
### 34. Write a C program to convert vowels into uppercase characters in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 34. Write a C program to convert vowels into uppercase characters in a string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char str[100];
        int i;

        printf("enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i] == 'a' || str[i] == 'e' || str[i] == 'i' || str[i] == 'o' || str[i] == 'u'){
                        str[i]=str[i]-32;
                }

        }

        printf("after conversion of vowels into uppercase : %s\n",str);
        return 0 ;
}

```
### Output
```c
enter a string : MissWorld
after conversion of vowels into uppercase : MIssWOrld
```
###  35.Write a C program to reverse all the vowels present in a given string. Return the newly created string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 35.Write a C program to reverse all the vowels present in a given string. Return the newly created string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
#include<string.h>

int isVowel(char ch){                 // Function to check if a character is a vowel
        if(ch >= 'A' && ch <= 'Z')
                ch =ch +32;
        return(ch == 'a' || ch == 'e' || ch == 'i' || ch == '0' || ch == 'u');
}
int main(){
        char str[100],vowels[50];
        int i,j=0;

        printf("enter a string : ");
        fgets(str,sizeof(str),stdin);

        // Step 1: Store all vowels from string
        for(i=0;str[i] != '\0';i++){
                if(isVowel(str[i])){
                        vowels[j] = str[i];
                        j++;
                }
        }
        vowels[j] = '\0';

        // Step 2: Replace vowels in reverse order
        j--; //move to last vowel

        for(i=0;str[i]!='\0';i++){
                if(isVowel(str[i])){
                        str[i]=vowels[j];
                        j--;
                }
        }

        printf("string after reversing vowels : %s",str);
        return 0;
}
```
### Output
```c
enter a string : hello
string after reversing vowels : holle
```
###  36.Write a C program to find the longest palindromic substring from a given string. Return the substring.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 36.Write a C program to find the longest palindromic substring from a given string. Return the substring. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
#include<string.h>
int isPalindrome(char str[],int start,int end){
        while(start < end){
                if(str[start] != str[end])
                        return 0;
                start++;
                end--;
        }
        return 1;
}

int main(){
        char str[100];
        int i,j,len,maxLen = 1,startIndex = 0;

        printf("Enter a string : ");
        scanf("%s",str);

        len=strlen(str);

        for(i=0;i<len;i++){
                for(j=i;j<len;j++){

                        // Check if substring from i to j is palindrome
                        if (isPalindrome(str, i, j)) {
                               int currLen = j - i + 1;
                                if (currLen > maxLen) {  // Update if it's the longest so far
                                        maxLen = currLen;
                                        startIndex = i;
                                 }
                        }
                }
        }
        printf("Longest Palindromic Substring: ");
        for (i = startIndex; i < startIndex + maxLen; i++) {
                printf("%c", str[i]);
        }
        return 0;
}
         
```
### Output
```c
Enter a string : sheismadam
Longest Palindromic Substring: madam
```
### 37. Write a C program to replace each lowercase letter with the same uppercase letter of a given string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 37. Write a C program to replace each lowercase letter with the same uppercase letter of a given string. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i] >= 'a' && str[i] <= 'z'){
                        str[i] = str[i] -32;
                }
        }

        printf("After replacing lower to upper of a given string : %s",str);

        return 0;
}
```
### Output
```c
Enter a string : Hello World
After replacing lower to upper of a given string : HELLO WORLD
```
###  38.. Write a C program to copy one string to another string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 38. Write a C program to copy one string to another string. *
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

        printf("Copied string is %s\n",str2);

        return 0;
}
```
### Output
```c
Enter a string : peace
Copied string is peace
```
### 39. Write a C program to concatenate two strings.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 39. Write a C program to concatenate two strings. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str1[100],str2[100];

        int i=0,j=0;

        printf("Enter string 1 : ");
        gets(str1);

        printf("Enter string 2 : ");
        gets(str2);

        while(str1[i]!='\0'){
                i++;
        }
        while(str2[j]!='\0'){
                str1[i]=str2[j];
                i++;
                j++;
        }

        str1[i] ='\0';  //end of the string :

        printf("After concatenation : %s",str1);
        return 0;
}
```
### Output
```c
Enter string 1 : my
Enter string 2 : programs
After concatenation : myprograms
```
###  40. Write a C program to compare two strings.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  Write a C program to compare two strings.*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str1[100],str2[100];
        int i=0;

        printf("Enter str 1 : ");
        fgets(str1,sizeof(str1),stdin);

        printf("Enter str 2 : ");
        fgets(str2,sizeof(str2),stdin);

        while(str1[i]!='\0' && str2[i]!='\0'){
                if(str1[i] != str2[i]){
                        printf("Both strings are not equal ");
                        return 0;
                }
                i++;
        }

        printf("Both strings are equal");

        return 0;
}
```
### Output
```c
Enter str 1 : hellomiss
Enter str 2 : hiimiss
Both strings are not equal
```
###  41. Write a C program to find the total number of alphabets, digits or special characters in a string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 41. Write a C program to find the total number of alphabets, digits or special characters in a string.*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char str[100];
        int i;
        int alphabets=0,digits=0,symbols=0;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i] >= 'A' && str[i] <= 'Z' || str[i] >= 'a' && str[i] <= 'z')
                        alphabets++;
                else if (str[i] >= '0' && str[i] <='9')
                        digits++;
                else if (str[i] != '\n' && str[i] != ' ')
                        symbols++;
        }

        printf("Total numbers of Alphabets = %d\n Digits =%d\n Symbols=%d\n",alphabets,digits,symbols);

        return 0;
}
```
### Output
```c
Enter a string : hello@123
Total numbers of Alphabets = 5
 Digits =3
 Symbols=1
```
### 42.Write a C program to count the total number of vowels and consonants in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 42.Write a C program to count the total number of vowels and consonants in a string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    char str[100];
    int i, vowels = 0, consonants = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++) {
        // check for vowels (both lowercase and uppercase)
        if (str[i]=='a' || str[i]=='e' || str[i]=='i' || str[i]=='o' || str[i]=='u' ||
            str[i]=='A' || str[i]=='E' || str[i]=='I' || str[i]=='O' || str[i]=='U') {
            vowels++;
        }
        // check for consonants (only alphabets that are not vowels)
        else if ((str[i] >= 'a' && str[i] <= 'z') || (str[i] >= 'A' && str[i] <= 'Z')) {
            consonants++;
        }
    }

    printf("Number of vowels = %d\n", vowels);
    printf("Number of consonants = %d\n", consonants);

    return 0;
}
```
### Output
```c
Enter a string: coconut
Number of vowels = 3
Number of consonants = 4
```
### 43. Count total number of words in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  Count total number of words in a string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i,count=1;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i] == ' ' && str[i+1]!='\0' && str[i+1]!=' ' && str[i+1]!='\n'){
                        count++;
                }
        }


        printf("Total words = %d\n",count);
        return 0;
}
```
### Output
```c
Enter a string : pretty good
Total words = 2
```
### 44. Write a C program to check whether a string is palindrome or not
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  Write a C program to check whether a string is palindrome or not. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i=0,j=0;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        while(str[j]!='\0'){
                j++;
        }
        if(str[j-1]=='\n'){
                str[j-1]='\0';
                j--;
        }

        j--;

        while(i<j){
                if(str[i]!=str[j]){
                        printf("not a palindrome ");
                        return 0;
                }
                i++;
                j--;
        }

        printf("palindrome\n");
        return 0;
}
```
### Output
```c
Enter a string : Level
not a palindrome
```
### 45. Write a C program to find the reverse of a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 45. Write a C program to find the reverse of a string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){

        char str[100];
        int i,len=0;

        printf("enter a string : ");
        fgets(str,sizeof(str),stdin);

        for(i=0;str[i]!='\0';i++){
                if(str[i]=='\n')
                        break;
                        len++;

        }

        //reverse string
        printf("reversed string : ");
        for(i=len-1;i>=0;i--){
                printf("%c",str[i]);
        }
        return 0;
}

```
### Output
```c
enter a string : strong
reversed string : gnorts
```
### 46 write a c program to reverse words in a string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * write a c program to reverse words in a string. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        char str[100];
        int i,end,start;

        printf("Enter a string : ");
        fgets(str,sizeof(str),stdin);

        //find lenth
        for(i=0;str[i]!='\0';i++);
        i--; //points to last charcter

        while(i>=0){
                //skip spaces
                while(i>=0 && (str[i]== ' ' || str[i] == '\n' || str[i]=='\t'))
                        i--;
                if(i<0)
                        break;
                end=i; //end of word

                //move to start of word
                while(i>=0 && str[i]!= ' ' && str[i]!='\n' && str[i]!='t')
                        i--;
                start = i+1;

                //print the word

                for(int k=start;k<=end;k++)
                        printf("%c",str[k]);

                printf(" ");
        }
        return 0;
}
```
### Output
```c
Enter a string : hello world
world hello
```
###  47 Write a C program to find the first occurrence of a character in a given string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 47. Write a C program to find the first occurrence of a character in a given string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    char str[100], ch;
    int i;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    printf("Enter character to find: ");
    scanf("%c", &ch);

    for(i = 0; str[i] != '\0'; i++) {
        if(str[i] == ch) {
            printf("First occurrence at index %d\n", i);
            return 0;  // exit after first match
        }
    }

    printf("Character not found\n");

    return 0;
}

```
### Output
```c
Enter a string: viven embedded
Enter character to find: d
First occurrence at index 10
```
###  48. Write a C program to find the last occurrence of a character in a given string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 48. Write a C program to find the last occurrence of a character in a given string*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    char str[100], ch;
    int i, lastIndex = -1;

    // Input string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Input character to search
    printf("Enter the character to find: ");
    scanf("%c", &ch);

    // Find last occurrence
    for (i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch) {
            lastIndex = i;  // update every time the character is found
        }
    }

    if (lastIndex == -1)
        printf("Character '%c' not found in the string.\n", ch);
    else
        printf("Last occurrence of '%c' is at index %d.\n", ch, lastIndex);

    return 0;
}

```
### Output
```c
Enter a string: programming
Enter the character to find: g
Last occurrence of 'g' is at index 10.
```
###  49 Write a C program to search all occurrences of a character in a given string
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 49 Write a C program to search all occurrences of a character in a given string *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    char str[100], ch;
    int i;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    printf("Enter a character to search: ");
    scanf("%c", &ch);

    printf("Occurrences at positions: ");

    for (i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch) {
            printf("%d ", i);
        }
    }

    return 0;
}

```
### Output
```c
Enter a string: Viven Embedded
Enter a character to search: d
Occurrences at positions: 10 11 13
```
###  50. Write a C program to count occurrences of a character in a given string.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 50. Write a C program to count occurrences of a character in a given string.*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    char str[100], ch;
    int i, count = 0;

    // Input string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Input character
    printf("Enter the character to count: ");
    scanf("%c", &ch);

    // Count occurrences
    for (i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch) {
            count++;
        }
    }

    printf("Character '%c' occurs %d time(s) in the string.\n", ch, count);

    return 0;
}

```
### Output
```c
Enter a string: viven embedded
Enter the character to count: d
Character 'd' occurs 3 time(s) in the string.
```
