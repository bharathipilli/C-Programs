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
