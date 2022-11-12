## Arrays
We can build matrices in **C** using vectors.

### Declaration of an Array

```C
int array[row][column];
```

### Accessing Array Values

```C
int array[2][2] //allocating a quadratic array of order 2

array[0][0] = 10;
//allocating the integer value equal to 10 in the first row and column of the matrix
```

### Example

```C
#include <stdio.h>
#define LINE 2
#define COLUMN 2

int main(){
  int array[ROW][COLUMN];

for(int i = 0; i < LINE; i++){
    for(int j = 0; j < COLUMN; j++){
      scanf("%d", &(matrix[i][j]));  //allocating values in the array
    }
  }

  //showing array values
  for(int i = 0; i < LINE; i++){
    for(int j = 0; j < COLUMN; j++){
      printf("%s %d\n", "MATRIX VALUE: ", matrix[i][j]);
    }
  }
  return 0;
}
