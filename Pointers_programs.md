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
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 2. Find the sum of all elements in an array using pointers  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
```c

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
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 3. Find the maximum element in an array.using pointers       *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
 ```c

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
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 4. Find the minimum element in an array.using pointers       *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /
 ```c                                                            
 
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

### Output
```c
Enter size of array: 5
Enter 5 elements: 12 43 5 67 78
Minimum element = 5

```
5. Count the number of even and odd numbers in an array using pointers
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 5. Count the number of even and odd numbers in an array using pointers *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /
```c

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

### Output
```c
Enter size of array: 5
Enter 5 elements: 12 65 23 76 90
Even numbers = 3
Odd numbers  = 2

```

6. Reverse the elements of an array using pointers 
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 6. Reverse the elements of an array using pointers *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /
```c

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
### Output
```c
Enter size of array: 4
Enter 4 elements: 2 3 4 5
Reversed array: 5 4 3 2

```

7. Copy elements of one array into another array using pointers
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 7. Copy elements of one array into another array using pointers
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /
```c

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
### Output
```c
Enter size of array: 5
Enter 5 elements for  first array: 2 3 4 5 6
Elements of second array: 2 3 4 5 6
```
8. Find the average of all elements in an array using pointers
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* 8. Find the average of all elements in an array using pointers
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * /
```c
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

### Output
```c
Enter size of array: 5
Enter 5 elements: 9 8 7 6 5
Average of all elements = 7.00
```

