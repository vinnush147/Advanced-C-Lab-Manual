### EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
c
```
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void display()  
{
    struct Node *temp = malloc (sizeof(struct Node));
    temp = head;
    while(temp != NULL){
        printf("%c\n", temp->data);
        temp = temp->next;
    }
}
```

Output:
<img width="359" height="449" alt="12(1)" src="https://github.com/user-attachments/assets/caa29567-2f88-4c60-918e-0a363c20f87e" />



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



### EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
c
```
struct Node   
{  
char data[20];  
struct Node *next;  
}*head;  
void pop()  
{
    struct Node *temp = malloc(sizeof(struct Node));
    if(head == NULL){
        printf("stack is empty\n");
    }
    else{
        temp = head;
        head = temp->next;
    }
}

```

Output:

<img width="1033" height="621" alt="12(2)" src="https://github.com/user-attachments/assets/a602adab-f76c-4cd6-9143-c79c3c555d54" />


Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
### EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
c
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *temp = front;
    if(temp == NULL){
        printf("queue is empty\n");
    }
    else{
        printf("queue elements:\n");
        while(temp != NULL){
            printf("%c\n", temp->data);
            temp = temp->next;
        }
    }
}

```

Output:
<img width="568" height="510" alt="12(3)" src="https://github.com/user-attachments/assets/562634f0-81e2-4d1e-89d2-6b09170e1560" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
### EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
c
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node *n = malloc (sizeof(struct Node));
    n->data = data;
    n->next = NULL;
    if(front == NULL){
        front = rear = n;
    }
    else{
        rear->next = n;
        rear = n;
    }
}

```

Output:

<img width="576" height="521" alt="12(4)" src="https://github.com/user-attachments/assets/9584aef2-e6fb-4b7a-9f52-3e3606b28b18" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



### EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
c
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%c\n", front->data);
}

```

Output:
<img width="387" height="525" alt="12(5)" src="https://github.com/user-attachments/assets/3ce2957c-b708-4c46-9e95-9a0d1324d61c" />



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
