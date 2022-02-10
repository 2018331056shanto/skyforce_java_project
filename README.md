Question Setter
---------------
Name:  __Al Fahad Mollah__         
Registration # __2018331075__            
Session: *2018-2019*            
GitHub Username: *isolated77*               
Cell: *01311721959*              
Email: *iamfahad105@gmail.com*         

Question Set with Answers
=========================
<div align="center"><img src="sust-logo.png" alt="sust-logo" width="100px"></div>
<div style="text-align:center">
  <div align="center">Shahjalal University of Science and Technology
  </div>   
  <div align = "center">Department of Computer Science and Engineering
  </div>  
  <div align = "center"><span> 1<sup>st</sup> Year 1<sup>st</sup> Semester Final Examination &mdash;
  June 2020 (Session 2019-20) </span></div>  
  <br>
  <div align = "center"> Course No. &mdash; <b> CSE 133</b> </div>  
  <div align="center"> Course Title &mdash; <b> Structured Programming Language</b> </div>
  <br>
  <div align = "center">
    Time &mdash; <b> 3 Hours</b>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Credit:<b> 3.00</b>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Total Marks # <b> 100</b>
    </div><br>
    <div align = "center">(Answer all the questions)</div></div>
<div align="center"><h4>Group A</h4></div>
<div style="text-align:left">1. Answer the following Questions in short. (Any <b>Five</b>).</div>
<div align="right">5 &times; 2 = 10 </div>

(a) What is the difference between the functions fabs() and abs()? 

**Answer:** <br>

 Both functions are use to return absotlute value but fabs() use for floating type numbers and abs() is use for integer type numbers.
 Prototype of abs() is under the library header 
 ```cpp
 < stdlib.h >
 ```

  and
  ```cpp
   fabs() 
  ```
   is under 
   ```cpp
   < math.h >

   ```
   .

(b) What is the header file of `tolower()` function?   <br>


**Answer:** <br>

```C
 ctype.h

 ```

( c) What is identifier in C language ?

**Answer:**
```
In C language, an identifier is a combination of alphanumeric characters, i.e. first begin with a letter of the alphabet or an underline, and the remaining are letter of an alphabet, any numeric digit, or the underline.And Identifiers must be unique

For example,
   int student;
   float marks;

```

(d) What does scanf() function return?

**Answer:** <br>
```
The scanf() function returns the number of fields that were successfully converted and assigned. The return value does not include fields that were read but not assigned.
```

(e) What is the difference between scanf and getchar?

**Answer:** The main difference between scanf and getchar is that scanf function helps to read input from the keyboard and to store them according to the given format specifier while getchar reads a single character from the keyboard. 


(f) What is merge sort?
**Answer:** 
```
Merge sort, is a  divide-and-conquer approach for sorting the data. In a sequence of data, adjacent ones are merged and sorted to create bigger sorted lists. 
 These sorted lists are then merged again to form an even bigger sorted list, which continues until you have one single sorted list.
 ```

(g) what are multidimentional arrays?

**Answer:** <br>
```
 Multidimensional arrays make use of multiple indexes to store data.It is useful when storing data that cannot be represented using single dimensional indexing, such as data representation in a board game, tables with data stored in more than one column.
 ```

(h) Why C called a structured programming language?

**Answer:** 
 
 C is called a structured programming language because to solve a large problem, C programming language divides the problem into smaller modules called functions or procedures each of which handles a particular responsibility. 
 The program which solves the entire problem is a collection of such functions
    
<br>

<div align="left">2. Answer the following Questions. (Any <b>Four</b>).</div>
<div align="right">4 &times; 5 = 20 </div>

(a) Why loop in Programming ? What is the difference between while loop and for loop and which is better?
 
**Answer:** 
```
 Almost all the programming languages provide a concept called loop, which helps in executing one or more statements up to a desired number of times.
 All high-level programming languages provide various forms of loops, which can be used to execute one or more statements repeatedly.
 The difference between for loop and while loop is that in for loop the number of iterations to be done is already known and is used to obtain a certain result 
 whereas in while loop the command runs until a certain condition is reached and the statement is proved to be false.
 In general, you should use a for loop when you know how many times the loop should run. If you want the loop to break based on a condition other than the number of times it runs, 
 you should use a while loop.
 ```
 <br>


(b) Write a program to find out the LCM of two positive integer a and b using GCD and find GCD using recursion.
 

**Answer:**<br>
```cpp
#include<stdio.h>
   int hcf(int n1, int n2);
int main() {
    int n1, n2;
    printf("Enter two positive integers: ");
    scanf("%d %d", &n1, &n2);
	int gcd=hcf(n1,n2);
	int lcm=(n1*n2)/gcd;
	
    printf("L.C.M of %d and %d is %d.", n1, n2, lcm);
    return 0;
}

int hcf(int n1, int n2) {
    if (n2 != 0)
        return hcf(n2, n1 % n2);
    else
        return n1;
}
 
```

( c)Write a Program to print following pattern:
Examples : 

Input :` 5 `
Output: 
```
 * * * * *  * * * * *
 * * * *      * * * *
 * * *          * * *
 * *              * *
 *                  *
 *                  *
 * *              * *
 * * *          * * *
 * * * *      * * * *
 * * * * *  * * * * *
 ```
**Answer:**<br>
```cpp
#include<stdio.h>
void pattern(int n)
{
	int i,j;

	for (i=1; i<=n; i++)
	{
		for (j=1; j<=(2*n); j++)
		{
			if (i>(n-j+1))
				printf(" ");
			else
				printf("*");
				
			if ((i+n)>j)
				printf(" ");
			else
				printf("*");
		}
		printf("\n");
	}
	
	for (i=1; i<=n; i++)
	{
		for (j=1; j<=(2*n); j++)
		{
			if (i<j)
				printf(" ");
			else
				printf("*");
			
			if (i<=((2*n)-j))
				printf(" ");
			else
			
				printf("*");
		}
		printf("\n");
	}
}

int main()
{
	pattern(5);
	return 0;
}
```



(d)Differentiate between a constant pointer and pointer to a constant? 

**Answer:**<br>
```Constant pointer:
A constant pointer is a pointer whose value (pointed address) is not modifiable. If you will try to modify the pointer value, you will get the compiler error.

A constant pointer is declared as follows :

Data_Type * const Pointer_Name;
*eg,
int *const ptr; //constant pointer to integer
Pointer to a constant:
In this scenario the value of the pointed address is constant that means we can not change the value of the address that is pointed by the pointer.
A constant pointer is declared as follows :
Data_Type  const*  Pointer_Name;
eg,
int const *ptr// pointer to const integer
```

(e) What do you mean by enumeration in C?

**Answer:** 
```
Enumeration is a user defined datatype in C language. It is used to assign names to the integral constants which makes a program easy to read and maintain.
The keyword “enum” is used to declare an enumeration.
Basically, we used the enum to increase the code readability and with enum easy to debug the code as compared to symbolic constant (macro).
The most important property of enum is that it follows the scope rule and the compiler automatically assigns the value to its member constant. 
```

(f) what is linked list? what is data abstraction?


**Answer:** 
```
Linked-list:
A linked list is a sequence of nodes in which each node is connected to the node following it. This forms a chain-like link for data storage.
Data abstraction :
Data abstraction is a powerful tool for breaking down complex data problems into manageable chunks. This is applied by initially specifying
the data objects involved and the operations to be performed on these data objects without being overly concerned with how the data objects will 
be represented and stored in memory.
```


<div align="left">3. Answer the following Questions. (Any <b>Two</b>).</div>
<div align="right">2 &times; 10 = 20 </div>


(a) Descrive File Handling Functions in C?

**Answer:** <br>
```
The following are the operations performed on files in the c programming language
  a)Creating (or) Opening a file
  b)Reading data from a file
  c)Writing data into a file
  d)Closing a file.
  
  Creating (or) Opening a file:
  
  We use the pre-defined method fopen() to create a new file or to open an existing file. In C programming language, there different modes are available to open a file.They are given below-
    1)r	 Opens a text file in reading mode.
	2)w	 Opens a text file in wirting mode.
	3)a	 Opens a text file in append mode.
	4)r+ Opens a text file in both reading and writing mode.
	5)w+ Opens a text file in both reading and writing mode. It set the cursor position to the begining of the file if it exists.
	6)a+ Opens a text file in both reading and writing mode. The reading operation is performed from begining and writing operation is performed at the end of the file.
	
  Reading from a file:

  The reading from a file operation is performed using the following pre-defined file handling methods.
    1)getc()
    2)getw()
    3)fscanf()
    4)fgets()
    5)fread().
	
  Writing into a file:

  The writing into a file operation is performed using the following pre-defined file handling methods.
   1)putc()
   2)putw()
   3)fprintf()
   4)fputs()
   5)fwrite().
   
  Closing a file:

   Closing a file is performed using a pre-defined method fclose().The method fclose() returns '0'on success of file close otherwise it returns EOF (End Of File).
```

(b)Write a suducode for Tower of hanoi problem then implement it using recursion.

**Answer:** <br>
```
 Suducode for tower of hanoi:-
   
                              FUNCTION MoveTower(disk, source, dest, spare):
  IF disk == 0, THEN:
    move disk from source to dest
  ELSE:
    MoveTower(disk - 1, source, spare, dest)   // Step 1 above
    move disk from source to dest              // Step 2 above
    MoveTower(disk - 1, spare, dest, source)   // Step 3 above
  END IF
```
<br>
  C implementation for tower of hanoi:-
  <br>

```cpp
#include <stdio.h>

 void towers(int, char, char, char); 
 int main()
  {
    int num;
 
    printf("Enter the number of disks : ");
    scanf("%d", &num);
    printf("The sequence of moves involved in the Tower of Hanoi are :\n");
    towers(num, 'A', 'C', 'B');
    return 0;
  }
   void towers(int num, char frompeg, char topeg, char auxpeg)
  {
    if (num == 1)
    {
        printf("\n Move disk 1 from peg %c to peg %c", frompeg, topeg);
        return;
    }
    towers(num - 1, frompeg, auxpeg, topeg);
    printf("\n Move disk %d from peg %c to peg %c", num, frompeg, topeg);
    towers(num - 1, auxpeg, topeg, frompeg);
  }
```

( c)What is the difference between Structure and Union in C Program?Explain in details .
**Answer:**
```
For storage of data of same type C provides concept of Array which stores data variables of same
  type while for storing data of different type C has concept of structure and union that can store
  data variable of different type as well.Both Structure and Union can hold different type of data 
  in them but now on the basis of internal implementation we can find several differences in both of
  these containers.
```
<br>
Differences between Structure and Union are given below:<br>

```
  1)Structure is the container defined in C to store data variables of different type and also supports
   for the user defined variables storage. On other hand Union is also similar kind of container in C
   which can also holds the different type of variables along with the user defined variables.
  2)Structure in C is internally implemented as that there is separate memory location is allotted to
   each input member. While in case Union memory is allocated only to one member having largest size 
   among all other input variables and the same location is being get shared among all of these.
  3)Structure do not have shared location for its members so size of Structure is equal or greater 
   than the sum of size of all the data members.On other hand Union does not have separate location 
   for each of its member so its size or equal to the size of largest member among all data members.
  4)In Structure multiple members can be can be initializing at same time.On other hand in case of
    Union only the first member can get initialize at a time.
  5)Syntax of declare a Structure in C is as follow :
    struct struct_name{
     type element1;
     type element2;
    } variable1, variable2;
	On other syntax of declare a Union in C is as follow:
    union u_name{
     type element1;
     type element2;
    } variable1, variable2;
```

<div align="center"><h4>Group B</h4></div>
<div align="left">1. Answer the following Questions in short. (Any <b>Five</b>).</div>
<div align="right">5 &times; 2 = 10 </div>


(a) what is a graph?

**Answer:** 
A graph is one type of data structure that contains a set of ordered pairs. These ordered pairs are also referred to as edges or arcs and are used to connect nodes where data can be stored and retrieved.

(b)  Describe fmod() function..

**Answer:**<br>

fmod function takes 2 floating-point number a,b as parameter and count the a mod b and returns a double.  
`double fmod (double a, double b);`   
Returns the floating-point remainder of a/b (rounded towards zero):  
fmod = a - rem * b

(c) Which one of the following is a keyword fr and shortly describe its application?   
i) **which**   
ii) **std**      
iii) **volatile**

**Answer:** 
iii) volatile   
By using ``` volatile ``` the program reports the compiler that the value of the variable may change at any time-without any action being implemented by the code the compiler finds nearby.   


(d)
Write could be  the output of this following program:   
```c
int a=8;
printf("%d %d %d\n",++a,a,a++);
``` 
**Answer:** 
`10 10 8`
(e) What is the difference between empty string and null string?

**Answer:** Empty string has a null character ('\0') at index 0.<br>
 But null string does not have any character.
(f) What's the output of this program?
```c
int x = 10, y = -10;
printf("%d", x - (~y) - 1);

```
**Answer:** 0

(g) What is the difference between 
```c 
int (*p) (char *a)
```
<br>

 and

 <br> 

 ```c
 int *p (char *a)
 ```

**Answer:** <br>
In the first one p is a pointer to a function that accepts an argument which is a pointer to a character and returns an integer quantity. On the other hand, in the second one p is a function that accepts an argument which is a pointer to character and returns a pointer to an integer quantity.<br>

(h) What is the difference between 
```c
printf()
```
and
```c
 puts() 
```
**Answer:** <br>
The function 
```c 
printf()
```
 writes the data on standard output device with the ability of formatted string using
 ```c
  %c, %d, %s, %20s
```
 .. etc and printf does not add new line after displaying text.
 ```c
 int printf(const char *format, ...);
 ```
 <br>

 ```c
  puts()
 ```
  writes the string on standard output device and add new line after displaying text.

```c
int puts(const char *s);
```

<div align="left">2. Answer the following Questions. (Any <b>Four</b>).</div>
<div align="right">4 &times; 5 = 20 </div>

(a) Write a program which will print the Pascal's Triangle..

**Answer:** <br>
```cpp
#include <stdio.h>
int main() {
   int row, co = 1, sp, i, j;
   printf("Enter the number of rows: ");
   scanf("%d", &row);
   for (i = 0; i < row; i++) {
      for (sp = 1; sp <= row - i; sp++)
         printf("  ");
      for (j = 0; j <= i; j++) {
         if (j == 0 || i == 0)
            co = 1;
         else
            co = co * (i - j + 1) / j;
         printf("%4d", co);
      }
      printf("\n");
   }
   return 0;
}
```


( b)write a basic algorithm for searching a BST.


**Answer:**

  1. if the tree is empty, then the target is not in the tree, end search
  2. if the tree is not empty, the target is in the tree
  3. check if the target is in the root item
  4. if a target is not in the root item, check if a target is smaller than the root’s value
  5. if a target is smaller than the root’s value, search the left subtree
  6. else, search the right subtree

(c) When is a switch statement can be better than an if statement?

**Answer:**
If you have more than one condition to check on single variable or a single expression, then switch is better than if. In switch statement, program’s execution jumps to the matching value if found. If you use if condition, it checks one by one condition. So it is highly recommended to use switch, if you have to check a variable/condition/expression with multiple values.<br>


```cpp
if( err == 0)
	printf("Error code is 0: reading failed error.\n");
if( err == 1)
	printf ("Error code is 1: writing failed error.\n");
if( err == 2)
	printf("Error code is 2: opening failed error.\n");
if( err == 3)
	printf("Error code is 3: write protected.\n");
```
<br>

Here, errorCode variable is checking with values 0,1,2 and 3. In such case you can use switch

```cpp
switch(err)
{
	case 0:
		printf("Error code is 0: reading failed error.\n");
		break;

	case 1:
		printf ("Error code is 1: writing failed error.\n");
		break;

	case 2:
		printf("Error code is 2: opening failed error.\n");
		break;

	case 3:
		printf("Error code is 3: write protected.\n");
		break;

	default:
		printf("Undefined error.\n");
}

```

(d) Describe malloc, calloc, realloc and free functions with examples.
**Answer:**
<br>

```
malloc function takes a size as a parameter and allocates that memory
to a pointer.
Example: int *p = (int*)malloc(10*sizeof(int));

calloc function takes number of total elements and size of
one element and alocates the needed memory to a pointer. Initialy
all the elements are assigned with the value zero.
Example: int *p = (int*)calloc(10,sizeof(int));

realloc function takes a pointer and a size and re allocates memory
to that pointer and returns that memory to a pointer.
The extra memory is assigned with garbage value.
Example: int *v = (int*)realloc(u,10*sizeof(int));

free function frees the memory allocated to a pointer;
Example: free(p);
```

(e) What do you mean by `pass by value` and `pass by reference?

**Answer:** 
<br>

```cpp
int sum1(int a,int b)
{
    int sum;
    sum = a+b;
    return sum;
}
int sum2(int *a,int *b)
{
    int sum;
    sum = *a+*b;
    return sum;
} 

```  
In the `sum1` function, the arguments of function are taken as value and called_ `pass by value`. In this declaration the function copies the argument values to its varaible and processes on it. In the_ `sum2` function, the argument of function are taken as pointers of memory addresses and it is called_ `pass by reference`. In this type of declaration, the function takes the memory address as argument and then accesses the value inside the address.


(f) What is the output of the following code?
<br>

```cpp
 #include <stdio.h>
        #include <stdlib.h>

        int main() {
            char ***b;
            char a[] = "asdixziojghebbxkqorhytgilokcuf";
            int ab = 69;
            char name[] = "abbas";
            for (int i = 0; i < 25; i++) {
                a[i] = name[i % 5];
            }
            for (int i = 29; i > -1; i--) {
                printf("%c", a[i]);
            }
            puts("");
            return 0;
        }

```

**Answer:**<br>

```
suckosabbasabbasabbasabbasabba
```


<div align="left">3. Answer the following Questions. (Any <b>Two</b>).</div>
<div align="right">2 &times; 10 = 20 </div>


(a) Sort an array using Merge Sort algorithm in ascending order.

**Answer:**
```cpp
#include <stdio.h>
#define f(i, a, b) for(int i=a; i<=b; i++)
#define sz 10

int a[11] = { 100, 145, 59, 526, 56, 313, 333, 1, 426, 894, 0 };
int b[10];

void merging (int low, int mid, int high)
{
    int l1, l2, i;
    for (l1 = low, l2 = mid + 1, i = low; l1 <= mid && l2 <= high; i++)
    {
        if (a[l1] <= a[l2]) b[i] = a[l1++];
        else b[i] = a[l2++];
    }
    while (l1 <= mid) b[i++] = a[l1++];
    while (l2 <= high) b[i++] = a[l2++];
    for (i = low; i <= high; i++) a[i] = b[i];
}

void sort (int low, int high)
{
    int mid;
    if (low < high)
    {
        mid = (low + high) / 2;
        sort (low, mid);
        sort (mid + 1, high);
        merging (low, mid, high);
    }
    else return;
}

int main()
{
    int i;
    printf ("Before sorting: ");
    f (i, 0, sz) printf ("%d ", a[i]);
    puts ("");
    sort (0, sz);
    printf ("After sorting: ");
    f (i, 0, sz) printf ("%d ", a[i]);
}
```

(b) Correct the following code and give appropriate output

```cpp
#include <stdio.h>
        #include <stdlib.h>

        int main() {
            int ****a;

            for (int i = 0; i < 10; i++)
                for (int j = 0; j < 5; j++)
                    if (i < 5) {
                        for (int k = 9; k > -1; k--)
                            if (i * k % 2 == 0) {
                                a[i][j][k][0]++;
                            } else {
                                a[i][j][k][1]++;
                            }
                    } else {
                        for (int k = 20; k > 5; k--)
                            if (j * k % 2 == 0) {
                                a[i][j][k][0]++;
                            } else {
                                a[i][j][k][1]++;
                            }
                    }

            printf("%d ", a[0][1][10][0]);
            return 0;
        }

```


**Answer:**
```cpp
 #include <stdio.h>
        #include <stdlib.h>

        int main() {
            int ****a = malloc(sizeof(int ***) * 10);
            for (int i = 0; i < 10; i++) {
                a[i] = malloc(sizeof(int **) * 5);
                for (int j = 0; j < 5; j++) {
                    a[i][j] = malloc(sizeof(int *) * 21);

                    for (int k = 0; k < 21; k++) {
                        a[i][j][k] = malloc(sizeof(int) * 2);
                        a[i][j][k][0] = 0;
                        a[i][j][k][1] = 0;
                    }
                }
            }

            for (int i = 0; i < 10; i++)
                for (int j = 0; j < 5; j++)
                    if (i < 5) {
                        for (int k = 9; k > -1; k--)
                            if (i * k % 2 == 0) {
                                a[i][j][k][0]++;
                            } else {
                                a[i][j][k][1]++;
                            }
                    } else {
                        for (int k = 20; k > 5; k--)
                            if (j * k % 2 == 0) {
                                a[i][j][k][0]++;
                            } else {
                                a[i][j][k][1]++;
                            }
                    }

            printf("%d ", a[0][1][10][0]);
            return 0;
        }

```

( c) Implement a queue using pointer (Linked List). Write a function <b>Insert</b> to take integer elements and store them in decending order. Also write a print function to print the whole list. Example, take 5, 100, 25, 22, 13 as input using function and print 100 25 22 13 5. <br> 
**Answer:**
```cpp
#include <stdio.h>
#include <stdlib.h>

struct node
{
	int data;
	struct node* link;
};

struct node* head;

void print () {
	struct node* temp = head;

	while (temp != NULL) {
		printf ("%d ", temp -> data);
		temp = temp -> link;
	}
}


void Insert (int value) {
	struct node* temp1 = (struct node*) malloc (sizeof (struct node));

	temp1 -> data = value;

	if (head == NULL || value >= head -> data) {
		temp1 -> link = head;
		head = temp1;
	}
	
	else {
		struct node* pred;
		struct node* p;

		p = head;

		while (p != NULL && p -> data > value) {
			pred = p;
			p = p -> link;
		}

		pred -> link = temp1;
		temp1 -> link = p;
	}
}

int main () {
	head = NULL;
		Insert (5);
	Insert (100);
	Insert (25);
	Insert (22);
	Insert (13);

	print ();
}

```

---

  <div align="center"><h2>END</h2></div>

- [x] I am declaring that, the above work is my own work. Whatever added above
except the template is the result of my brainstorming. I also understand that
submitting work that isn’t my own may result in permanent failure of this course
as well as the whole current semester.
