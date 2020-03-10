# Duplicated Code!

## How to recognize Duplicated Code

[Sourced From Wikipedia](https://en.wikipedia.org/wiki/Duplicate_code)  
When two sections or functions do the same thing, it is code duplication. Some algorithms to detect code duplication are: Baker's algorithm, Rabin–Karp string search algorithm. Using Abstract Syntax Trees, Visual clone detection, count Matrix Clone Detection, Locality-sensitive hashing, and Anti-unification.

## Duplicated Code example:

[Sourced From Wikipedia](https://en.wikipedia.org/wiki/Duplicate_code)
```cpp
extern int array_a[];
extern int array_b[];
 
int sum_a = 0;

for (int i = 0; i < 4; i++)
   sum_a += array_a[i];

int average_a = sum_a / 4;
 
int sum_b = 0;

for (int i = 0; i < 4; i++)
   sum_b += array_b[i];

int average_b = sum_b / 4;
```

Can be replaced with

```cpp
int calc_average_of_four(int* array) {
   int sum = 0;
   for (int i = 0; i < 4; i++)
       sum += array[i];

   return sum / 4;
}
```

## Why is it bad design?

Because if you need to change the functionality of anything that is duplicated, you have to change it in every place it is duplicated. If it was abstracted into a single function, you'd only have to change that function

## How should it be fixed?

All duplicated code that does the same functionality should be abstracted into a single function.
