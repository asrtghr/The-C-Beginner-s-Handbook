## Condition Structures

Condition structures become extremely useful tools in many programming languages ​​because of the possibility of directing your program to desired actions according to the obtained values.

**In the use of decision structures it is necessary to know and use the relational operators involved, namely:**

### Relational Operators

| Operation | Operator | 
| :--- | :---: |
| **Greater Than** | `>` | 
| **Less  Than** | `<` |
| **Greater Than or Equal To** | `>=` | 
| **Less Than or Equal To** | `<=` |
| **Equal To** | `==` |
| **Not Equal To** | `!=` | 

```C
int a = 10;
int b = 20;

a <= (b/2);	  // True                       

a < 5;        // False               	

a < b;       // True

```

### Logical Operators

| Operation | Operator | 
| :--- | :---: |
| **and** | `&&` | 
| **or** | `||` |
| **not** | `!` | 

---

### **Simple Conditionals**

For this case we will only have a single condition to be tested.
```C
if(age > 18)
printf("%s", "You are a minor!");
```

### **Compound Conditionals**
For this case we will have a second condition that will activate if the first one is false.
```C
if(age > 18)
  printf("%s", "You are a minor!");
else
  printf("%s", "You are of legal age")
```

### **Chained Conditionals**

In this case we will have a chain of conditionals for testing your program.
```C
if(age > 18)
  printf("You are a minor!");
else if(age > 18 || age < 25)
  printf("%s", "You are in the young age group");
else
  printf("%s", "You are over 25 years old!");
```

---

## Switch

**The Switch command structure follows the same principle as the Decision Command structure, but we can use it when we have predefined conditions.**

```C
int color;

printf("%s", "Choose between: 1- Red / 2- Blue / 3- Green");
scanf("%d", &color);

switch(color){
  case 1:
    printf("%s", "The color chosen was Red");
    break;
  case 2:
    printf("%s", "The color chosen was Blue");
    break;
  case 3:
    printf("%s", "The color chosen was Green");
    break;
  default:
    printf("%s", "Error. Choose between 1, 2 and 3");
```

> **Hint: Switch can only be used for decisions involving int and char variables**.

