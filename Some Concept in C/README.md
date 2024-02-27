
**1. Struct in C**
A `struct` (short for structure) in C is a user-defined data type that allows you to combine data items of different kinds. Structures are used to represent a record. Here's an example:
```c
struct Student {
   char name[50];
   int roll_no;
};
```
In this example, `Student` is a `struct` that has two members: `name` (a string) and `roll_no` (an integer).

**2. Pointer in C**
A pointer is a variable that stores the memory address of another variable. For example:
```c
int var = 50;  
int *p;  
p = &var;  
```
In this example, `var` is a variable and `p` is a pointer. We assign the address of `var` to `p` using `&` (address of) operator.

**3. Arrow Operator in C**
The arrow operator `->` in C is used to access members of a structure or a union using a pointer. For example:
```c
struct demo {
   int x;
};

int main() {
   struct demo *ptr = (struct demo*)malloc(sizeof(struct demo));
   ptr->x = 10;
   printf("%d", ptr->x);
   return 0;
}
```
In this example, `ptr` is a pointer to a structure `demo`. We access the member `x` of `demo` using the arrow operator `->`.

**4. Dot Operator in C**
The dot operator `.` is used to access the members of a structure or a union directly. For example:
```c
struct demo {
   int x;
};

int main() {
   struct demo obj;
   obj.x = 10;
   printf("%d", obj.x);
   return 0;
}
```
In this example, `obj` is an object of structure `demo`. We access the member `x` of `demo` using the dot operator `.`.

**5. Linked List in C**
A linked list is a sequence of data structures, which are connected together via links. Here is a simple example of a linked list:
```c
struct Node {
   int data;
   struct Node *next;
};

int main() {
   struct Node* head = NULL;
   struct Node* second = NULL;
   struct Node* third = NULL;
   
   // allocate 3 nodes in the heap  
   head = (struct Node*)malloc(sizeof(struct Node));
   second = (struct Node*)malloc(sizeof(struct Node));
   third = (struct Node*)malloc(sizeof(struct Node));
   
   head->data = 1; //assign data in first node
   head->next = second; // Link first node with second
   
   second->data = 2; //assign data to second node
   second->next = third;
   
   third->data = 3; //assign data to third node
   third->next = NULL;
   
   return 0;
}
```
In this example, we created a simple linked list with three nodes. Each node has a data part and an address part that points to the next node. The `head` node points to the start of the linked list, and the last element, `third`, points to `NULL`, indicating the end of the list.

Source: Conversation with Bing, 27/2/2024
(1) github.com. https://github.com/pankaj-pundir/templates/tree/4ac06ad3876c2ca890a04c9fbb80efb19350c42f/competitiveCoding%2Falgorithms.cpp.
(2) github.com. https://github.com/BhagwanBende/cpp.assignment/tree/ac7b8c02b91fe0b90f8c7fee7027e4b2b60c899f/linklist%2Flinklist.c.
(3) github.com. https://github.com/shinjasingh/github-upload/tree/e8fdb791f654d360f2bea11b16279578ecd46405/PrintList.cpp.
(4) github.com. https://github.com/akcho/CTCI/tree/f214a390c7dc00c2e9dd83ae04cf90ed07363601/ReturnKthToLast2B.cpp.
