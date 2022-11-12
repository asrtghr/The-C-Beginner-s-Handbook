## Data Input and Output

Whenever we want to show data to the user or send a message for the user to do a certain action, we can use the native functions of **C** for that.

### **Data Input**
To perform an allocation of a value received during the code, we will have to use the **native allocation function** `scanf()`.
```C
int age;

scanf("%d", &age);
```

Note that to receive a value, we will always have an execution order.

**The command** `%d` **tells the machine that a value of type integer** will be allocated to a variable.**

**The command** `&variable` **pass the memory address of the variable that will be allocated a value.**

### **Data Output**

Now when we want to show this data stored in our variables to the user, we will use another native function of the **C** language, the `printf()` function.
```C
printf("%s","Hello World");
```

In the example above we are calling the native function `printf()` and asking it to print a string or string on the screen.

**Note that, to print a value to the user, it is always necessary to indicate the type of variable to be *printed*.**

```C
int age = 22;
printf("%s %d %s", "My name is John and I am: ", age, " years old");
```

Note that it is possible to *print* different types of variables on the screen at once, just pay attention to their respective orders according to the formatting.

---

## Arithmetic Operators

**As in every programming language, we will perform the algorithm operations through mathematical logic operations.**

| Operation | Operator | Example | Result|
| :--- | :---: | :---: | :---:|
| **Adição** | `+` | 10 `+` 5 | 15 |
| **Subtração** | `-` | 10 `-` 5 | 5 |
| **Divisão** | `/` | 10 `/` 5 | 2 |
| **Produto** | `*` | 10 `*` 5 | 50 |
| **Resto de Divisão** | `%` | 10 `%` 5 | 0 |

**Order of Precedence**
```html
() 
* / %  
+ -
```

---

## Increment and Decrement
In **C** we can **increase or decrease** the value of a numeric variable using the command `++` or `--` respectively.

```C
int a, b, sum;

a = b = sum = 0;

sum = a + b++;

OUTPUT: 0
```

```C
int a, b sum;

a = b = sum = 0;

sum = a + ++b;

OUTPUT: 1
```
