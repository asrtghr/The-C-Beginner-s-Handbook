## What are Variables?

A **variable** is a memory location that can be identified by a name. 

These variables can have their contents (values) changed during the program through **assignment commands.**

### Declaration and Initialization of Variables

When using variables in **C**, it is always necessary to **declare their type** *- we will see the types of variables in more detail in the topic below-* before they are used in your program.

The purpose of indicating the type of variable for our compiler (virtual machine) to interpret the code is due to the fact that in **C** we are working directly with the allocation of a physical memory space present on the machine in question.

In this way, when we indicate the type of variable that we are going to work with, our machine will allocate a space of a specific size so that this variable **(access key)** can have a value.

```C
#include <stdio.h> //C build library import

int main(void){
	int age; // inline declaration of an integer variable
	int bday = 2000; // inline declaration of an integer variable

	return 0;
}
```

### Constants
When creating an extensive algorithm, we may notice over time that certain values end up being repeated numerous times throughout the code.

In this way, we can use **constants** as a form of control and better understanding of something that will always appear.

To declare constant values in **C**, we will use the `#define` command.

**Remember: Constants cannot have their values changed!**

```C
#define WEEK_DAYS 7  
#define HOURS_DAY 24  

int main (void)  {  
   int time;  
  
    time = 10 * WEEK_DAYS * HOURS_DAY;  
}
```
---

## C Variables

| C Variables | Keyword | Formatting| Memory Size |
|      ---         |      ---      |   :---:   | :------    |
| **Integer**          |      `int`      |     `%d`    | **4 bits**| 
| **Long Integer**    |      `long int`      |     `%li`    | **8 bits** |
| **Float**    |      `float`      |     `%f`    | **4 bits** | 
| **Double**    |      `double`      |     `%lf`    | **8 bits** |  
| **Long Double**    |      `long double`      |     `%lf`    | **16 bits** |  
| **Unsigned Int**    |      `unsigned int`      |     `%Lf`    | **4 bits** | 
| **Char**    |      `char`      |     `%c`    | **1 bit** |  
| **String**    |      `char*`      |     `%s`    | **4 bits** |  























