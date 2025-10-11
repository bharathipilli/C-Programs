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
### 16. Merge two arrays into third using pointers
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *16. Merge two arrays into third using pointers *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n1, n2, i;
    printf("Enter size of first array: ");
    scanf("%d", &n1);

    int arr1[n1];
    printf("Enter %d elements of first array: ", n1);
    for (i = 0; i < n1; i++) {
        scanf("%d", &arr1[i]);
    }

    printf("Enter size of second array: ");
    scanf("%d", &n2);

    int arr2[n2];
    printf("Enter %d elements of second array: ", n2);
    for (i = 0; i < n2; i++) {
        scanf("%d", &arr2[i]);
    }

    int arr3[n1 + n2];   // merged array
    int *ptr1 = arr1, *ptr2 = arr2, *ptr3 = arr3;

    // Copy arr1 into arr3
    for (i = 0; i < n1; i++) {
        *(ptr3++) = *(ptr1++);
    }

    // Copy arr2 into arr3
    for (i = 0; i < n2; i++) {
        *(ptr3++) = *(ptr2++);
    }

    printf("Merged array: ");
    for (i = 0; i < n1 + n2; i++) {
        printf("%d ", arr3[i]);
    }

    return 0;
}
```
### Output
```c
Enter size of first array: 3
Enter 3 elements of first array: 20 30 40
Enter size of second array: 3
Enter 3 elements of second array: 10 50 60
Merged array: 20 30 40 10 50 60
```
### 17. Sort an array in ascending order (without using built-in sort).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *17. Sort an array in ascending order (without using built-in sort). *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
int main(){
        int n,i,j,temp;

        printf("Enter the size of the array:");
        scanf("%d",&n);

        int arr[n];
        int *ptr=arr;

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr+i));
        }

        for(i=0;i<n-1;i++){
                for(j=0;j<n-1-i;j++){
                        if(*(ptr+j) > *(ptr+j+1)){
                                temp = *(ptr+j);
                                *(ptr+j) = *(ptr+j+1);
                                *(ptr+j+1)=temp;
                        }
                }
        }

        printf("After sorting result of array = \n ");
        for(i=0;i<n;i++){
                printf("%d\t",*(ptr+i));
        }

        return 0;
}
### Output
```c
Enter the size of the array:5
Enter 5 elements : 10 4 9 2 5
After sorting result of array = 2 4 5 9 10
```
### 18. Sort an array in descending order.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *18. Sort an array in descending order. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,j,temp;

        printf("Enter the size of the array:");
        scanf("%d",&n);

        int arr[n];

        int *ptr=arr;

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr+i));
        }

        for(i=0;i<n-1;i++){
                for(j=0;j<n-1-i;j++){
                        if(*(ptr+j) <  *(ptr+j+1)){
                                temp = *(ptr+j);
                                *(ptr+j) =  *(ptr+j+1);
                                *(ptr+j+1)=temp;
                        }
                }
        }

        printf("After sorting result of array = \n ");
        for(i=0;i<n;i++){
                printf("%d\n",*(ptr+i));
        }

        return 0;
}
```
### Output
```c
Enter the size of the array:5
Enter 5 elements : 4 2 8 5 1
After sorting result of array = 8 5 4 2 1
```
### 19. Find the sum of all elements at even indices.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *19. Find the sum of all elements at even indices. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
int main(){
        int n,i,sum=0;


        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];

        int *ptr=arr;
        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr +i));
        }
        for(i=0;i<n;i++){
                if(i % 2==0){
                        sum += *(ptr+i);
                }
        }

        printf("Sum of all even indices = %d\n", sum);

        return 0;
}
```
### Output
```c
Enter the size of the array : 5
Enter 5 elements : 0 1 2 3 4
Sum of all even indices = 6
```
### 20. Rotate an array by k positions (left rotation).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 20. Rotate an array by k positions (left rotation). *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,j,k,temp;

        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];
        int *ptr=arr;
        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr + i));
        }

        printf("Number of positions to shift: ");
        scanf("%d",&k);

        k = k % n;

        for(i=0;i < k ; i++){
                temp = *( ptr + 0 );
                for(j=0;j<n-1;j++){
                        *(ptr + j) = *(ptr + j +1);
                }
                *(ptr + n -1) = temp;
        }

        printf(" Array after %d left rotations : \n ",k);
        for(i=0;i<n;i++){
                printf(" %d ",*(ptr+i));
        }

        return 0;
}
```
### Output
```c
Enter the size of the array : 5
Enter 5 elements : 1 2 3 4 5
Number of positions to shift: 2
 Array after 2 left rotations :  3 4 5 1 2
```
### 21.Rotate an array by k positions (right rotation)
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 21 Rotate an array by k positions (right rotation) *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,k,i,j,temp;

        printf("Enter the size of the array :");
        scanf("%d",&n);

        int arr[n];
        int *ptr = arr;
        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr +i));
        }

        printf("Enter number of postions to rotate(k) : ");
        scanf("%d",&k);

        //Normalize k

        k= k%n;

        //perform rotation k times

        for(i=0;i<k;i++){
                temp = *(ptr+n-1);  //it stores last element
                for(j= n-1;j>0;j--){
                        *(ptr +j) = *(ptr+j-1); //shift right
                }
                *(ptr+0) = temp; //it puts last element at first index
        }

        printf("Array after %d right rotations :\n ",k);
        for(i=0;i<n;i++){
                printf("%d ",*(ptr+i));
        }

        printf("\n");
        return 0;
}
```
### Output
```c
Enter the size of the array :5
Enter 5 elements : 1 2 3 4 5
Enter number of postions to rotate(k) : 2
Array after 2 right rotations :
 4 5 1 2 3
```
### 22. Find duplicate elements in an array using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 22. Find duplicate elements in an array using pointers.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,j,k,found;

        printf("Enter the size of array : ");
        scanf("%d",&n);

        int arr[n];
        int *ptr=arr;
        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",(ptr+i));
        }
        printf("Duplicate elements are : \n");
        for(i=0;i<n;i++){
                found=0;
                for(j=0;j<i;j++){
                        if (*(ptr+i) == *(ptr+j)){
                                found = 1;
                                break;
                        }
                }
                if(found)
                        continue;
                for(j=i+1;j<n;j++){
                        if(*(ptr+i)  == *(ptr+j)){
                                printf("%d ",*(ptr+i));
                                break;
                        }

                }
        }
        printf("\n");
        return 0;
}
```
### Output
```c
Enter the size of array : 5
Enter 5 elements : 1 2 1 2 3
Duplicate elements are :
1 2
```
### 23. Remove duplicate elements from an array using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 23. Remove duplicate elements from an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i, j, k;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr; // pointer to array

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i)); // input using pointer
    }

    // Remove duplicates
    for (i = 0; i < n; i++) {
        for (j = i + 1; j < n; j++) {
            if (*(ptr + i) == *(ptr + j)) {
                // Shift elements left
                for (k = j; k < n - 1; k++) {
                    *(ptr + k) = *(ptr + k + 1);
                }
                n--;   // reduce array size
                j--;   // recheck current index after shifting
            }
        }
    }

    printf("Array after removing duplicates:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", *(ptr + i)); // printing using pointer
    }
    printf("\n");

    return 0;
}


```
### Output
```c
Enter size array : 5
Enter 5 elements : 1 2 1 3 4
Array after removing duplicates :
1 2 3 4
```
### 24. Find the element that appears only once in an array where every other element appears twice using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  24. Find the element that appears only once in an array where every other element appears twice.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, result = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr; // pointer to the array

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));  // input using pointer
    }

    // XOR all the elements using pointer
    for (i = 0; i < n; i++) {
        result ^= *(ptr + i);  // accessing with pointer
    }

    printf("The element that appears only once is : %d\n", result);

    return 0;
}

```
### Output
```c
Enter size of array: 5
Enter 5 elements: 10 20 30 20 30
The element that appears only once is : 10
```
### 25. Find the intersection of two arrays using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 25. Find the intersection of two arrays using pointers.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n1, n2, i, j;

    printf("Enter size of first array: ");
    scanf("%d", &n1);
    int arr1[n1];
    int *p1 = arr1;   // pointer to first array

    printf("Enter %d elements: ", n1);
    for (i = 0; i < n1; i++) {
        scanf("%d", (p1 + i));   // input using pointer
    }

    printf("Enter size of second array: ");
    scanf("%d", &n2);
    int arr2[n2];
    int *p2 = arr2;   // pointer to second array

    printf("Enter %d elements: ", n2);
    for (i = 0; i < n2; i++) {
        scanf("%d", (p2 + i));   // input using pointer
    }

    printf("Intersection of the two arrays:\n");
    for (i = 0; i < n1; i++) {
        for (j = 0; j < n2; j++) {
            if (*(p1 + i) == *(p2 + j)) {   // compare using pointers
                printf("%d ", *(p1 + i));   // print element using pointer
                break; 
            }
        }
    }
    printf("\n");

    return 0;
}

```
### Output
```c
Enter size of first array: 5
Enter 5 elements: 1 2 3 4 5
Enter size of second array: 5
Enter 5 elements: 3 4 5 6 7
Intersection of the two arrays:
3 4 5
```
### 26. Find the union of two arrays using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 26. Find the union of two arrays.*
#include <stdio.h>

int main() {
    int n1, n2, i, j, k = 0;

    printf("Enter size of the first array: ");
    scanf("%d", &n1);

    int arr1[n1];
    printf("Enter elements of first array: ");
    int *ptr1 = arr1; 
    for (i = 0; i < n1; i++) {
        scanf("%d", (ptr1 + i));
    }

    printf("Enter size of the second array: ");
    scanf("%d", &n2);

    int arr2[n2];
    printf("Enter elements of second array: ");
    int *ptr2 = arr2;  
    for (i = 0; i < n2; i++) {
        scanf("%d", (ptr2 + i));
    }

    int unionArr[n1 + n2];
    int *ptrU = unionArr;  // pointer to union array

    // Copy arr1 into unionArr
    for (i = 0; i < n1; i++) {
        *(ptrU + k) = *(ptr1 + i);
        k++;
    }

    // Add arr2 elements if not already present
    for (i = 0; i < n2; i++) {
        int found = 0;
        for (j = 0; j < k; j++) {
            if (*(ptr2 + i) == *(ptrU + j)) {
                found = 1;
                break;
            }
        }
        if (!found) {
            *(ptrU + k) = *(ptr2 + i);
            k++;
        }
    }

    // Print union
    printf("Union of arrays: ");
    for (i = 0; i < k; i++) {
        printf("%d ", *(ptrU + i));
    }

    return 0;
}

```
### Output
```c
Enter size of the first array : 5
Enter elements of first array : 1 2 3 4 5
Enter size of the second array : 5
Enter elements of first array : 3 4 5 6 7
Union of arrays : 1234567
```
### 27. Insert an element at a given position in an array using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 27. Insert an element at a given position in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, pos, i, element;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[50];
    int *ptr = arr;  

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));  
    }

    // Input element and position
    printf("Enter element to insert: ");
    scanf("%d", &element);
    printf("Enter position (1 to %d): ", n + 1);
    scanf("%d", &pos);

    if (pos < 1 || pos > n + 1) {
        printf("Invalid position!\n");
    } else {
        // Shift elements to the right using pointers
        for (i = n; i >= pos; i--) {
            *(ptr + i) = *(ptr + i - 1);
        }

        *(ptr + pos - 1) = element; // Insert element using pointer
        n++; // Increase size

        
        printf("Array after insertion: ");
        for (i = 0; i < n; i++) {
            printf("%d ", *(ptr + i));
        }
    }

    return 0;
}

```
### Output
```c
Enter size of array: 5
Enter 5 elements:
20 40 50 60 70
Enter element to insert: 30
Enter position (1 to 6): 2
Array after insertion: 20 30 40 50 60 70
```
### 28. Delete an element from a given position in an array using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *28. Delete an element from a given position in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, pos, i;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[50];  
    int *ptr = arr;   

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i)); 
    }

    // Position to delete
    printf("Enter position to delete (1 to %d): ", n);
    scanf("%d", &pos);

    if (pos < 1 || pos > n) {
        printf("Invalid position!\n");
    } else {
        // Shift elements to left using pointer
        for (i = pos - 1; i < n - 1; i++) {
            *(ptr + i) = *(ptr + i + 1);
        }
        n--;  // size decreases

        printf("Array after deletion: ");
        for (i = 0; i < n; i++) {
            printf("%d ", *(ptr + i));
        }
    }

    return 0;
}

```
### Output
```c
Enter size of array: 5
Enter 5 elements:
20 45 67 83 49
Enter position to delete (1 to 5): 3
Array after deletion: 20 45 83 49
```
### 29. Count the frequency of a specific element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *29. Count the frequency of a specific element in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, element, count = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[50];
    int *ptr = arr;  

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));   
    }

    printf("Enter element to find frequency: ");
    scanf("%d", &element);

    for (i = 0; i < n; i++) {
        if (*(ptr + i) == element) {
            count++;
        }
    }
    printf("Frequency of %d = %d\n", element, count);

    return 0;
}

```
### Output
```c
Enter size of array: 5
Enter 5 elements:
18 1 18 27 31
Enter element to find frequency: 18
Frequency of 18 = 2
```
### 30.Find the largest and smallest element in a single scan.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *30.Find the largest and smallest element in a single scan.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr=arr;
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int max = *(ptr+0), min = *(ptr+0);

    // Single scan
    for (i = 1; i < n; i++) {
        if (*(ptr+i) > max)
            max = *(ptr+i);
        if (*(ptr+i) < min)
            min = *(ptr+i);
    }

    printf("Largest element = %d\n", max);
    printf("Smallest element = %d\n", min);

    return 0;
}
```
### Output
```c
Enter size of array: 5
Enter 5 elements:
45 89 34 12 9
Largest element = 89
Smallest element = 9
```
### 31.Rearrange an array so that all negative numbers appear before positive numbers using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *31. Rearrange an array so that all negative numbers appear before positive numbers*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter array elements: ");
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int *left = arr;          // Pointer to start
    int *right = arr + n - 1; // Pointer to end
    int temp;

    // Rearrange negatives before positives
    while (left < right) {
        // Move left forward if it's already negative
        while (*left < 0 && left < right)
            left++;

        // Move right backward if it's already positive
        while (*right >= 0 && left < right)
            right--;

        // Swap if left is positive and right is negative
        if (left < right) {
            temp = *left;
            *left = *right;
            *right = temp;
        }
    }

    printf("Rearranged array: ");
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

    return 0;
}
```
### Output
```c
Enter the size: 6
Enter the elements : 1 2 3 0 -1 -3
Rearranged array : -3 -1 3 0 2 1
```
### 32. Rearrange an array so that even numbers come before odd numbers using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *32. Rearrange an array so that even numbers come before odd numbers.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter array elements: ");
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int *left = arr;          
    int *right = arr + n - 1; 
    int temp;

    // Rearrange even numbers before odd numbers
    while (left < right) {
        // Move left forward if even
        while (*left % 2 == 0 && left < right)
            left++;

        // Move right backward if odd
        while (*right % 2 != 0 && left < right)
            right--;

        // Swap if left is odd and right is even
        if (left < right) {
            temp = *left;
            *left = *right;
            *right = temp;
        }
    }

    printf("Rearranged array (even before odd): ");
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

    return 0;
}

```
### Output
```c
Enter size of array: 6
Enter 6 elements:
1 4 6 2 7 3
Rearranged array : 2 4 6 1 7 3
```
### 33. Find the first repeating element in an array using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *33. Find the first repeating element in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", arr + i);  
    }

    int *p1, *p2;
    int found = 0;

    // Find first repeating element using pointers
    for (p1 = arr; p1 < arr + n; p1++) {
        for (p2 = p1 + 1; p2 < arr + n; p2++) {
            if (*p1 == *p2) {
                printf("First repeating element is: %d\n", *p1);
                found = 1;
                break;
            }
        }
        if (found)
            break;
    }

    if (!found)
        printf("No repeating elements found.\n");

    return 0;
}


```
### Output
```c
Enter size of array: 6
Enter 6 elements: 1 2 3 3 4 5
First repeating element: 3
```
### 34. Find the first non-repeating element in an array using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *34. Find the first non-repeating element in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", arr + i);  // Using pointer to take input
    }

    int *p1, *p2;
    int found = 0;

    // Find first non-repeating element
    for (p1 = arr; p1 < arr + n; p1++) {
        int count = 0;
        for (p2 = arr; p2 < arr + n; p2++) {
            if (*p1 == *p2)
                count++;
        }
        if (count == 1) {  // Appears only once
            printf("First non-repeating element is: %d\n", *p1);
            found = 1;
            break;
        }
    }

    if (!found)
        printf("No non-repeating element found.\n");

    return 0;
}

```
### Output
```c
Enter size of array: 6
Enter 6 elements:
4 5 6 7 5 4
First non-repeating element: 6
```
### 35. Find the missing number in an array containing numbers from 1 to n using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *35. Find the missing number in an array containing numbers from 1 to n.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, total = 0, sum = 0;
    printf("Enter total numbers from 1 to n: ");
    scanf("%d", &n);

    int arr[n - 1]; // one number is missing

    printf("Enter %d numbers (from 1 to %d, one missing):\n", n - 1, n);
    int *ptr;

    // Using pointer to read and calculate sum
    for (ptr = arr; ptr < arr + (n - 1); ptr++) {
        scanf("%d", ptr);
        sum += *ptr;  // Add value pointed by ptr
    }

    total = n * (n + 1) / 2; // Sum of 1 to n

    printf("Missing number = %d\n", total - sum);

    return 0;
}

```
### Output
```c
Enter total numbers from 1 to n: 5
Enter 4 numbers (from 1 to 5, one missing): 2 3 4 5 6
Missing number = 1
```
### 36. Find the pair of elements whose sum is equal to a given number k using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *36. Find the pair of elements whose sum is equal to a given number k.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, k, found = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", arr + i);  // using pointer for input
    }

    printf("Enter the value of k (target sum): ");
    scanf("%d", &k);

    int *p1, *p2;

    // Find pair with sum = k using pointers
    for (p1 = arr; p1 < arr + n; p1++) {
        for (p2 = p1 + 1; p2 < arr + n; p2++) {
            if (*p1 + *p2 == k) {
                printf("Pair found: (%d, %d)\n", *p1, *p2);
                found = 1;
            }
        }
    }

    if (!found)
        printf("No pair found with sum %d.\n", k);

    return 0;
}

```
### Output
```c
Enter size of array: 5
Enter 5 elements: 2 3 4 5 6
Enter the value of k (target sum): 6
Pair found: (2, 4)
```
### 37.Find the majority element (element occurring more than n/2 times) using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *37. Find the majority element (element occurring more than n/2 times).*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, count, found = 0;
    printf("Enter size of array: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", arr + i);  // Using pointer to input values
    }

    int *p1, *p2;

    // Check frequency of each element using pointers
    for (p1 = arr; p1 < arr + n; p1++) {
        count = 0;

        for (p2 = arr; p2 < arr + n; p2++) {
            if (*p1 == *p2)
                count++;
        }

        if (count > n / 2) {
            printf("Majority element = %d\n", *p1);
            found = 1;
            break;
        }
    }

    if (!found)
        printf("No majority element found.\n");

    return 0;
}

```
### Output
```c
Enter size of array: 6
Enter 6 elements: 1 2 2 2 2 3
Majority element = 2
```
### 38. Move all zeros to the end of the array using pointers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *38. Move all zeros to the end of the array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", arr + i);  // using pointer for input
    }

    int *p, *q;
    q = arr; // q points to the position where next non-zero element will go

    // Move non-zero elements to the front
    for (p = arr; p < arr + n; p++) {
        if (*p != 0) {
            *q = *p;
            q++;
        }
    }
    // Filling remaining elements with zero
    while (q < arr + n) {
        *q = 0;
        q++;
    }

    // Print the updated array
    printf("Array after moving zeros to the end:\n");
    for (p = arr; p < arr + n; p++) {
        printf("%d ", *p);
    }

    return 0;
}

```
### Output
```c
Enter size of array: 6
Enter 6 elements: 1 0 3 4 0 5 
Array after moving zeros to the end: 1 3 4 5 0 0 
```
### 39. Find the maximum product of two elements in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *39. Find the maximum product of two elements in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n;
    int *p1, *p2;
    int maxProduct, num1, num2;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", arr + i);  // using pointer for input
    }

    // Assume first two elements as having the maximum product
    maxProduct = arr[0] * arr[1];
    num1 = arr[0];
    num2 = arr[1];

    // Check every possible pair using pointers
    for (p1 = arr; p1 < arr + n; p1++) {
        for (p2 = p1 + 1; p2 < arr + n; p2++) {
            int product = (*p1) * (*p2);
            if (product > maxProduct) {
                maxProduct = product;
                num1 = *p1;
                num2 = *p2;
            }
        }
    }

    printf("Maximum product is %d (from %d × %d)\n", maxProduct, num1, num2);

    return 0;
}

```
### Output
```c
Enter size of array: 6
Enter 6 elements: 1 2 3 4 5 6
Maximum product is 30 (from 5 × 6)
```
### 40. Find the maximum sum of a contiguous subarray (Kadane’s Algorithm).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *40. Find the maximum sum of a contiguous subarray (Kadane’s Algorithm).*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int *ptr = arr;
    int current_sum = *ptr;
    int max_sum = *ptr;

    ptr++; // move pointer to next element

    for (i = 1; i < n; i++, ptr++) {
        // choose between current element or add to current sum
        if (*ptr > current_sum + *ptr)
            current_sum = *ptr;
        else
            current_sum = current_sum + *ptr;

        // update maximum sum
        if (current_sum > max_sum)
            max_sum = current_sum;
    }

    printf("Maximum sum of contiguous subarray = %d\n", max_sum);

    return 0;
}

```
### Output
```c
Enter size of array: 8
Enter 8 elements: -2 -3 4 -1 -2 1 5 -3
Maximum sum of a contiguous subarray = 7
```
### 41. Find the minimum sum of a contiguous subarray.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 41. Find the minimum sum of a contiguous subarray. *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int current_sum = arr[0];
    int min_sum = arr[0];

    for (i = 1; i < n; i++) {
        // either start new subarray or add to current one
        if (arr[i] < current_sum + arr[i])
            current_sum = arr[i];
        else
            current_sum = current_sum + arr[i];

        // update overall minimum
        if (current_sum < min_sum)
            min_sum = current_sum;
    }

    printf("Minimum sum of contiguous subarray = %d\n", min_sum);

    return 0;
}
```
### Output
```c
Enter size of array: 7
Enter 7 elements: 3 -4 2 -3 -1 7 -5
Minimum sum of contiguous subarray = -6
```
### 42. Find the length of the longest increasing subsequence
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *42. Find the length of the longest increasing subsequence *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, j, max = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n], lis[n];
    int *ptr = arr;   // pointer for main array
    int *lptr = lis;  // pointer for LIS array

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));
        *(lptr + i) = 1;  // each element has LIS length 1 initially
    }

    // Calculate LIS using pointers
    for (i = 1; i < n; i++) {
        for (j = 0; j < i; j++) {
            if (*(ptr + i) > *(ptr + j) && *(lptr + i) < *(lptr + j) + 1) {
                *(lptr + i) = *(lptr + j) + 1;
            }
        }
    }

    // Find maximum value in LIS array
    for (i = 0; i < n; i++) {
        if (max < *(lptr + i))
            max = *(lptr + i);
    }

    printf("Length of the longest increasing subsequence = %d\n", max);

    return 0;
}

```
### Output
```c
Enter size of array: 8
Enter 8 elements: 10 22 9 33 21 50 41 60
Length of the longest increasing subsequence = 5
```
### 43. Find the length of the longest subarray with sum equal to k.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *43. Find the length of the longest subarray with sum equal to k. *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, k, i, j;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));
    }

    printf("Enter the target sum (k): ");
    scanf("%d", &k);

    int maxLen = 0;

    // Check all subarrays using pointer arithmetic
    for (i = 0; i < n; i++) {
        int sum = 0;
        for (j = i; j < n; j++) {
            sum += *(ptr + j);  // add current element

            if (sum == k) {
                int len = j - i + 1;
                if (len > maxLen)
                    maxLen = len;
            }
        }
    }

    printf("Length of longest subarray with sum %d = %d\n", k, maxLen);

    return 0;
}

```
### Output
```c
Enter size of array: 5
Enter 5 elements: 1 2 4 5 6
Enter the target sum (k): 11
Length of longest subarray with sum 11 = 3
```
### 44. Find the maximum difference between two elements such that larger comes after smaller. uisng arrays
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *44. Find the maximum difference between two elements such that larger comes after smaller. uisng arrays *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", (ptr + i));
    }

    int min = *ptr;               // first element as initial minimum
    int maxDiff = *(ptr + 1) - *ptr; // initial max difference

    for (i = 1; i < n; i++) {
        if (*(ptr + i) - min > maxDiff)
            maxDiff = *(ptr + i) - min;

        if (*(ptr + i) < min)
            min = *(ptr + i);
    }

    printf("Maximum difference = %d\n", maxDiff);

    return 0;
}

```
### Output
```c
Enter size of array: 7
Enter 7 elements: 1 2 5 2 3 5 3
Maximum difference = 4
```
### 45. Implement binary search on a sorted array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 45. Implement binary search on a sorted array. *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i, target;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;  // pointer to the array

    printf("Enter %d sorted elements:\n", n);
    for (i = 0; i < n; i++)
        scanf("%d", ptr + i);  // input via pointer

    printf("Enter element to search: ");
    scanf("%d", &target);

    int low = 0, high = n - 1, mid, found = 0;

    while (low <= high) {
        mid = (low + high) / 2;

        if (*(ptr + mid) == target) {
            found = 1;
            break;
        } else if (target < *(ptr + mid)) {
            high = mid - 1;
        } else {
            low = mid + 1;
        }
    }

    if (found)
        printf("Element %d found at index %d\n", target, mid);
    else
        printf("Element %d not found in the array.\n", target);

    return 0;
}

```
### Output
```c
Enter size of array: 6
Enter 6 sorted elements: 1 3 4 5 6 7
Enter element to search: 5
Element 5 found at index 3
```
### 46. Merge two sorted arrays into a single sorted array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 46. Merge two sorted arrays into a single sorted array. *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n1, n2, i = 0, j = 0, k = 0;

    printf("Enter size of first sorted array: ");
    scanf("%d", &n1);
    int arr1[n1], arr2[n2], merged[n1 + n2];
    int *ptr1 = arr1, *ptr2 = arr2, *mPtr = merged;

    printf("Enter %d elements of first array:\n", n1);
    for (i = 0; i < n1; i++)
        scanf("%d", ptr1 + i);

    printf("Enter size of second sorted array: ");
    scanf("%d", &n2);
    printf("Enter %d elements of second array:\n", n2);
    for (i = 0; i < n2; i++)
        scanf("%d", ptr2 + i);

    i = j = k = 0;

    // Merge arrays
    while (i < n1 && j < n2)
        *(mPtr + k++) = (*(ptr1 + i) < *(ptr2 + j)) ? *(ptr1 + i++) : *(ptr2 + j++);

    // Copy remaining elements
    while (i < n1) *(mPtr + k++) = *(ptr1 + i++);
    while (j < n2) *(mPtr + k++) = *(ptr2 + j++);

    // Print merged array
    printf("Merged array: ");
    for (i = 0; i < n1 + n2; i++)
        printf("%d ", *(mPtr + i));
    printf("\n");

    return 0;
}

```
### Output
```c
Enter size of first sorted array: 3
Enter 3 elements of first array: 1 2 3
Enter size of second sorted array: 3
Enter 3 elements of second array: 4 5 6
Merged array: 1 2 3 4 5 6
```
### 47. Find the kth smallest element in an array. 
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 47. Find the kth smallest element in an array.  *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, k, i, j, temp;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;  // pointer to the array

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++)
        scanf("%d", ptr + i);  // input using pointer

    printf("Enter k: ");
    scanf("%d", &k);

    // Sort array in ascending order using pointers
    for(i = 0; i < n-1; i++) {
        for(j = 0; j < n-i-1; j++) {
            if(*(ptr + j) > *(ptr + j + 1)) {
                temp = *(ptr + j);
                *(ptr + j) = *(ptr + j + 1);
                *(ptr + j + 1) = temp;
            }
        }
    }

    printf("The %dth smallest element = %d\n", k, *(ptr + k - 1));

    return 0;
}

```
### Output
```c
Enter size of array: 7
Enter 7 elements: 2 5 3 8 4 6 1
Enter k: 4
The 4th smallest element = 4
```
### 48. Find the kth largest element in an array. 
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 48. Find the kth largest element in an array.  *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, k, i, j, temp;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    int *ptr = arr;  // pointer to the array

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++)
        scanf("%d", ptr + i);

    printf("Enter k: ");
    scanf("%d", &k);

    // Sort array in ascending order using pointers
    for(i = 0; i < n-1; i++) {
        for(j = 0; j < n-i-1; j++) {
            if(*(ptr + j) > *(ptr + j + 1)) {
                temp = *(ptr + j);
                *(ptr + j) = *(ptr + j + 1);
                *(ptr + j + 1) = temp;
            }
        }
    }

    printf("The %dth largest element = %d\n", k, *(ptr + n - k));

    return 0;
}

```
### Output
```c
Enter size of array: 6
Enter 6 elements: 7 10 4 3 20 15
Enter k: 3
The 3th largest element = 10
```
