###  1.Creating and displaying list
```c
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
 *  1.Creating and displaying list  *
 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node *next;
};

void display(struct node *temp) {
    while(temp != NULL) {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    printf("NULL");
}

int main() {
    struct node *head, *second, *third;

    head = malloc(sizeof(struct node));
    second = malloc(sizeof(struct node));
    third = malloc(sizeof(struct node));

    head->data = 10;
    head->next = second;

    second->data = 20;
    second->next = third;

    third->data = 30;
    third->next = NULL;

    display(head);
    return 0;
}

```
### Output
```c
10 -> 20 -> 30 -> NULL 
```
