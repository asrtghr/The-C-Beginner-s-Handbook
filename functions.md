## Functions
As we program long lines of code, there will come times when you'll notice that there are certain snippets that end up repeating themselves.

That way, using functions we can **modulate** our code making it better to perform a *debug* when fixing errors.

As well as we can make it more and more optimized with small snippets of code with low execution time and that perform simple and local tasks.

### Definition of a Function

```C
type function_name(parameters){
  code
}
``

### Example

```C
//I can perform a sum function in different ways
int sum(int a, int b) {
  return(a+b);
}

int sum(int a, int b) {
  int sum = a + b;
  return sum;
}

void sum(int a, int b) {
  int sum = a + b;
  printf("%d", sum);
}
```

Note that when using functions of type `void` there will be no `return` of a variable of the same type as the declared function.

Therefore, when we declare a function other than `void`, we define it as a **return** function. That is, it will return something to the main code.

```C
#include <stdio.h>

int sum(int a, int b);
// always declare the scope of your function above main

int main(){
  int a, b, c;
  
  c = sum(a,b);
  printf("%d", c);
  
  return 0;
}

int sum(int a, int b) {
  return(int)(a+b); //performing a casting for int formality only
}
