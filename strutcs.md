## Structs

**Structs**, also known as Records, define data types that group variables under the same data type. The idea of ​​using a **struct** is to allow, when storing the data of the same entity, this can be done with a single variable.

For example, if you need to store a person's height, weight and age, you can create a struct called Person and group the data into a single data type, as shown in the following example.

**The data grouped in a struct is called fields.**

```C
struct person{
  float weight; // define the Weight field
  int age; // define the Age field
  float height; // define the Height field
}
```

After creating the type, it is possible to declare variables of type **person**, like this:

```C
struct person P1;
//To access the fields of a struct, use the syntax  VariableName.FieldName

P1.age = 15;
P1.weight = 60.5;
P1.height = 1.75;
```

### Passing Structs by Parameter
To pass a struct by value, just declare it as one of the parameters.

```C
#include <stdio.h>

struct person{
  float weight; // define the Weight field
  int age; // define the Age field
  float height; // define the Height field
}

typedef struct person person_t;
//creating a keyword as a reference to the struct

void printPerson(person_t person);

int main(){
  person_t joao

  João.age = 15;
  John.weight = 60.5;
  John.height = 1.75;

  printPerson(John);
  return 0;
}
void printPerson(person_t P){
  printf("Age: %d  Weight: %f Height: %f\n", P.age, P.weight, P.height);
}
```

### Return of Structs in Functions
Since a struct defines a data type, that type can be returned in a function, just like any other data type.

```C
#include <stdio.h>

struct person{
  float weight; // define the Weight field
  int age; // define the Age field
  float height; // define the Height field
}

typedef struct person person_t;
//creating a keyword as a reference to the struct

person_t setPerson(int age, float weight, float height);
void PrintPerson(person_t P);

int main(){
  Person John;

  John = setPessoa(15,60.5,1.75);
  // assign the function return to a struct variable

  printPerson(John);
  return 0;
}
 
person_t setPerson(int age, float weight, float height);{
  person_t P;
  P.age = age;
  P.weight = weight;
  P.height = height;
  return P;
}

void printPerson(person_t P){
  printf("Age: %d  Weight: %f Height: %f\n", P.age, P.weight, P.height);
}
```
