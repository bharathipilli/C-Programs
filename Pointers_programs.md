1. Input an array of size n and print all elements using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
Input an array of size n and print all elements using pointers *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;
        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];
        int *ptr = arr; //pointer points to first element of array

        printf("Enter %d elements ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr + i )); //moves the pointer to the i-th element of the array
        }

        printf("Array elements are :" );
        for(i=0;i<n;i++){
                printf("%d ", *(ptr + i));//// accessing using pointer
        }

        return 0;

}
```
### Output
```c
Enter the size of the array : 5
Enter 5 elements 10 20 30 40 50
Array elements are :10 20 30 40 50
```

2. Find the sum of all elements in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 2. Find the sum of all elements in an array using pointers  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */


#include<stdio.h>
int main(){
        int n,i,sum=0;

        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];
        int *ptr = arr ; //// pointer to array

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr + i)); // store input using pointer
        }

        for(i=0;i<n;i++){
                sum += *(ptr + i); //adds each element’s value to the total.
        }

        printf("Sum of all the elements = %d\n",sum);

        return 0;
}
```
### Output
```c
Enter the size of the array : 3
Enter 3 elements : 10 20 40
Sum of all the elements = 70

```
3. Find the maximum element in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 3. Find the maximum element in an array.using pointers       *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */


#include<stdio.h>
int main(){

        int n,i;

        printf("Enter the size of the array : " );
        scanf("%d",&n);

        int arr[n];

        int *ptr = arr ;



        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr + i));
        }

        int max = *ptr; //assume first element is max
        for(i=0;i<n;i++){
                if(*(ptr + i) > max){
                        max = *(ptr + i );
                }
        }

        printf("Maximum element = %d\n",max);

        return 0;
}
```
### Output
```c
Enter the size of the array : 5
Enter 5 elements : 23 56 123 67 43 90
Maximum element = 123

```

4. Find the minimum element in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 4. Find the minimum element in an array.using pointers       *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /                                               
 
#include <stdio.h>

int main() {
    int n, i;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;   // pointer to array

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));   // input using pointer
    }

    int min = *ptr;   // assume first element is minimum

    for (i = 1; i < n; i++) {
        if (*(ptr + i) < min) {
            min = *(ptr + i);    // update min
        }
    }

    printf("Minimum element = %d\n", min);

    return 0;
}                                                        
```
### Output
```c
Enter size of array: 5
Enter 5 elements: 12 43 5 67 78
Minimum element = 5

```
5. Count the number of even and odd numbers in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 5. Count the number of even and odd numbers in an array using pointers *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /
#include <stdio.h>
int main() {
    int n, i;
    int even = 0, odd = 0;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;   

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));   
    }

    for (i = 0; i < n; i++) {
        if (*(ptr + i) % 2 == 0) {
            even++;   // count even
        } else {
            odd++;    // count odd
        }
    }

    printf("Even numbers = %d\n", even);
    printf("Odd numbers  = %d\n", odd);

    return 0;
}
```
### Output
```c
Enter size of array: 5
Enter 5 elements: 12 65 23 76 90
Even numbers = 3
Odd numbers  = 2

```

6. Reverse the elements of an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 6. Reverse the elements of an array using pointers *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /

#include <stdio.h>

int main() {
    int n, i;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;   

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));   
    }

    // Reverse the array using two pointers
    int *start = ptr;          // points to first element
    int *end = ptr + n - 1;    // points to last element

    while (start < end) {
        int temp = *start;
        *start = *end;
        *end = temp;

        start++;
        end--;
    }

    printf("Reversed array: ");
    for (i = 0; i < n; i++) {
        printf("%d ", *(ptr + i));   // print reversed array
    }

    return 0;
}
```
### Output
```c
Enter size of array: 4
Enter 4 elements: 2 3 4 5
Reversed array: 5 4 3 2

```

7. Copy elements of one array into another array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 7. Copy elements of one array into another array using pointers
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /

#include <stdio.h>

int main() {
    int n, i;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr1[n], arr2[n];   // source and destination arrays
    int *ptr1 = arr1;       // pointer to arr1
    int *ptr2 = arr2;       // pointer to arr2

    printf("Enter %d elements for first array: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr1 + i));   // input elements into arr1
    }

    // Copy elements from arr1 to arr2
    for (i = 0; i < n; i++) {
        *(ptr2 + i) = *(ptr1 + i);   // copying using pointers
    }

    printf("Elements of second array: ");
    for (i = 0; i < n; i++) {
        printf("%d ", *(ptr2 + i));   // print arr2
    }

    return 0;
}
```
### Output
```c
Enter size of array: 5
Enter 5 elements for  first array: 2 3 4 5 6
Elements of second array: 2 3 4 5 6
```
8. Find the average of all elements in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 8. Find the average of all elements in an array using pointers
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /

#include <stdio.h>

int main() {
    int n, i, sum = 0;
    float avg;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;   

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));   
    }

    for (i = 0; i < n; i++) {
        sum += *(ptr + i);        // add elements using pointer
    }

    avg = (float)sum / n;         // calculate average

    printf("Average of all elements = %.2f\n", avg);

    return 0;
}
```
### Output
```c
Enter size of array: 5
Enter 5 elements: 9 8 7 6 5
Average of all elements = 7.00
```
9. Search for a given element in an array (linear search) using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 9. Search for a given element in an array (linear search) using pointers
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /
#include <stdio.h>

int main() {
    int n, key, i, found = 0;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr; 

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));  
    }

    printf("Enter the element to search: ");
    scanf("%d", &key);

    for (i = 0; i < n; i++) {
        if (*(ptr + i) == key) {   // compare using pointer
            found = 1;
            break;   // stop searching when found
        }
    }

    if (found) {
        printf("Element %d found at position %d\n", key, i + 1);
    } else {
        printf("Element %d not found in the array\n", key);
    }

    return 0;
}
```
### Output
```c
Enter size of array: 5
Enter 5 elements: 11 22 33 44 55
Enter the element to search: 33
Element 33 found at position 3
```
### 10.Count the number of positive, negative, and zero elements in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 10.Count the number of positive, negative, and zero elements in an array using pointers
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /

#include <stdio.h>

int main() {
    int n, i, positive = 0, negative = 0, zero = 0;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;   // pointer to array

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));  
    }

    for (i = 0; i < n; i++) {
        if (*(ptr + i) > 0) {
            positive++;
        } else if (*(ptr + i) < 0) {
            negative++;
        } else {
            zero++;
        }
    }

    printf("Positive elements = %d\n", positive);
    printf("Negative elements = %d\n", negative);
    printf("Zero elements = %d\n", zero);

    return 0;
}
```
### Output
```c
Enter size of array: 6
Enter 6 elements: 6 5 0 7 -9 0
Positive elements = 3
Negative elements = 1
Zero elements = 2
```
### 11. Print array elements in alternate positions (odd/even indices) using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 11. Print array elements in alternate positions (odd/even indices) using pointers  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;
        printf("Enter size: ");
        scanf("%d",&n);

        int arr[n];
        int *ptr=arr;

        printf("Enter %d elements: ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr+i));
        }

        printf("Elements at even indices are : ");

        for(i=0;i<n;i+=2){
                printf("%d ",*(ptr+i));
        }

        printf("\n");

        printf("Elements at odd  indices are : ");

        for(i=1;i<n;i+=2){
                printf("%d ",*(ptr+i));
        }

        return 0;
}
```
### Output
```c
Enter array size :6
Enter 6 elements:20 30 40 50 60 70
Elements at even indices are : 20 40 60
Elements at odd  indices are : 30 50 70 
```
### 12. Find the second largest element in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 12. Find the second largest element in an array using pointers  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;
        printf("Enter the array size : ");
        scanf("%d",&n);

        int arr[n];
        int *ptr=arr;

        printf("Enter %d elements " ,n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr +i));
        }

        int max1,max2;

        if( *(ptr +0) > *(ptr + 1) ){
                max1 = *(ptr+0);
                max2 = *(ptr +1);
        }else{
                max1 = *(ptr+1);
                max2 = *(ptr +0);
        }

        for(i=2;i<n;i++){
                if(*(ptr +i) >  max1){
                        max2 = max1;
                        max1 = *(ptr + i);
                }else if ( *(ptr + i ) >  max2 && *(ptr+i) != max1){                        max2=*(ptr +i );
                }
        }

        printf("Largest  element = %d\n",max1);
        printf("Second largest  element = %d\n ",max2);

        return 0;
}
```
### Output
```c
Enter size of array: 5
Enter 5 elements: 23 45 78 54 98
Largest element = 98
Second largest element = 78
```
### 13. Find the second smallest element in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *13. Find the second smallest element in an array using pointers  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;
        printf("Enter the array size : ");
        scanf("%d",&n);

        int arr[n];
        int *ptr=arr;

        printf("Enter %d elements " ,n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr +i));
        }

        int min1,min2;

        if( *(ptr +0) < *(ptr + 1) ){
                min1 = *(ptr+0);
                min2 = *(ptr +1);
        }else{
                min1 = *(ptr+1);
                min2 = *(ptr +0);
        }

        for(i=2;i<n;i++){
                if(*(ptr +i) < min1){
                        min2 = min1;
                        min1 = *(ptr + i);
                }else if ( *(ptr + i )< min2 && *(ptr+i) != min1){
                        min2=*(ptr +i );
                }
        }

        printf("Smallest element = %d\n",min1);
        printf("Second smallest element = %d\n ",min2);

        return 0;
}

```
### Output
```c
Enter size of array: 5
Enter 5 elements: 12 43 5 67 16
Smallest element = 5
Second smallest element = 12
```
### 14. Check if an array is sorted in ascending order using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *14. Check if an array is sorted in ascending order using pointers  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;
        printf("Enter size : ");
        scanf("%d",&n);

        int arr[n];

        int *ptr =arr;

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr +i));
        }

        i=0;


        while(i < n-1 && *(ptr + i) <=  *(ptr + i+ 1) ){
                i++;
        }

        if( i == n-1)
                printf("The array is sorted in ascending order \n");
        else
                printf("The array is not sorted in ascending order\n");
        return 0;
}
```
### Output
```c
Enter the size of the array :5
Enter 5 elements : 12 54 67 76 98
The array is sorted in ascending order
```

### 15. Find the frequency of each element in an array using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *15. Find the frequency of each element in an array using pointers *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, j, count;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;  // pointer to first element

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));   // store using pointer
    }

    printf("\nFrequency of each element:\n");
    for (i = 0; i < n; i++) {
        count = 1;

        // check if already counted
        for (j = 0; j < i; j++) {
            if (*(ptr + i) == *(ptr + j)) {
                count = 0;
                break;
            }
        }

        if (count == 0)
            continue;

        // count frequency
        for (j = i + 1; j < n; j++) {
            if (*(ptr + i) == *(ptr + j)) {
                count++;
            }
        }

        printf("%d occurs %d times\n", *(ptr + i), count);
   }
   return 0;
}
```
### Output
```c
Enter size of array: 6
Enter 6 elements: 1 4 1 3 5 3

Frequency of each element:
1 occurs 2 times
4 occurs 1 times
3 occurs 2 times
5 occurs 1 times
```
