### 1.Create a structure to represent a student with the following members: name (string),
roll number (int), and marks (float). Write a function to display the details of a student
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * Create a structure to represent a student with the following members: name (string), 
roll number (int), and marks (float). Write a function to display the details of a student    *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
struct student
{
        char name[50];
        int rollnum;
        float marks;
};
int main(){

        struct student st1={"Ramu",1,98.690};

        struct student st2={"Mamazen",2,83.780};

        struct student st3={"Abdul",3,85.40};

        printf("%s %d %.2f \n",st1.name,st1.rollnum,st1.marks);
        printf("%s %d %.2f \n",st2.name,st2.rollnum,st2.marks);
        printf("%s %d %.2f \n",st3.name,st3.rollnum,st3.marks);
        return 0;
}

```
### Output
```c
Ramu 1 98.69
Mamazen 2 83.78
Abdul 3 85.40
```

### 2.Define a union to store either an integer or a floatingpoint number. 
Write a function to accept the type of data (integer or float) and then 
read the corresponding value from the user. Store the value in the union and print it.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 2.Define a union to store either an integer or a floatingpoint number. 
Write a function to accept the type of data (integer or float) and then 
read the corresponding value from the user. Store the value in the union and print it.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>

union number{
        int i;
        float f;
};

//function to accept and display value

void readValue(){

        union number num;
        int choice;

        printf("Enter data type(1 for integer , 2 for float) : ");
        scanf("%d",&choice);

        if(choice ==1){
                printf("enter integer value : ");
                scanf("%d",&num.i);
                printf("you entered : %d\n",num.i);

        }

        else if(choice == 2){
                printf("enter float value : ");
                scanf("%f",&num.i);
                printf("you entered : %.2f\n",num.f);
        }
        else{
                printf("Invalid choice ");
        }
}
int main(){
        readValue();
        return 0;
}

```
### Output
```c
Enter data type(1 for integer , 2 for float) : 2
enter float value : 12.34
you entered : 12.34
```
### 3.Define a structure to represent a point in 2D space with x and y coordinates 
(both integers). Write a function to check if two points are equal (have the same x and y 
coordinates).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * Define a structure to represent a point in 2D space with x and y coordinates 
(both integers). Write a function to check if two points are equal (have the same x and y 
coordinates).   *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
struct point
{
        int x;
        int y;
};
int areEqual(struct point p1,struct point p2){
        if(p1.x == p2.x && p1.y == p2.y )
                return 1;
        else
                return 0;
}

int main(){
        struct point a,b;

        printf("enter x and y for point 1 : ");
        scanf("%d %d",&a.x,&a.y);

        printf("enter x and y for point 2 : ");
        scanf("%d %d",&b.x,&b.y);

        if(areEqual(a,b))
                printf("Points are equal\n");
        else
                printf("points are not equal\n");
        return 0;
}

```
### Output
```c
enter x and y for point 1 : 2 3
enter x and y for point 2 : 2 3
Points are equal
```
### 4.Create a structure to represent a book with the following members: title (string),
author (string), ISBN (long int), and number of pages (int). Write a function to accept 
details of a book from the user and store them in a structure variable.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  4.Create a structure to represent a book with the following members: title (string),
author (string), ISBN (long int), and number of pages (int). Write a function to accept 
details of a book from the user and store them in a structure variable.*
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
struct book
{
        char title[100];
        char author[100];
        long int ISBN;
        int pages;
};
void detailsOfBook(struct book *b){
        printf("enter title : ");
        scanf("%s",b->title);

        printf("enter author : ");
        scanf("%s",b->author);

        printf("enter ISBN :");
        scanf("%ld",&b->ISBN);

        printf("enter number of pages : ");
        scanf("%d",&b->pages);
}

int main(){

        struct book b1;

        printf("--enter book details --\n");
        detailsOfBook(&b1);
        printf("\n");
        printf("---Book Details ---\n");
        printf("Tile : %s\n",b1.title);
        printf("Author : %s\n",b1.author);
        printf("ISBN : %ld\n",b1.ISBN);
        printf("Pages : %d\n",b1.pages);

        return 0;
}
```
### Output
```c
--enter book details --
enter title : Bhagavadgita
enter author : Veda Vyasa
enter ISBN :enter number of pages :
---Book Details ---
Tile : Bhagavadgita
Author : Veda Vyasa
ISBN :  978-9352581078
Pages : 938

```
### 5. Define a union to represent the size of a product, which can be specified in centimeters,
inches, or feet. Write a function to convert the size from one unit to another (e.g., centimeters 
to inches)
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 5. Define a union to represent the size of a product, which can be specified in centimeters,
inches, or feet. Write a function to convert the size from one unit to another (e.g., centimeters 
to inches)    *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
union size
{
        float cm;
        float inch;
        float feet;
};
//simple function to convert
float convert(float value, int choice){
        if(choice==1)                     //cm->inches
                return value/2.54;
        else                              //inchem->cm
                return value * 2.54;
}

int main(){
        union size s;
        int choice;
        float result;

        printf("1.convert cm to inches\n");
        printf("2.convert inches to cm\n");
        printf("enter your choice : ");
        scanf("%d",&choice);

        if(choice == 1){
                printf("enter value in cm : ");
                scanf("%f",&s.cm);
                result=convert(s.cm,1);
                printf("Inches = %.2f\n",result);
        }

        else if(choice==2){
                printf("enter value in iches: ");
                scanf("%f",&s.inch);
                result=convert(s.inch,2);
                printf("Centimeters = %.2f\n",result);
        }
         else{
                printf("Invalid choice\n");
        }
        return 0;
}

```
### Output
```c
1.convert cm to inches
2.convert inches to cm
enter your choice : 1
enter value in cm : 2.5
Inches = 0.98
```
### 6. Define a structure to represent a date with day, month, and year (all integers). 
Write a function to check if a given year is a leap year.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  6. Define a structure to represent a date with day, month, and year (all integers). 
Write a function to check if a given year is a leap year.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
struct date
{
        int day;
        int month;
        int year;
};
//function to check leap year
int isleap(int year){
        if((year%400 == 0) || (year%4==0 && year%100!=0))
                return 1;
        else
                return 0;
}

int main(){

        struct date d;

        printf("enter day month year : ");
        scanf("%d %d %d",&d.day,&d.month,&d.year);

        if(isleap(d.year))
                printf("%d is a leap year\n",d.year);
        else
                printf("%d is not a leap year\n",d.year);

        return 0;
}

```
### Output
```c
enter day month year : 31 10 1973
1973 is not a leap year
```
### 7. Define a structure to represent a complex number with real and imaginary parts 
(both floats). Write a function to add two complex numbers represented by structures.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  7. Define a structure to represent a complex number with real and imaginary parts 
(both floats). Write a function to add two complex numbers represented by structures.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
struct complex
{
        float real;
        float img;
};
struct complex add(struct complex c1,struct complex c2){
        struct complex result;
        result.img=c1.img+c2.img;
        result.real=c1.img + c2.real;

        return result;
}

int main(){
        struct complex c1,c2,sum;

        printf("enter first complex number(real ,imaginary) :");
        scanf("%f%f\n",&c1.real,&c1.img);

        printf("enter second complex number (real ,imaginary) : ");
        scanf("%f%f\n",&c2.real,&c2.img);

        sum=add(c1,c2);

        printf("Sum = %.2f+%.2fi\n",sum.real,sum.img);

        return 0;
}

```
### Output
```c
enter first complex number(real ,imaginary) :2 3
enter second complex number (real ,imaginary) : 2 4
Sum = 7.00+8.00i
```
### 8. Implement a linked list using structures. Each node in the list should hold an 
integer value and a pointer to the next node.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  8. Implement a linked list using structures. Each node in the list should hold an 
integer value and a pointer to the next node.  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node* next;
};
int main(){
        struct node *head=NULL,*second=NULL,*third=NULL;

        //allocate memory for 3 nodes

        head=(struct node*)malloc(sizeof(struct node));
        second=(struct node*)malloc(sizeof(struct node));
        third=(struct node*)malloc(sizeof(struct node));

        head->data=10;
        head->next=second;

        second->data=20;
        second->next=third;

        third->data=30;
        third->next=NULL;

        //printing linked list

        struct node *temp=head;
        while(temp!=NULL){
                printf("%d->",temp->data);
                temp=temp->next;
        }

        printf("NULL");
        return 0;
}
```
### Output
```c
10->20->30->NULL
```
### 9. Define a self-referential structure to represent a binary tree node.
Each node should have data (integer) and pointers to left and right child nodes.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *   9. Define a self-referential structure to represent a binary tree node.
Each node should have data (integer) and pointers to left and right child nodes. *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include<stdio.h>
struct node{
        int data;
        struct node *left;
        struct node *right;
};

int main(){

        struct node n1;

        n1.data=10;
        n1.left=NULL;
        n1.right=NULL;

        printf("Node created : %d\n",n1.data);
        printf("Left Node : %d\n",n1.left);
        printf("Right Node : %d\n",n1.right);

        return 0;
}


```
### Output
```c
Node created : 10
Left Node : 0
Right Node : 0
```
### 10. Implement a function that takes a structure representing a date (day, month,
year) and checks if the date is valid (e.g., not exceeding the number of days in a month).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  10. Implement a function that takes a structure representing a date (day, month,
year) and checks if the date is valid (e.g., not exceeding the number of days in a month).   *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>

struct Date {
    int day;
    int month;
    int year;
};

// function to check if year is leap year
int isLeap(int year) {
    return ((year % 400 == 0) || (year % 4 == 0 && year % 100 != 0));
}

// function to check valid date
int isValid(struct Date d) {
    // month range
    if (d.month < 1 || d.month > 12)
        return 0;

    // days in each month
    int daysInMonth;

    switch (d.month) {
        case 1: case 3: case 5: case 7: case 8: case 10: case 12:
            daysInMonth = 31;
            break;
        case 4: case 6: case 9: case 11:
            daysInMonth = 30;
            break;
        case 2:
            if (isLeap(d.year))
                daysInMonth = 29;
            else
                daysInMonth = 28;
            break;
    }
    // day range check
    if (d.day < 1 || d.day > daysInMonth)
        return 0;

    return 1;
}

int main() {
    struct Date d;

    printf("Enter day month year: ");
    scanf("%d %d %d", &d.day, &d.month, &d.year);

    if (isValid(d))
        printf("Valid Date\n");
    else
        printf("Invalid Date\n");

    return 0;
}
```
### Output
```c
Enter day month year: 18 05 2002
Valid Date
```
### 11. Define a union to represent a shape. The union can hold the dimensions of different
shapes like circle (radius), rectangle (length, breadth), or triangle (base, height). 
Write functions to calculate the area of each shape based on the type stored in the union
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *   11. Define a union to represent a shape. The union can hold the dimensions of different
shapes like circle (radius), rectangle (length, breadth), or triangle (base, height). 
Write functions to calculate the area of each shape based on the type stored in the union *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
union Shape {
    float radius;          // for circle
    struct {
        float length;
        float breadth;
    } rect;                // for rectangle
    struct {
        float base;
        float height;
    } tri;                 // for triangle
};

// function to calculate circle area
float circleArea(float r) {
    return 3.14 * r * r;
}

// function to calculate rectangle area
float rectArea(float l, float b) {
    return l * b;
}

// function to calculate triangle area
float triArea(float base, float height) {
    return 0.5 * base * height;
}

int main() {
    union Shape s;
    int choice;

    printf("1. Circle\n");
    printf("2. Rectangle\n");
    printf("3. Triangle\n");
    printf("Enter your choice: ");
    scanf("%d", &choice);

    if (choice == 1) {
        printf("Enter radius: ");
        scanf("%f", &s.radius);
        printf("Area of Circle = %.2f\n", circleArea(s.radius));
    }
    else if (choice == 2) {
        printf("Enter length and breadth: ");
        scanf("%f %f", &s.rect.length, &s.rect.breadth);
        printf("Area of Rectangle = %.2f\n",
               rectArea(s.rect.length, s.rect.breadth));
    }
    else if (choice == 3) {
        printf("Enter base and height: ");
        scanf("%f %f", &s.tri.base, &s.tri.height);
        printf("Area of Triangle = %.2f\n",
               triArea(s.tri.base, s.tri.height));
    }
    else {
        printf("Invalid choice\n");
    }

    return 0;
}
```
### Output
```c
1. Circle
2. Rectangle
3. Triangle
Enter your choice: 1
Enter radius: 4
Area of Circle = 50.24
```
### 12. Define a structure to represent a playing card with suit (enum) and rank (integer).
Write a function to generate a random playing card and another function to print the card's
details.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  12. Define a structure to represent a playing card with suit (enum) and rank (integer).
Write a function to generate a random playing card and another function to print the card's
details.    *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

// enum for suit
enum Suit { HEARTS, DIAMONDS, CLUBS, SPADES };

// structure for a playing card
struct Card {
    enum Suit suit;
    int rank;   // 1–13  (1=Ace, 11=Jack, 12=Queen, 13=King)
};

// function to generate a random card
struct Card generateCard() {
    struct Card c;
    c.suit = rand() % 4;     // 0–3
    c.rank = (rand() % 13) + 1;  // 1–13
    return c;
}

// function to print card details
void printCard(struct Card c) {
    char *suitNames[] = { "Hearts", "Diamonds", "Clubs", "Spades" };

    printf("Card: ");

    // Print rank
    if (c.rank == 1) printf("Ace of ");
    else if (c.rank == 11) printf("Jack of ");
    else if (c.rank == 12) printf("Queen of ");
    else if (c.rank == 13) printf("King of ");
    else printf("%d of ", c.rank);

    // Print suit
    printf("%s\n", suitNames[c.suit]);
}
int main() {
    srand(time(NULL));  // random seed

    struct Card card = generateCard();
    printCard(card);

    return 0;
}
```
### Output
```c
Card: King of Diamonds
```
### 13. Implement a function that takes a structure representing a time (hours, minutes, 
seconds) and performs basic time arithmetic (e.g., adding two time durations).
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *13. Implement a function that takes a structure representing a time (hours, minutes, 
seconds) and performs basic time arithmetic (e.g., adding two time durations).    *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */

#include <stdio.h>

struct Time {
    int h;
    int m;
    int s;
};

// Function to add two time values
struct Time addTime(struct Time t1, struct Time t2)
{
    struct Time result;

    result.s = t1.s + t2.s;
    result.m = t1.m + t2.m + result.s / 60;
    result.h = t1.h + t2.h + result.m / 60;

    result.s = result.s % 60;
    result.m = result.m % 60;

    return result;
}

int main()
{
    struct Time t1, t2, sum;

    printf("Enter first time (h m s): ");
    scanf("%d %d %d", &t1.h, &t1.m, &t1.s);

    printf("Enter second time (h m s): ");
    scanf("%d %d %d", &t2.h, &t2.m, &t2.s);

    sum = addTime(t1, t2);

    printf("Sum of time = %02d:%02d:%02d\n", sum.h, sum.m, sum.s);

    return 0;
}

```
### Output
```c
Enter first time (h m s): 2 13 30
Enter second time (h m s): 1 20 12
Sum of time = 03:33:42
```
### 14. Create a structure to represent a student enrollment record with student ID 
(string), course name (string), and grade (character). Write functions to add a new record 
to an array of structures and to search for a record based on student ID.
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 14. Create a structure to represent a student enrollment record with student ID 
(string), course name (string), and grade (character). Write functions to add a new record 
to an array of structures and to search for a record based on student ID.   *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
#include <string.h>

#define MAX 100

struct Enrollment {
    char studentID[20];
    char courseName[50];
    char grade;
};

// Function to add a new record
void addRecord(struct Enrollment records[], int *count) {
    printf("Enter Student ID: ");
    scanf("%s", records[*count].studentID);

    printf("Enter Course Name: ");
    scanf("%s", records[*count].courseName);

    printf("Enter Grade: ");
    scanf(" %c", &records[*count].grade);

    (*count)++;
    printf("Record added successfully!\n\n");
}

// Function to search by student ID
void searchRecord(struct Enrollment records[], int count) {
    char searchID[20];
    printf("Enter Student ID to search: ");
    scanf("%s", searchID);

    for (int i = 0; i < count; i++) {
        if (strcmp(records[i].studentID, searchID) == 0) {
            printf("\nRecord Found:\n");
            printf("Student ID: %s\n", records[i].studentID);
            printf("Course Name: %s\n", records[i].courseName);
            printf("Grade: %c\n", records[i].grade);
            return;
        }
    }

    printf("\nRecord Not Found!\n");
}

int main() {
    struct Enrollment records[MAX];
    int count = 0;
    int choice;

    while (1) {
        printf("1. Add Record\n");
        printf("2. Search Record\n");
        printf("3. Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                addRecord(records, &count);
                break;
            case 2:
                searchRecord(records, count);
                break;
            case 3:
                return 0;
            default:
                printf("Invalid choice! Try again.\n");
        }
    }

    return 0;
}
```
### Output
```c
1. Add Record
2. Search Record
3. Exit
Enter choice: 1
Enter Student ID: n180094
Enter Course Name: Linux
Enter Grade: 98
Record added successfully!
```
### 15.Write a C program to store employee details which contains three structures first structure contains personal details of employee ( i.e. first name ,last name ,employee number ) second structure contains address (i.e. city ,state , street number and house number) and third structure contains 2 pointer to structure of first and second structure and one self-reference pointer
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 * 15.Write a C program to store employee details which contains three structures first structure contains personal details of employee ( i.e. first name ,last name ,employee number ) second structure contains address (i.e. city ,state , street number and house number) and third structure contains 2 pointer to structure of first and second structure and one self-reference pointer   *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
#include <stdlib.h>
// First structure: Personal details 
struct Personal {
    char firstName[30];
    char lastName[30];
    int empNo;
};

// Second structure: Address 
struct Address {
    char city[30];
    char state[30];
    int streetNo;
    int houseNo;
};

// Third structure: contains pointers 
struct Employee {
    struct Personal *p;      // pointer to first structure
    struct Address *a;       // pointer to second structure
    struct Employee *next;   // self-referential pointer
};

int main() {
    // Create objects of first two structures 
    struct Personal per;
    struct Address add;

    //Input personal details 
    printf("Enter first name: ");
    scanf("%s", per.firstName);

    printf("Enter last name: ");
    scanf("%s", per.lastName);

    printf("Enter employee number: ");
    scanf("%d", &per.empNo);

    // Input address details 
    printf("Enter city: ");
    scanf("%s", add.city);

    printf("Enter state: ");
    scanf("%s", add.state);

    printf("Enter street number: ");
    scanf("%d", &add.streetNo);

    printf("Enter house number: ");
    scanf("%d", &add.houseNo);

    // Create third structure object 
    struct Employee emp;

    emp.p = &per;    // pointing to personal structure
    emp.a = &add;    // pointing to address structure
    emp.next = NULL; // no next employee (single node)

    // Display details using third structure 
    printf("\n--- Employee Details ---\n");
    printf("Name: %s %s\n", emp.p->firstName, emp.p->lastName);
    printf("Employee Number: %d\n", emp.p->empNo);
    printf("Address: House No %d, Street No %d, %s, %s\n",
           emp.a->houseNo,
           emp.a->streetNo,
           emp.a->city,
           emp.a->state);

    return 0;
}
```
### Output
```c
Enter first name: Bharathi
Enter last name: Pilli
Enter employee number: 101
Enter city: Hyderabad
Enter state: Telangana
Enter street number: 12
Enter house number: 45

--- Employee Details ---
Name: Bharathi Pilli
Employee Number: 101
Address: House No 45, Street No 12, Hyderabad, Telangana

```
