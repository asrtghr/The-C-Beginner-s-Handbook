## Repetition Structures

**Repeating structures are used in all programming languages ​​in order to repeat blocks of code in order to streamline the algorithm.**

* **For:** Repetition at a given interval
* **While:** Repetition until a condition breaks
* **Do / While:** Repeat until a condition breaks

### For Repetition Structure

```C
int number;
//start ; condition; increment
for (int i = 0; i < 10; i++){
  scanf("%d", &number);
  printf("%s %d", "The number entered was: ", number);
}

```

### While Loop Structure

```C
int number;

while(number >= 0){ //Loop condition
  scanf("%d", &number);
  printf("The number is greater than or equal to 0");
  printf("You have entered a negative number");
}

Conditional checking is done before entering the looping structure.
```
## Do / While Repetition Structure

```C
int number;

do{
  scanf("%d", &number);
  printf("The number is greater than or equal to 0");
  
}while(number >= 0) //Loop condition

printf("You have entered a negative number");

The conditional check is done after entering the repeating structure, the structure being executed without the initial check.
```
