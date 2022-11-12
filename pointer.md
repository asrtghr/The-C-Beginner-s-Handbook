## Pointers

A pointer is a variable capable of storing a memory address or the address of another variable.

```C
#include <stdio.h>
int main(){
  int a;
  int b;
  int c;
  int *ptr;
 
  a = 90;
  b = 2;
  c=3;
  ptr = &a;
  printf("Value of ptr: %p, Content of ptr: %d\n", ptr, *ptr);
  printf("B: %d, C: %d\n",b, c);
  return 0;
}
```

### Printing Pointers
In **C**, you can print the value stored in the pointer (an address), using the `printf` function with the formatter `%p` in the format string. For example:

```C
#include <stdio.h>
int main() {
  int x;
  int *ptr;
  ptr = &x;
  printf("The address of X is: %p\n", ptr);
  return 0;
}
```

### Accessing the Contents of a Memory Location through a Pointer

To access the contents of a memory location, whose address is stored in a pointer, the dereference operator `*` is used.

```C
#include <stdio.h>
int main(){
  int x;
  int *ptr;
  x = 5;
  ptr = &x; printf("The value of the X variable is: %d\n", *ptr);
  // dereferencing a pointer
  *ptr = 10; // using dereference on the "left side" of an assignment
  printf("Now, X is valid: %d\n", *ptr);
  return 0;
}
```

### Dynamic Memory Allocation

During the execution of a program, memory can be dynamically allocated to use as program variables.

**In C, the allocation is done with the ` malloc`  function (and, to free up memory, the `free` function is used).**

```C
#include <stdlib.h>
#include <stdio.h>
  
int main(){
  int *ptr_a;
  // create the required area for 01 integer and
  ptr_a = (int *)malloc(sizeof(int));

  printf("Address of ptr_a: %p\n",  ptr_a);
  *ptr_a = 90;
  printf("Content of ptr_a: %d\n", *ptr_a); // print 90
  free(ptr_a); // Release the allocated area
return 0;
}
```

### Vector Allocation
However, it is more common to use pointers for vector allocation. To do so, just specify the size of this vector at the time of allocation.

```C
#include <stdlib.h>

int main(){
  int i;
  int *v;
  v = (int*)malloc(10*sizeof(int));
  // 'v' is a pointer to an area that has 10 integers.
  // 'v' works just like a vector  v[0] = 10;
  v[1] = 11;
  v[2] = 12;
  // to be continued...
  v[9] = 19;

  for(i = 0; i < 10; i++)
  printf("v[%d]: %d\n", i, v[i]); printf("Address of 'v': %p", v);
  // print the address of the allocated area for 'v'
  free(v);
  return 0;
}
```

### Pointer Arithmetic

In addition to accessing the data of a dynamically allocated area as if it were a vector, it is possible to access them through the pointer itself, using the technique called pointer arithmetic.

```C
#include <stdlib.h>

int main(){
  int *vet;
  int *ptr;

  v = (int*)malloc(10*sizeof(int));
  vet[4] = 44;
  ptr = vet;
  // 'ptr'  points to the beginning of vet
  *ptr = 11; // vet[0] = 11
  ptr++; // advances the pointer
  *ptr = 12; // vet[1] = 12
  printf("%p\n",  ptr);
  printf("%d\n", *ptr);
  // free(ptr); // Releasing 'ptr' directly causes NULL POINTER ASSIGNMENT
  // Correcting, the correct form is:
  ptr--;
  free(ptr);
  return 0;
}
```
