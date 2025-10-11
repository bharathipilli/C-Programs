###  1. Input an array of size n and print all elements.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  1. Input an array of size n and print all elements.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include<stdio.h>
int main(){
        int n,i;
         // Step 1: Input array size
        printf("Enter size of the array:");
        scanf("%d",&n);
        // Step 2: Declare array of size n
        int arr[n];
        // Step 3: Input elements
        printf("Enter the elements : ");
        for(i=1;i<=n;i++){
                scanf("%d",&arr[i]);
        }

        printf("The elements of array are :\n ");
        for(i=1;i<=n;i++){
                printf("%d\n",arr[i]);
        }
        return 0;
}
```
### Output
```c
Enter size of the array:5
Enter the elements : 2 3 4 5 6
The elements of array are : 2 3 4 5 6
```
### 2. Find the sum of all elements in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 2. Write a c to Find the sum of all elements in an array.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,sum=0;
        printf("Enter the size of the array :");
        scanf("%d",&n);

        int arr[n];

        printf("Enter the %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
                sum += arr[i];
        }
        printf("The sum of the elements are : %d\n ",sum);

        return 0;
}
```
### Output
```c
Enter the size of the array : 3
Enter the 5 elements : 2 3 6
The sum of the elements are : 11
```                   
### 3. Find the maximum element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 3. Find the maximum element in an array.                 *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,max;

        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter the elements : ");
        for(i=0;i<=n;i++){
                scanf("%d",&arr[i]);
        }

        max=arr[0];
        for(i=1;i<=n;i++){
                if (arr[i]>max){
                        max = arr[i];
                }
        }

        printf("Max element in the array is : %d \n ",max);

        return 0;
}
```
### Output
```c
Enter the size of the array : 5
Enter the elements : 2 4 5 1 4 3
Max element in the array is : 5
```
### 4. Find the minimum element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 4. Find the minimum element in an array.                 *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,min;
        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter the %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        min =arr[0];

        for(i=1;i<n;i++){
                if(arr[i]<min){
                        min=arr[i];
                }
        }

        printf("The minimum element in the array is : %d ", min);

        return 0;
}
```
### Output
```c
Enter the size of the array : 5
Enter the 5 elements : 2 5 6 1 7 8
The minimum element in the array is : 1
```
### 5. Count the number of even and odd numbers in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 5. Count the number of even and odd numbers in an array.                 *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;
        int even=0,odd=0;

        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter the %d  elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        for(i=0;i<n;i++){
                if(arr[i]%2==0){
                        even++;
                }else{
                        odd++;
                }
        }

        printf("The count of even are %d :\n",even);
        printf("The count of odd are %d :\n", odd);
        return 0;
}
```
### Output
```c
Enter the size of the array : 6
Enter the 6  elements : 2 9 5 6 8 1 3
The count of even are : 3
The count of odd are : 3
```
### 6. Reverse the elements of an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 6. Reverse the elements of an array.                 *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include<stdio.h>
int main(){
        int n,i;
        printf("enter the size of the array :");
        scanf("%d",&n);

        int arr[n];

        printf("Enter the elements : ");
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        for(i=n-1;i>=0;i--){
                printf("%d",arr[i]);
        }

        return 0;
}
```
### Output
```c
enter the size of the array :5
Enter the elements : 1 2 3 4 5
5
4
3
2
1
```
### 7. Copy elements of one array into another array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *7. Copy elements of one array into another array.               *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;

        printf("Enter the size of the array : ");

        scanf("%d",&n);

        int arr1[n],arr2[n];

        printf("Enter the elements : ");
        for(i=0;i<n;i++){
                scanf("%d",&arr1[i]);
        }

        // Copy arr1 into arr2
        for(i=0;i<n;i++){
                arr2[i]= arr1[i];
        }

        printf("Copied array : ");
        for(i=0;i<n;i++){
                printf("%d\n",arr2[i]);
        }

        return 0;
}
```
### Output
```c
Enter the size of the array: 5
Enter 5 elements: 2 4 6 8 1
Copied array (arr2): 2 4 6 8 1
```
### 8. Find the average of all elements in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 8. Find the average of all elements in an array.               *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include<stdio.h>
int main(){
        int n,i;
        float sum=0,avg;

        printf("Enter size of the array : ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);

                // Add each element to sum
                sum+=arr[i];
        }
        avg = sum/n;    //Formula for average

        printf("Average of array elements : %.2f\n",avg);

        return 0;
}
```
### Output
```c
Enter size of the array : 5
Enter 5 elements : 1 2 3 4 5
Average of array elements : 3.00
```
### 9. Search for a given element in an array (Linear Search)
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 9. Search for a given element in an array (Linear Search)   *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include <stdio.h>

int main() {
    int n, i, key, found = 0;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter the element to search: ");
    scanf("%d", &key);

    for (i = 0; i < n; i++) {
        if (arr[i] == key) {
            found = 1;
            break;   // stop as soon as we find it
        }
    }

    if (found) {
        printf("Element %d found at position %d\n", key, i + 1); // position = index+1
    } else {
        printf("Element %d not found in the array\n", key);
    }

    return 0;
}
```
### Output
```c
Enter size of array: 6
Enter 6 elements: 2 4 1 5 7 8
Enter the element to search: 7
Element 7 found at position 5
```
### 10. Count the number of positive, negative, and zero elements in an array
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  10. Count the number of positive, negative, and zero elements in an array  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, positive = 0, negative = 0, zero = 0;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    for (i = 0; i < n; i++) {
        if (arr[i] > 0) {
            positive++;
        } else if (arr[i] < 0) {
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
Enter 6 elements: 4 -5 0 2 -3 9
Positive elements = 3
Negative elements = 2
Zero elements = 1
```
### 11. Print array elements in alternate positions (odd/even indices).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 11. Print array elements in alternate positions (odd/even indices).  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;
        printf("Enter array size :");
        scanf("%d",&n);

        int arr[n];

        printf("Enter %d elements:",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        //print elements at even indices

        printf("Elements at even indices are : ");
        for(i=0;i<n;i+=2){
                printf("%d ",arr[i]);
        }

        printf("\n");


         //print elements at odd  indices

        printf("Elements at odd  indices are : ");
        for(i=1;i<n;i+=2){
                printf("%d ",arr[i]);
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
### 12. Find the second largest element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 12. Find the second largest element in an array.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>

int main() {
    int n, i;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int max1,max2;

    // Initialize with first two elements by comparing which is largest
    if (arr[0] >  arr[1]) {
        max1 = arr[0];
        max2 = arr[1];
    } else {
        max1 = arr[1];
        max2 = arr[0];
    }

    // Traverse the rest of the array
    for (i = 2; i < n; i++) {
        if (arr[i] > max1) {
            max2 = max1;   // old smallest becomes second smallest
            max1 = arr[i]; // new smallest
        } else if (arr[i] > max2 && arr[i] != max1) {
            max2 = arr[i];
        }
    }

    printf("Largest element = %d\n", max1);
    printf("Second largest element = %d\n", max2);

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
### 13. Find the second smallest element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *13. Find the second smallest element in an array.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include<stdio.h>

int main() {
    int n, i;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int min1, min2;

    // Initialize with first two elements
    if (arr[0] < arr[1]) {
        min1 = arr[0];
        min2 = arr[1];
    } else {
        min1 = arr[1];
        min2 = arr[0];
    }

    // Traverse the rest of the array
    for (i = 2; i < n; i++) {
        if (arr[i] < min1) {
            min2 = min1;   // old smallest becomes second smallest
            min1 = arr[i]; // new smallest
        } else if (arr[i] < min2 && arr[i] != min1) {
            min2 = arr[i];
        }
    }

    printf("Smallest element = %d\n", min1);
    printf("Second smallest element = %d\n", min2);

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
### 14. Check if an array is sorted in ascending order.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *14. Check if an array is sorted in ascending order.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include<stdio.h>
int main(){
        int n,i;

        printf("Enter the size of the array :");
        scanf("%d",&n);

        int arr[n];

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        i=0;

        while(i < n-1 && arr[i]<= arr[i+1]){
                i++;
        }

        if(i == n-1 )
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

### 15. Find the frequency of each element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *15. Find the frequency of each element in an array. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i, j, count;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("\nFrequency of each element:\n");
    for (i = 0; i < n; i++) {
        count = 1; // start counting

        // skip if element already counted
        for (j = 0; j < i; j++) {
            if (arr[i] == arr[j]) {
                count = 0;
                break;
            }
        }

        if (count == 0)
            continue;

        // count frequency
        for (j = i + 1; j < n; j++) {
            if (arr[i] == arr[j]) {
                count++;
            }
        }

        printf("%d occurs %d times\n", arr[i], count);
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
### 16. Merge two arrays into a third array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *16.Merge two arrays into a third array. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include<stdio.h>
int main(){i
        int n1,n2,n3,i,j;

        printf("Enter size of the first array : ");
        scanf("%d",&n1);

        int arr1[n1];

        printf("Enter %d elements of first array : ",n1);
        for(i=0;i<n1;i++){
                scanf("%d",&arr1[i]);
        }

        printf("Enter size of the second  array : ");
        scanf("%d",&n2);

        int arr2[n2];

        printf("Enter %d elements of second array : ",n2);
        for(i=0;i<n2;i++){
                scanf("%d",&arr2[i]);
        }

        n3= n1+n2;

        int arr3[n3];

        //copy arr1 into arr3

       for(i=0;i<n1;i++){
                arr3[i] = arr1[i];
       }
        //copy arr2 into arr3

       for(j=0;j<n2;j++){
                arr3[i] = arr2[j];
                i++;
        }
       printf("Merged array : ");
       for(i=0;i<n3;i++){
                 printf("%d ", arr3[i]);
        }
       return 0;
}
```
### Output
```c
 Enter size of first array: 3
Enter 3 elements of first array: 10 20 30
Enter size of second array: 2
Enter 2 elements of second array: 40 50
Merged array: 10 20 30 40 50
```
### 17. Sort an array in ascending order (without using built-in sort).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *17. Sort an array in ascending order (without using built-in sort). *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,j,temp;

        printf("Enter the size of the array:");
        scanf("%d",&n);

        int arr[n];

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        for(i=0;i<n-1;i++){
                for(j=0;j<n-1-i;j++){
                        if(arr[j] > arr[j+1]){
                                temp = arr[j];
                                arr[j] = arr[j+1];
                                arr[j+1]=temp;
                        }
                }
        }

        printf("After sorting result of array = \n ");
        for(i=0;i<n;i++){
                printf("%d",arr[i]);
        }

        return 0;
}
```
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

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        for(i=0;i<n-1;i++){
                for(j=0;j<n-1-i;j++){
                        if(arr[j] <  arr[j+1]){
                                temp = arr[j];
                                arr[j] = arr[j+1];
                                arr[j+1]=temp;
                        }
                }
        }

        printf("After sorting result of array = \n ");
        for(i=0;i<n;i++){
                printf("%d",arr[i]);
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
#include<stdio.h>
int main(){
        int n,i,sum=0;

        printf("Enter the size of the array : ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        for(i=0;i<n;i++){
                if(i % 2==0){
                        sum += arr[i];
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

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        printf("Number of positions to shift: ");
        scanf("%d",&k);

        k = k % n;

        for(i=0;i < k ; i++){
                temp = arr[0];
                for(j=0;j<n-1;j++){
                        arr[j] = arr[j+1];
                }
                arr[n-1] = temp;
        }

        printf(" Array after %d left rotations : \n ",k);
        for(i=0;i<n;i++){
                printf(" %d ",arr[i]);
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

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        printf("Enter number of postions to rotate(k) : ");
        scanf("%d",&k);

        //Normalize k

        k= k%n;

        //perform rotation k times

        for(i=0;i<k;i++){
                temp = arr[n-1];  //it stores last element
                for(j= n-1;j>0;j--){
                        arr[j] = arr[j-1]; //shift right
                }
                arr[0] = temp; //it puts last element at first index
        }

        printf("Array after %d right rotations :\n ",k);
        for(i=0;i<n;i++){
                printf("%d ",arr[i]);
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
### 22. Find duplicate elements in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 22. Find duplicate elements in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,j,k,found;

        printf("Enter the size of array : ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }
        printf("Duplicate elements are : \n");
        for(i=0;i<n;i++){
                found=0;
                for(j=0;j<i;j++){
                        if (arr[i] == arr[j]){
                                found = 1;
                                break;
                        }
                }
                if(found)
                        continue;
                for(j=i+1;j<n;j++){
                        if(arr[i] == arr[j]){
                                printf("%d ",arr[i]);
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
### 23. Remove duplicate elements from an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 23. Remove duplicate elements from an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,j,k;

        printf("Enter size array : ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter %d elements : ",n);
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }

        for(i=0;i<n;i++){
                for(j =i+1;j<n;j++){
                        if(arr[i] == arr[j]){
                                for(k=j;k<n-1;k++){
                                        arr[k] =arr[k+1];
                                }
                                n--;
                                j--;
                        }
                }
        }
        printf("Array after removing duplicates : \n");
        for(i=0;i<n;i++){
                printf("%d ",arr[i]);
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
### 24. Find the element that appears only once in an array where every other element appears twice.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  24. Find the element that appears only once in an array where every other element appears twice.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i,result=0;

         printf("Enter size of array: ");
                scanf("%d", &n);

        int arr[n];
        printf("Enter %d elements: ", n);
        for (i = 0; i < n; i++) {
                scanf("%d", &arr[i]);
        }

        //XOR all the elements

        for(i=0;i<n;i++){
                result ^=arr[i];
        }

        printf("The element that appears only once is : %d\n",result);
        return 0;
}
```
### Output
```c
Enter size of array: 5
Enter 5 elements: 10 20 30 20 30
The element that appears only once is : 10
```
### 25. Find the intersection of two arrays.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 25. Find the intersection of two arrays.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n1, n2, i, j;

    printf("Enter size of first array: ");
    scanf("%d", &n1);
    int arr1[n1];
    printf("Enter %d elements: ", n1);
    for (i = 0; i < n1; i++) {
        scanf("%d", &arr1[i]);
    }

    printf("Enter size of second array: ");
    scanf("%d", &n2);
    int arr2[n2];
    printf("Enter %d elements: ", n2);
    for (i = 0; i < n2; i++) {
        scanf("%d", &arr2[i]);
    }

    printf("Intersection of the two arrays:\n");
    for (i = 0; i < n1; i++) {
        for (j = 0; j < n2; j++) {
            if (arr1[i] == arr2[j]) {
                printf("%d ", arr1[i]);
                break; // it stop checking arr2 once a match is found
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
### 26. Find the union of two arrays.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 26. Find the union of two arrays.*
#include<stdio.h>
int main(){

        int n1,n2,i,j,k=0;

        printf("Enter size of the first array : ");
        scanf("%d",&n1);

        int arr1[n1];
        printf("Enter elements of first array : ");
        for(i=0;i<n1;i++){
                scanf("%d",&arr1[i]);
        }

        int arr2[n2];

        printf("Enter size of the second array : ");
        scanf("%d",&n2);

        printf("Enter elements of first array : ");
        for(int i=0;i<n2;i++){
                scanf("%d",&arr2[i]);
        }

        int unionArr[n1+n2];

        // copy arr1 into unionArr

        for(i=0;i<n1;i++){
                unionArr[k++] = arr1[i];
        }

        //add elements of arr2 if not already in result

        for(i=0;i<n2;i++){
                int found =0;
                for(j=0;j<k;j++){
                        if (arr2[i] == unionArr[j]){
                                found = 1;
                                break;
                        }
                }
                if(!found){
                        unionArr[k++] = arr2[i];
                }
        }

        //step 3: print union

        printf("Union of arrays : ");
        for(i=0;i<k;i++){
                printf("%d",unionArr[i]);
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
### 27. Insert an element at a given position in an array.
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
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Input element and position
    printf("Enter element to insert: ");
    scanf("%d", &element);
    printf("Enter position (1 to %d): ", n+1);
    scanf("%d", &pos);

    if (pos < 1 || pos > n+1) {
        printf("Invalid position!\n");
    } else {
        // Shift elements to right
        for (i = n; i >= pos; i--) {
            arr[i] = arr[i-1];
        }

        arr[pos-1] = element; // Insert at correct place
        n++; // Size increased

        // Print array after insertion
        printf("Array after insertion: ");
        for (i = 0; i < n; i++) {
            printf("%d ", arr[i]);
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
### 28. Delete an element from a given position in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *28. Delete an element from a given position in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, pos, i;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // position to delete
    printf("Enter position to delete (1 to %d): ", n);
    scanf("%d", &pos);

    if (pos < 1 || pos > n) {
        printf("Invalid position!\n");
    } else {
        // Shift elements to left
        for (i = pos - 1; i < n - 1; i++) {
            arr[i] = arr[i + 1];
        }
        n--; 

        printf("Array after deletion: ");
        for (i = 0; i < n; i++) {
            printf("%d ", arr[i]);
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

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter element to find frequency: ");
    scanf("%d", &element);

    // Count frequency
    for (i = 0; i < n; i++) {
        if (arr[i] == element) {
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
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int max = arr[0], min = arr[0];

    // Single scan
    for (i = 1; i < n; i++) {
        if (arr[i] > max)
            max = arr[i];
        if (arr[i] < min)
            min = arr[i];
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
### 31.Rearrange an array so that all negative numbers appear before positive numbers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *31. Rearrange an array so that all negative numbers appear before positive numbers*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
int main(){
        int n,i;

        printf("Enter the size: ");
        scanf("%d",&n);

        int arr[n];

        printf("Enter the elements : ");
        for(i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }


        int left =0,right = n-1;

        while(left < right){
                while(arr[left]< 0 && left < right)
                        left++;
                while(arr[right]>=0 && left< right)
                        right--;


                if(left < right){
                        int temp = arr[left];
                        arr[left] = arr[right];
                        arr[right]=temp;
                }
        }
        printf("Rearranged array : \n");
        for(i=0;i<n;i++){
                printf("%d",arr[i]);
        }

        return 0;
}
```
### Output
```c
Enter the size: 6
Enter the elements : 1 2 3 0 -1 -3
Rearranged array : -3 -1 3 0 2 1
```
### 32. Rearrange an array so that even numbers come before odd numbers.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *32. Rearrange an array so that even numbers come before odd numbers.*
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

    int left = 0, right = n - 1;

    while(left<right){
            while (arr[left] % 2==0 && left < right)
                    left++;
    while(arr[right]%2 !=0 && left < right )
            right--;

    if(left<right){
            int temp = arr[left];
            arr[left] = arr[right];
            arr[right]=temp;
          }
    }
    printf("Rearranged array : \n");
    for(i=0;i<n;i++){
            printf("%d",arr[i]);
           }
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
### 33. Find the first repeating element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *33. Find the first repeating element in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i, j, found = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Find first repeating element
    for (i = 0; i < n; i++) {
        for (j = i + 1; j < n; j++) {
            if (arr[i] == arr[j]) {
                printf("First repeating element: %d\n", arr[i]);
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
### 34. Find the first non-repeating element in an array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *34. Find the first non-repeating element in an array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, j, count, found = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Find the first non-repeating element
    for (i = 0; i < n; i++) {
        count = 0;
        for (j = 0; j < n; j++) {
            if (arr[i] == arr[j] && i != j) {
                count++;
                break; // No need to check further if it repeats
            }
        }
        if (count == 0) {
            printf("First non-repeating element: %d\n", arr[i]);
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
### 35. Find the missing number in an array containing numbers from 1 to n.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *35. Find the missing number in an array containing numbers from 1 to n.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, sum = 0, total;

    printf("Enter total numbers from 1 to n: ");
    scanf("%d", &n);

    int arr[n - 1]; // because one number is missing

    printf("Enter %d numbers (from 1 to %d, one missing):\n", n - 1, n);
    for (i = 0; i < n - 1; i++) {
        scanf("%d", &arr[i]);
        sum = sum + arr[i]; // calculate actual sum
    }

    total = n * (n + 1) / 2; // sum of first n natural numbers

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
### 36. Find the pair of elements whose sum is equal to a given number k.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *36. Find the pair of elements whose sum is equal to a given number k.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

int main() {
    int n, i, j, k, found = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter the value of k (target sum): ");
    scanf("%d", &k);

    // Find pair with sum = k
    for (i = 0; i < n; i++) {
        for (j = i + 1; j < n; j++) {
            if (arr[i] + arr[j] == k) {
                printf("Pair found: (%d, %d)\n", arr[i], arr[j]);
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
### 37. 37. Find the majority element (element occurring more than n/2 times).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *37. Find the majority element (element occurring more than n/2 times).*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i, j, count, found = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Check frequency of each element
    for (i = 0; i < n; i++) {
        count = 1;
        for (j = i + 1; j < n; j++) {
            if (arr[i] == arr[j])
                count++;
        }

        if (count > n / 2) {
            printf("Majority element = %d\n", arr[i]);
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
### 38. Move all zeros to the end of the array.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *38. Move all zeros to the end of the array.*
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
int main() {
    int n, i, j = 0;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Move non-zero elements to the front
    for (i = 0; i < n; i++) {
        if (arr[i] != 0) {
            arr[j] = arr[i];
            j++;
        }
    }

    // Fill remaining positions with zeros
    while (j < n) {
        arr[j] = 0;
        j++;
    }

    // Print the updated array
    printf("Array after moving zeros to the end:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
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
    int n, i, j;
    int maxProduct, num1, num2;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    maxProduct = arr[0] * arr[1];  // assume first two as max product
    num1 = arr[0];
    num2 = arr[1];

    // Check every possible pair
    for (i = 0; i < n; i++) {
        for (j = i + 1; j < n; j++) {
            int product = arr[i] * arr[j];
            if (product > maxProduct) {
                maxProduct = product;
                num1 = arr[i];
                num2 = arr[j];
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

    int max_so_far = arr[0];
    int current_sum = arr[0];

    for (i = 1; i < n; i++) {
        // Step 1: Add current element or start new subarray
        if (current_sum + arr[i] > arr[i])
            current_sum = current_sum + arr[i];
        else
            current_sum = arr[i];

        // Step 2: Update max sum if needed
        if (current_sum > max_so_far)
            max_so_far = current_sum;
    }

    printf("Maximum sum of a contiguous subarray = %d\n", max_so_far);

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

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        lis[i] = 1; // each element is LIS of length 1
    }

    // Calculating LIS values in a bottom-up manner
    for (i = 1; i < n; i++) {
        for (j = 0; j < i; j++) {
            if (arr[i] > arr[j] && lis[i] < lis[j] + 1) {
                lis[i] = lis[j] + 1;
            }
        }
    }

    // Find maximum in lis[]
    for (i = 0; i < n; i++) {
        if (max < lis[i])
            max = lis[i];
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
    int n, i, j, k;

    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter the target sum (k): ");
    scanf("%d", &k);

    int maxLen = 0;

    // Check all subarrays
    for (i = 0; i < n; i++) {
        int sum = 0;
        for (j = i; j < n; j++) {
            sum += arr[j];
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
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int min = arr[0];
    int maxDiff = arr[1] - arr[0];

    for (i = 1; i < n; i++) {
        if (arr[i] - min > maxDiff)
            maxDiff = arr[i] - min;

        if (arr[i] < min)
            min = arr[i];
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
    printf("Enter %d sorted elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter element to search: ");
    scanf("%d", &target);

    int low = 0, high = n - 1, mid, found = 0;

    while (low <= high) {
        mid = (low + high) / 2;

        if (arr[mid] == target) {
            found = 1;
            break;
        } else if (target < arr[mid]) {
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
    int arr1[n1];
    printf("Enter %d elements of first array:\n", n1);
    for (i = 0; i < n1; i++) {
        scanf("%d", &arr1[i]);
    }

    printf("Enter size of second sorted array: ");
    scanf("%d", &n2);
    int arr2[n2];
    printf("Enter %d elements of second array:\n", n2);
    for (i = 0; i < n2; i++) {
        scanf("%d", &arr2[i]);
    }

    int mergedArr[n1 + n2];
    i = j = k = 0;

    // Merge arrays
    while (i < n1 && j < n2) {
        if (arr1[i] < arr2[j])
            mergedArr[k++] = arr1[i++];
        else
            mergedArr[k++] = arr2[j++];
    }

    // Copy remaining elements
    while (i < n1)
        mergedArr[k++] = arr1[i++];
    while (j < n2)
        mergedArr[k++] = arr2[j++];

    // Print merged array
    printf("Merged array: ");
    for (i = 0; i < n1 + n2; i++)
        printf("%d ", mergedArr[i]);
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
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    printf("Enter k: ");
    scanf("%d", &k);

    // Sort array using simple bubble sort
    for(i = 0; i < n-1; i++) {
        for(j = 0; j < n-i-1; j++) {
            if(arr[j] > arr[j+1]) {
                temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }

    printf("The %dth smallest element = %d\n", k, arr[k-1]);

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
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    printf("Enter k: ");
    scanf("%d", &k);

    // Sort array in ascending order using bubble sort
    for(i = 0; i < n-1; i++) {
        for(j = 0; j < n-i-1; j++) {
            if(arr[j] > arr[j+1]) {
                temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }

    printf("The %dth largest element = %d\n", k, arr[n - k]);

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

