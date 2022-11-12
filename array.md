## Vectors
Vectors are sequential memory storage structures on your computer.

### Declaring a vector

```c
type_var vector[size];
```

### Accessing values from an array

```C
int vector[10];  //allocating an array of 10 positions [0-9]

vector[0] = 10;  //allocated an integer value in the first position of my array
```

## Example

```C
#include <stdio.h>

int main(){
int size; // reporting the size of the vector;
scanf("%d", &size); // an integer value of size equal to the value entered by the user is being allocated in my memory;
int vector[size];

for(int i = 0; i < size; i++){
  vector[i] = i + 10;
}

//or we can allocate a value to each position this way
for(int i = 0; i < size; i++){
  scanf("%d", &vector[i]);
}

for(int i = 0; i < size; i++){
  printf("%d\n", vector[i]);
} 

return 0;
} 
```
