## Recursion

Recursion **is the programming mechanism in which a definition of a function or another object refers to the object itself being defined**. So a recursive function is a function that is defined in terms of itself.

**Base case:** is the simplest case. A condition is used where the problem is easily resolved.

**Recursive calls:** seek to simplify the problem in such a way that they converge to the base case.

### Example

```C
#include <stdio.h>

int factorial(int number);

int main(){
  int number;

  printf("%s", "Choose a number to see the factorial: ");
  scanf("%d", &number);

  printf("%d\n", factorial(number));
  return 0;
}

int factorial(int number){
  if(number == 0)
  return 1;
  else{
  return number * factorial(number-1);
}
```
