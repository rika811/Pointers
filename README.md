# Pointers

## What is Pointer in C?

The Pointer in C, is a variable that stores address of another variable. A pointer can also be used to refer to another pointer function. A pointer can be incremented/decremented, i.e., to point to the next/ previous memory location. The purpose of pointer is to save memory space and achieve faster execution time.

### Declaring a Pointer
Like variables, pointers in C programming have to be declared before they can be used in your program. Pointers can be named anything you want as long as they obey C’s naming rules. A pointer declaration has the following form.

```
data_type * pointer_variable_name;
```

Here,

+ data_type is the pointer’s base type of C’s variable types and indicates the type of the variable that the pointer points to.
+ The asterisk (*: the same asterisk used for multiplication) which is indirection operator, declares a pointer.

### Initialize a pointer

After declaring a pointer, we initialize it like standard variables with a variable address. If pointers in C programming are not uninitialized and used in the program, the results are unpredictable and potentially disastrous.

To get the address of a variable, we use the ampersand (&)operator, placed before the name of a variable whose address we need. Pointer initialization is done with the following syntax.

**Pointer Syntax**

```
pointer = &variable;
```
## Types of Pointers in C

Following are the different Types of Pointers in C:

**Null Pointer**

We can create a null pointer by assigning null value during the pointer declaration. This method is useful when you do not have any address assigned to the pointer. A null pointer always contains value 0.

Following program illustrates the use of a void pointer:

```
#include <stdio.h>
int main()
{
void *p = NULL; 	//void pointer
printf("The size of pointer is:%d\n",sizeof(p));
return 0;
}
```

Output:

```
The value inside variable p is:
0
```


**Void Pointer**

In C programming, a void pointer is also called as a generic pointer. It does not have any standard data type. A void pointer is created by using the keyword void. It can be used to store an address of any variable.

```
Following program illustrates the use of wild pointer:

#include <stdio.h>
int main()
{
int *p; 	//wild pointer
printf("\n%d",*p);
return 0;
}
```
Output:

```
The size of pointer is:4
```

**Wild pointer**

A pointer is said to be a wild pointer if it is not being initialized to anything. These types of C pointers are not efficient because they may point to some unknown memory location which may cause problems in our program and it may lead to crashing of the program. One should always be careful while working with wild pointers.

Following program illustrates the use of wild pointer:

```
#include <stdio.h>
int main()
{
int *p; 	//wild pointer
printf("\n%d",*p);
return 0;
}
```

Output:

```
timeout: the monitored command dumped core
sh: line 1: 95298 Segmentation fault      timeout 10s main
```

Output for the attached code-

![Screenshot 2023-04-11 at 2 39 59 AM](https://user-images.githubusercontent.com/91966167/230999502-e000eefe-509f-43c5-b31a-a26b40c89828.png)


