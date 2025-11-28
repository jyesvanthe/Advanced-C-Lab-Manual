EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include<stdio.h>
struct d
{
    int n;
    char name[90];
};
int main()
{
    struct d s;
    scanf("%d",&s.n);
    scanf("%s",s.name);
    if(s.n>18)
    printf("Age:%d\nName:%svaccine:%d\neligibility:yes",s.n,s.name,s.n);
    else
    printf("Age:%d\nName:%svaccine:%d\neligibility:no",s.n,s.name,s.n);
}
```
Output:

<img width="1252" height="327" alt="image" src="https://github.com/user-attachments/assets/10618efa-6e74-4548-bf5d-f1368e750580" />



Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:
```
#include <stdio.h>
union book {
   int bookno;
char bookname[20];
float price;
} j;
int main()
{
    scanf("%d",&j.bookno);
    printf("Book Number:%d\n",j.bookno);
    scanf("%s",j.bookname);
    printf("Book Name:%s\n",j.bookname);
    scanf("%f",&j.price);
    printf("BooK Price:%.2f\n",j.price);
}
```

Output:


<img width="1023" height="615" alt="image" src="https://github.com/user-attachments/assets/d21ad737-fbb4-477d-9993-9b9db22a7f66" />




Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>

int main() {
    char s[100];  
    FILE *fp;

    scanf("%s", s);
    fp = fopen(s, "w");

    if (fp != NULL) {
        printf("%s File Created Successfully\n%s File Opened\n", s, s);
        fclose(fp);
        printf("%s File Closed\n", s);
    } else {
        printf("Error: Could not create %s\n", s);
    }

    return 0;
}


```
Output:


<img width="1011" height="629" alt="image" src="https://github.com/user-attachments/assets/6b164f5a-d54f-42fd-a795-01c1e95c94e5" />











Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>
struct d
{
    int r;
    char n[100];
    float m;
};
int main()
{
    FILE* fp;
    char c[100];
    scanf("%s",c);
    fp=fopen(c,"w");
    if(fp!=NULL)
    {
        printf("%s Opened\n",c);
    }
    int n;
    scanf("%d",&n);
    struct d t[n];
    while(n!=0)
    {
        scanf("%d %s %f",&t[n].r,t[n].n,&t[n].m);
        fprintf(fp,"%d %s %.2f\n",t[n].r,t[n].n,t[n].m);
        n--;
    }
    printf("Data added Successfully");
    fclose(fp);
}


```
Output:


<img width="1039" height="569" alt="image" src="https://github.com/user-attachments/assets/45c99883-1359-47a9-b825-96729b16cffe" />






Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:
```

#include <stdio.h>
  #include<string.h>
   struct student
   {
       int regno;
       char name[20];
       int no_of_present;
       int jun;
       int july;
       int aug;
       int sep;
       float avg;
       char eligibilty[5];
   };
   int main()
   { 
       struct student stu1;
   scanf("%d%s",&stu1.regno,stu1.name);
   scanf("%d%d%d%d",&stu1.jun,&stu1.july,&stu1.aug,&stu1.sep);
   if(stu1.jun<=21 && stu1.july<=21 && stu1.aug<=21 && stu1.sep<=21)
   {
   stu1.no_of_present=stu1.jun+stu1.july+stu1.aug+stu1.sep;
   stu1.avg=(float)stu1.no_of_present/84 * 100;
   if(stu1.avg>75)
   strcpy(stu1.eligibilty,"yes");
   else
   strcpy(stu1.eligibilty,"no");
   printf("Reg.no:%d\nName:%s\nTotal.No.of.present days:%d\n",stu1.regno,stu1.name,stu1.no_of_present);
   printf("Attendence:%.2f\neligibility:%s",stu1.avg,stu1.eligibilty);
   }
   else
   {
   printf("Invalid data:No.of.present days is greater than working day");
   }
   return 0;
   }


```

Output:


<img width="1010" height="669" alt="image" src="https://github.com/user-attachments/assets/15fec5b9-6ea0-474c-90af-005e775bc94f" />

Result: Thus, the program is verified successfully




Result:
Thus, the program is verified successfully



### module 8 
EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
```
#include<stdio.h> #include<math.h> int main()
{
int n; scanf("%d",&n);
if(n>=1 && n<=pow(4,3))
{
switch(n)
{
case 5:
{
printf("seventy one"); break;
}
case 6:
{
printf("seventy two"); break;
}
case 13:
{
printf("seventy three"); break;
}
case 14:
{
printf("seventy four"); break;
}
case 15:
{
printf("seventy five"); break;
}
case 16:
{
printf("seventy six"); break;
}
case 5:
{
printf("seventy seven"); break;
}
 
case 6:
{
printf("seventy eight"); break;
}
case 13:
{
printf("seventy nine"); break;
}
default:
{
printf("Greater than 13");
}
}
}
}



```
Output:

<img width="574" height="274" alt="image" src="https://github.com/user-attachments/assets/2225d3c0-5303-4ca2-a8b2-142b271a456b" />








Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include<stdio.h> #include<string.h> int main()
{
char a[50]; scanf("%s",a); int l=strlen(a); char h='0';
for(int i=0;i<4;i++)
{
int c=0;
for(int j=0;j<l;j++)
{
if(a[j]==h)
{
c+=1;
}
}
printf("%d ",c); h++;
}
}



```
Output:

<img width="766" height="198" alt="image" src="https://github.com/user-attachments/assets/46c2cd18-e514-4bb8-be97-92cfb7e78d50" />








Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include<stdio.h> #include<string.h> #include<stdlib.h>
int next_per(int n, char **s)
{
for(int i = n - 1 ; i > 0 ; i--) if(strcmp(s[i],s[i-1]) > 0)
{
int j=i+1;
for(;j<n;j++) if (strcmp(s[j],s[i-1])<=0) break; char *t=s[i-1];
s[i-1]=s[j-1];
s[j-1]=t;
for(;i<n-1;i++,n--)
{
t=s[i]; s[i]=s[n-1]; s[n-1]=t;
}
return 1;
}
for(int i=0;i<n-1;i++,n--)
{
char *t=s[i]; s[i]=s[n-1]; s[n-1]=t;
}
return 0;
}
int main()
{
char **s; int n;
scanf("%d",&n); s=calloc(n,sizeof(char*)); for(int i=0;i<n;i++)
{
s[i]=calloc(n,sizeof(char*)*5); scanf("%s",s[i]);
}
do
{
for(int i=0;i<n;i++) printf("%s%c",s[i],i==n-1?'\n':' ');
}
while(next_per(n,s));
 
{
for(int i=0;i<n;i++) free (s[i]);
free(s); return 0;
}
}

```


Output:


<img width="388" height="460" alt="image" src="https://github.com/user-attachments/assets/69065f0d-9bf9-4aa0-9f4b-a416dd94a395" />







Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include<stdio.h> int main()
{
int n,i,j,min; scanf("%d",&n);
int len=n*2-1; for (i=0;i<len;i++)
{
for (j=0;j<len;j++)
{
min=i<j?i:j;
min=min<len-i-1?min:len-1-i; min=min<len-j-1?min:len-1-j; printf("%d ",n-min);
}
printf("\n");
}
return 0;
}

```

Output:


<img width="276" height="284" alt="image" src="https://github.com/user-attachments/assets/c4bb560f-284a-42a6-b7b2-65f0c34adadc" />







Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:
```
#include <stdio.h>
void square();
int main(){
    
    square();
    return 0;
}
void square(){
    int a;
    scanf("%d",&a);
    float ans = a*a;
    printf("The square of %d is : %.2f",a,ans);
}


```

Output:
<img width="1165" height="347" alt="image" src="https://github.com/user-attachments/assets/c2626b14-4618-46af-a930-0c68d8e944ea" />









Result:
Thus, the program is verified successfully

### 9th module 

EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
int stack[40],top,i; void display()
{
for(i=top;i>=0;i--)
{
printf("%d\n",stack[i]);
}
}
```
Output:

<img width="290" height="524" alt="image" src="https://github.com/user-attachments/assets/048af570-3a4b-47c8-8dbc-fe1a409875d7" />



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
int size=3,top=1; float stack[40];
void push (float data)
{
if (top==size-1 )
{
printf("stack is full\n");
}
else
{
top ++; stack[top] = data;
}
}
```

Output:

<img width="538" height="457" alt="image" src="https://github.com/user-attachments/assets/2b5ac387-eb09-4ffc-b9b2-c337fdefd4d5" />




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
int queue[50], rear, front,i; void display()
{
if(front==-1)
{
printf("No elements to display");
}
else
{
for(i=front;i<=rear;i++)
{
printf("%d ",queue[i]);
}
}
}
```

Output:

<img width="589" height="478" alt="image" src="https://github.com/user-attachments/assets/b8cb3eac-2de5-4a2f-835e-b0720fea8bd1" />


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```

int size=4, rear=-1, front=-1; float queue[50];
void enqueue(float data)
{
if(rear<size)
{
if(front==-1)
{
front=0;
}
rear=rear+1; queue[rear]=data;
}
}
```
Output:

<img width="674" height="353" alt="image" src="https://github.com/user-attachments/assets/d8ad28f9-5084-4d3f-a975-d59dc3a02941" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
int front, rear;
void dequeue()
{
    if(front==-1&&rear==-1)
    printf("Queue Underflow.");
    else if(front==rear)
    front=rear=-1;
    else{
        front=front+1;
    }
}
```

Output:

<img width="1154" height="878" alt="image" src="https://github.com/user-attachments/assets/6a1de6cf-40eb-45d7-a59e-4985e3dc390c" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.


### 10 th module 
EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
struct Node{
struct Node *next; char data;
}*head;
void search(char data)
{
struct Node *ptr; char item=data; int i=0,flag;
ptr = head; if(ptr == NULL)
{
printf("Empty List\n");
}
else
{
while (ptr!=NULL)
{
if(ptr->data == item)
{
printf("item %c found at location %d ",item,i+1); flag=0;
}
i++;
ptr = ptr -> next;
}
if(flag!=0)
{
printf("Item not found\n");
}
}

}
```
Output:

<img width="705" height="488" alt="image" src="https://github.com/user-attachments/assets/238cece3-2f8e-43dd-b490-498283c95bd1" />



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```
struct Node{ char data;
struct Node *next;
}*head;

void insert(char data)
{
struct Node n=(struct Node)malloc(sizeof(struct Node)); struct Node *temp;
if(head==NULL)
{
head=n;
n->data=data; n->next=NULL; temp=head; return;
}
while(temp->next!=NULL)
{
temp=temp->next;
}
n->data=data; n->next=NULL; temp->next=n;
}
```
Output:

<img width="467" height="408" alt="image" src="https://github.com/user-attachments/assets/e4554ab2-8fa8-4482-8a86-b5df58da0159" />


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
```
struct Node
{
    struct Node *prev; 
    struct Node *next; 
    int data;
}*head;
void display()
{
    struct Node *temp; 
    temp=head; 
    while(temp!=0)
    {
        printf("%d ",temp->data); 
        temp=temp->next;
        
    }
}
```
Output:
<img width="392" height="458" alt="image" src="https://github.com/user-attachments/assets/ee916f55-78c6-4f86-a2b2-bba15793201e" />


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 

EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;
void insert(float data)
{
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    struct Node *temp;
if(head==NULL)
{
    head=n;
    n->data=data;
    n->next=NULL; 
    n->prev=NULL; 
    temp=head;
}
else
{
    while(temp->next!=NULL)
    {
        temp=temp->next;        
    }
    n->data=data; 
    n->next=NULL; 
    n->prev=temp; 
    temp->next=n;  
}
}
```
Output:

<img width="463" height="630" alt="image" src="https://github.com/user-attachments/assets/893d9915-6169-4f3a-b924-740914a912ee" />


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 






### 11 th module 



EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
int max_of_four(int a,int b,int c,int d)
{
    if(a>b && a>c && a>d)
    {
        return a;  
    }
    else if(b>a && b>c && b>d)
    {
        return b;  
    }
    else if(c>a && c>b && c>d)
    {
        return c;        
    }
    else
    {
        return d;      
    }    
}
int main()
{
    int n1,n2,n3,n4,greater;
    scanf("%d%d%d%d",&n1,&n2,&n3,&n4); 
    greater=max_of_four(n1,n2,n3,n4);
    printf("%d",greater);
}
```
Output:
<img width="256" height="342" alt="image" src="https://github.com/user-attachments/assets/022645a5-2b0e-4ba6-badf-d061b258d8c6" />

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include<stdio.h>
void calculate_the_max(int n,int k)
{
    int a=0,o=0,x=0;
    for(int i=1;i<=n;i++)
    {
        for(int j=1+i;j<=n;j++)
        {
            if((i&j)>a && (i&j)<k)
            {
                a=i&j;              
            }
            if((i|j)>o && (i|j)<k)
            {
                o=i|j;      
            }
            if((i^j)>x && (i^j)<k)
            {
                x=i^j;     
            }   
        }
}
printf("%d\n%d\n%d\n",a,o,x);
}
int main()
{
    int n,k; 
    scanf("%d%d",&n,&k); 
    calculate_the_max(n,k);
}
```
Output:
<img width="240" height="264" alt="image" src="https://github.com/user-attachments/assets/11e3718c-5f4a-42b2-98ac-4c804c8e104b" />


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include<stdio.h> 
int main()
{
    int noshel,noque; 
    scanf("%d%d",&noshel,&noque); 
    int shelarr[noshel][noshel];
    int nobookarr[noshel]; 
    int k=0,c=0;
    for(int i=0;i<noque;i++)
    {
        int queno; 
        scanf("%d",&queno);
        if(queno==1)
        {
            int shelno,nopage;
            scanf("%d%d",&shelno,&nopage);
            shelarr[shelno][k]=nopage; 
            nobookarr[shelno]=c+=1;
            k=k+1;         
        }
        else if(queno==2)
        {
            int pshelno,pbookno;
            scanf("%d%d",&pshelno,&pbookno); 
            printf("%d",shelarr[pshelno][pbookno]);   
        }
        else if(queno==3)
        {
            int ppshelno;
            scanf("%d",&ppshelno); 
            printf("%d",nobookarr[ppshelno]);
        }
    }
}
```
Output:
<img width="235" height="192" alt="image" src="https://github.com/user-attachments/assets/cc2f01a7-9943-4bfc-8506-f47b695c815d" />


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include<stdio.h>
int main()
{
    int n; scanf("%d",&n);
    int a[n];
    int sum=0;
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
        sum=sum+a[i];
        
    }
    printf("%d",sum);
}
```
Output:
<img width="429" height="213" alt="image" src="https://github.com/user-attachments/assets/19ffbb74-8d65-41a2-9ead-dc8cc088ea10" />

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    fgets(str,sizeof(str),stdin);
    int len=sizeof(str);
    int count=1;
     for(int i=0;i<len-1;i++){
         if(str[i]==' ')
         count++;
         
     }
     printf("Total number of words in the string is :%d",count);
    return 0;
}
```
Output:
<img width="1156" height="206" alt="image" src="https://github.com/user-attachments/assets/a188f03c-6dc5-4700-aaf0-1c4244808b7f" />




Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.

### 12 th module 



EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
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
```
struct Node
{
    int data;
    struct Node *next;
}*head;
void display()
{
    struct Node *p; 
    p=head;
    while(p!=NULL)
    {
        printf("%d\n",p->data);
        p=p->next;
        
    }
}
```
Output:

<img width="261" height="332" alt="image" src="https://github.com/user-attachments/assets/f982dc0c-3e99-44ac-be34-305591b20786" />



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
struct Node
{
    int data;
    struct Node *next;
}*head; 
void pop()
{
    if(head==NULL)
    {
        printf("stack is empty");        
    }
    else
    {
        head=head->next;    
    }
}
```
Output:

<img width="801" height="557" alt="image" src="https://github.com/user-attachments/assets/9399a1ba-65a7-4fcb-ac3a-b0c3509f9ec6" />



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
struct Node
{
    char data;
    struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    if(front==NULL)
    {
        printf("queue is empty");        
    }
    else
    {
        printf("queue elements:\n");
        while(front!=NULL)
        {
            printf("%c\n",front->data);
            front=front->next;      
        }   
    }
}
```
Output:

<img width="494" height="526" alt="image" src="https://github.com/user-attachments/assets/3bfb7b43-ad2d-4e5e-98dc-51b9caf997b4" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

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
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
   struct Node *p=(struct Node*)malloc(sizeof(struct Node));
   p->data=data;
   p->next=NULL;
   if(front==NULL)
   {
       front=rear=p;   
   }
   else
   {
       rear->next=p; 
       rear=p;  
   }
}
```
Output:

<img width="504" height="526" alt="image" src="https://github.com/user-attachments/assets/71a6bf5c-6681-4331-81ad-0686147f7064" />

Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%c",front->data);
}
```
Output:

<img width="1158" height="812" alt="image" src="https://github.com/user-attachments/assets/ebb6e730-f4c3-4f73-838a-0486d0d9e75d" />




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.

























