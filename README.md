# C Programming – Learning Progress

## About

This repository contains my C Programming learning journey, including programming fundamentals, problem solving, functions, arrays, strings, pointers, and Embedded C-oriented concepts.

---

# C Programming Learning Workflow

C Basics
↓
Variables & Data Types
↓
Operators
↓
Input / Output
↓
if / else
↓
switch
↓
Loops
↓
Type Casting
↓
Scope & Lifetime
↓
Functions
↓
Arrays
↓
Strings
↓
Pointers

---

# 1. Variables & Data Types

## Concept

A variable is a named memory location used to store data.

Common data types:

int → Integer values
float → Decimal values
double → Higher precision decimal values
char → Single character

## Syntax

int age = 20;
float voltage = 230.5;
double value = 123.456;
char grade = 'A';

## Workflow

Declare Variable
↓
Assign Value
↓
Process Value
↓
Display Result

---

# 2. Operators

Operators are symbols used to perform operations on data.

## Types of Operators

Arithmetic
Relational
Logical
Assignment
Increment / Decrement
Bitwise
Conditional / Ternary
sizeof

## Arithmetic Operators

+  -  *  /  %

Example:

int power = voltage * current;

## Relational Operators

>  <  >=  <=  ==  !=

Example:

if(temperature > 35)

## Logical Operators

&&  ||  !

Example:

if(temperature > 35 && current > 10)

## Assignment Operators

=  +=  -=  *=  /=

Example:

alarm += 1;

## Increment / Decrement

i++;
i--;

## Bitwise Operators

&  |  ^  ~  <<  >>

Example:

registerValue |= (1 << 2);

## Conditional / Ternary Operator

condition ? value1 : value2;

Example:

status = (warning == 1) ? "WARNING" : "NORMAL";

## sizeof Operator

sizeof(int)

Used to find the memory size occupied by a data type or variable.

---

# 3. Input / Output

## Output

printf("Hello");

## Input

scanf("%d", &number);

## Common Format Specifiers

%d  → Integer
%f  → Float
%c  → Character
%s  → String
%p  → Memory Address
%zu → sizeof result

## Workflow

User Input
↓
Store in Variable
↓
Process
↓
printf()
↓
Output

---

# 4. if / else

## Concept

if / else is used for decision making.

## Syntax

if(condition)
{
    // statements
}
else
{
    // statements
}

## Example

if(waterLevel < 10)
{
    printf("LOW WATER");
}
else
{
    printf("NORMAL");
}

## Workflow

Condition
↓
TRUE → if block
↓
FALSE → else block

---

# 5. switch

## Concept

switch is used when one variable needs to be compared with multiple fixed cases.

## Syntax

switch(value)
{
    case 1:
        // statements
        break;

    case 2:
        // statements
        break;

    default:
        // statements
}

## Example

int mode = 2;

switch(mode)
{
    case 1:
        printf("Pump OFF");
        break;

    case 2:
        printf("Pump ON");
        break;

    case 3:
        printf("Pump AUTO");
        break;

    default:
        printf("Invalid Mode");
}

## Workflow

Value
↓
switch
↓
Match Case
↓
Execute
↓
break

---

# 6. Loops

Loops are used to repeat a block of code.

## for Loop

### Syntax

for(initialization; condition; update)
{
    // statements
}

### Example

for(int i = 1; i <= 5; i++)
{
    printf("%d\n", i);
}

### Workflow

Initialization
↓
Condition
↓
TRUE → Execute
↓
Update
↓
Condition
↓
FALSE → Stop

---

# while Loop

## Syntax

while(condition)
{
    // statements
}

## Example

int i = 1;

while(i <= 5)
{
    printf("%d\n", i);
    i++;
}

---

# do-while Loop

## Syntax

do
{
    // statements
}
while(condition);

## Concept

do-while executes the block at least once before checking the condition.

---

# 7. Type Casting

## Concept

Type casting means converting one data type into another data type.

## Syntax

(new_type)value;

## Example

int a = 10;
int b = 3;

float result = (float)a / b;

printf("%.2f", result);

Without casting:

10 / 3 → Integer Division

With casting:

(float)10 / 3 → Decimal Result

## Workflow

Original Data Type
↓
Type Casting
↓
Converted Data Type
↓
Operation
↓
Result

---

# 8. Scope & Lifetime

## Scope

Scope means where a variable can be accessed.

## Example

int x = 10;

if(x > 5)
{
    int y = 20;

    printf("%d", x);
    printf("%d", y);
}

printf("%d", x);

Here:

x → Accessible inside and outside the block
y → Accessible only inside the if block

## Function Scope Example

void sensor()
{
    int temperature = 30;

    printf("%d", temperature);
}

temperature is local to the sensor() function.

## Workflow

Variable Declaration
↓
Scope decides where it can be accessed
↓
Lifetime decides how long it exists

---

# 9. Functions

## Concept

A function is a reusable block of code.

Function → Reusable Code
Parameter → Input to Function
Return → Output from Function
Call by Value → Copy of value is passed
Pointer + Function → Address is passed
Recursion → Function calls itself

## Syntax

return_type function_name(parameters)
{
    // statements
}

## Example

int add(int a, int b)
{
    return a + b;
}

Calling the function:

int result = add(10, 20);

## Workflow

Function Declaration
↓
Function Definition
↓
Function Call
↓
Parameters
↓
Processing
↓
Return Value

## Function Learning Order

Function Basics
↓
Parameters & Return
↓
Call by Value
↓
Pointers + Functions
↓
Arrays + Functions
↓
Recursion

---

# 10. Arrays

## Concept

An array is a collection of multiple values of the same data type.

## Syntax

int numbers[5];

## Initialization

int numbers[5] = {10, 20, 30, 40, 50};

## Access

numbers[0]
numbers[1]
numbers[2]

## Example

for(int i = 0; i < 5; i++)
{
    printf("%d\n", numbers[i]);
}

## Workflow

Array Declaration
↓
Store Multiple Values
↓
Index
↓
Loop
↓
Access / Process
↓
Output

## Common Array Problems

Largest
Smallest
Second Largest
Reverse
Sum
Average
Search
Sort
Frequency

---

# 11. Strings

## Concept

In C, a string is a character array terminated by the null character '\0'.

## Example

char name[] = "SRI";

Memory:

S | R | I | \0

## Character vs String

char ch = 'A';

char name[] = "SRI";

%c → Character
%s → String

## String Input

scanf("%s", name);

For a full line including spaces:

fgets(name, sizeof(name), stdin);

## Important String Functions

strlen() → Find length
strcpy() → Copy string
strcat() → Join strings
strcmp() → Compare strings

Header:

#include <string.h>

## String Workflow

String Input
↓
Character Array
↓
'\0' indicates String End
↓
Loop Through Characters
↓
Process
↓
Output

## String Practice

Reverse
Palindrome
Vowel Count
Character Count
String Compare
String Copy
String Concatenation

---

# 12. Pointers

## Concept

A pointer is a variable that stores the memory address of another variable.

## Basic Example

int x = 10;
int *p = &x;

## Core Concept

&x → Address of x
p  → Stores address of x
*p → Value stored at that address

## Pointer Declaration

data_type *pointer_name;

Examples:

int *p;
float *q;
char *r;

## Address Operator

&x

Used to get the memory address of x.

## Dereference Operator

*p

Used to access the value stored at the address held by p.

## Pointee Variable

int temperature = 30;
int *ptr = &temperature;

ptr → Pointer
temperature → Pointee Variable

---

# 13. Pointer + Variables

## Read Value

int x = 10;
int *p = &x;

printf("%d", *p);

Output:

10

## Modify Value

*p = 50;

Now:

x = 50

## Workflow

Variable
↓
Address &
↓
Pointer
↓
Dereference *
↓
Read / Modify Value

---

# 14. Pointer Arithmetic

Pointer arithmetic is mainly used with arrays.

## Operators

p++
p--
p + n
p - n

## Example

int arr[] = {10, 20, 30, 40};

int *p = arr;

printf("%d", *p);

p++;

printf("%d", *p);

Output:

10
20

## Meaning

p → Current Element
p++ → Next Element
p-- → Previous Element
p+n → Move n Elements Forward
p-n → Move n Elements Backward

---

# 15. Pointer + Arrays

## Example

int arr[] = {10, 20, 30, 40};

int *p = arr;

The array name represents the address of its first element in this context.

## Access Using Pointer

*(p + 0) → 10
*(p + 1) → 20
*(p + 2) → 30
*(p + 3) → 40

## Example

for(int i = 0; i < 4; i++)
{
    printf("%d ", *(p + i));
}

Output:

10 20 30 40

## Workflow

Array
↓
First Element Address
↓
Pointer
↓
Pointer Arithmetic
↓
*(p + i)
↓
Array Values

---

# 16. Pointer + Functions

## Concept

A pointer can be used to pass the address of a variable to a function, allowing the function to modify the original object.

## Example

void update(int *p)
{
    *p = 100;
}

int x = 50;

update(&x);

Now:

x = 100

## Workflow

Original Variable
↓
&x
↓
Function Receives Address
↓
*p
↓
Modify Original Value

Note:

C is technically a pass-by-value language. In this case, the value being passed is an address, allowing the function to modify the object at that address.

---

# 17. Pointer to Pointer

## Concept

A pointer to pointer stores the address of another pointer.

## Example

int x = 10;

int *p = &x;

int **q = &p;

## Workflow

q
↓
p
↓
x
↓
10

*p → Value of x
**q → Value of x

---

# 18. Pointer + Strings

## Example

char name[] = "SRI";

char *p = name;

## Access Character

printf("%c", *p);

Output:

S

## Move Pointer

p++;

Now:

*p → R

## String Traversal

while(*p != '\0')
{
    printf("%c", *p);
    p++;
}

Output:

SRI

## Workflow

String
↓
First Character Address
↓
char *
↓
*p
↓
p++
↓
Next Character

---

# 19. Pointer + Structures

## Structure

struct Sensor
{
    int temperature;
    int voltage;
};

## Structure Variable

struct Sensor s = {30, 230};

## Structure Pointer

struct Sensor *p = &s;

## Normal Access

s.temperature

## Pointer Access

p->temperature

## Important

p->temperature

is equivalent to:

(*p).temperature

## Workflow

Structure
↓
Structure Variable
↓
Address &
↓
Structure Pointer
↓
-> Operator
↓
Access Member

---

# 20. NULL Pointer

## Concept

A NULL pointer does not currently point to a valid object.

## Syntax

int *p = NULL;

## Check

if(p != NULL)
{
    printf("%d", *p);
}

Never dereference a NULL pointer.

## Workflow

Pointer
↓
NULL
↓
Check
↓
If Valid → Dereference
↓
If NULL → Do Not Dereference

---

# 21. Dynamic Memory

Dynamic memory is used to allocate memory at runtime.

Header:

#include <stdlib.h>

## malloc()

int *p = malloc(5 * sizeof(int));

Allocates memory for 5 integers.

malloc() does not initialize the allocated memory.

## calloc()

int *p = calloc(5, sizeof(int));

Allocates memory for 5 integers and zero-initializes the allocated bytes.

## realloc()

p = realloc(p, 10 * sizeof(int));

Changes the size of an existing allocation.

In robust programs, use a temporary pointer when calling realloc() so that allocation failure does not lose the original pointer.

## free()

free(p);
p = NULL;

Releases dynamically allocated memory.

## Workflow

malloc()
↓
Use Memory
↓
realloc() if required
↓
free()
↓
p = NULL

---

# 22. Function Pointer

## Concept

A function pointer stores the address of a function.

## Example

int add(int a, int b)
{
    return a + b;
}

int (*p)(int, int) = add;

printf("%d", p(10, 20));

Output:

30

## Workflow

Function
↓
Function Address
↓
Function Pointer
↓
Call Function

## Applications

Callbacks
Drivers
Menus
Embedded Systems

---

# 23. Void Pointer

## Concept

A void pointer can store the address of an object of any object type.

## Syntax

void *p;

## Example

int x = 10;

void *p = &x;

printf("%d", *(int *)p);

A void pointer must be converted to the appropriate pointer type before dereferencing.

---

# 24. Wild Pointer

## Concept

A wild pointer is an uninitialized pointer that does not have a known valid address.

## Example

int *p;

Dangerous:

*p = 10;

## Better

int *p = NULL;

---

# 25. Dangling Pointer

## Concept

A dangling pointer points to memory whose lifetime has ended.

## Example

int *p = malloc(sizeof(int));

*p = 10;

free(p);

After free(), p should not be dereferenced.

## Better

free(p);
p = NULL;

---

# 26. const + Pointer

There are three important forms.

## 1. Pointer to const

const int *p = &x;

The value cannot be modified through p.

*p = 20;   // Not allowed

But the pointer can point somewhere else.

p = &y;    // Allowed

---

## 2. Const Pointer

int *const p = &x;

The pointer cannot point somewhere else.

p = &y;    // Not allowed

But the value can be modified.

*p = 20;   // Allowed

---

## 3. Const Pointer to Const

const int *const p = &x;

The pointer cannot be changed and the value cannot be changed through p.

*p = 20;   // Not allowed
p = &y;    // Not allowed

## Easy Way to Remember

const int *p
→ Value protected

int *const p
→ Pointer protected

const int *const p
→ Value + Pointer protected

---

# POINTERS – COMPLETE ROADMAP

POINTERS
│
├── Basics
│   ├── &
│   ├── *
│   ├── Declaration
│   └── Pointee
│
├── Variables
│   ├── Read
│   └── Modify
│
├── Arithmetic
│   ├── ++
│   ├── --
│   ├── +n
│   └── -n
│
├── Arrays
│
├── Functions
│
├── Pointer to Pointer
│
├── Strings
│
├── Structures
│   └── -> Operator
│
├── NULL Pointer
│
├── Dynamic Memory
│   ├── malloc()
│   ├── calloc()
│   ├── realloc()
│   └── free()
│
├── Function Pointer
│
├── Void Pointer
│
├── Wild Pointer
│
├── Dangling Pointer
│
└── const + Pointer

---

# C Programming Practice Workflow

For every topic:

Learn Concept
↓
Understand Syntax
↓
Write Small Program
↓
Understand Code Line by Line
↓
Modify the Code
↓
Solve Practice Problems
↓
Debug Errors
↓
Commit Code to GitHub

---

# Repository Structure

c-programming/
│
├── README.md
│
├── 01-basics/
│
├── 02-operators/
│
├── 03-control-statements/
│
├── 04-loops/
│
├── 05-type-casting/
│
├── 06-scope-lifetime/
│
├── 07-functions/
│
├── 08-arrays/
│
├── 09-strings/
│
└── 10-pointers/

---

# Current Learning Progress

Variables & Data Types → Completed
Operators → Completed
Input / Output → Completed
if / else → Completed
switch → Completed
Loops → Completed
Type Casting → Completed
Scope & Lifetime → Completed
Functions → Completed
Arrays → Completed
Strings → Completed
Pointers → In Progress

---

# Goal

The main goal of this repository is to build strong C Programming fundamentals for:

- Embedded Systems
- Firmware Development
- Microcontroller Programming
- RTOS Development
- Open Source Contributions
- GSoC Preparation

---

# Next Learning Focus

Pointers
↓
Structures
↓
Dynamic Memory
↓
Bitwise Programming
↓
const / static / volatile
↓
Embedded C
↓
Git & Open Source
↓
Zephyr RTOS
