## DATE: 28-03-2026

## AIM:
To write a C program to calculate the area of a triangle using pointers.

## Algorithm
1. **Start** the program.
2. **Declare** floating-point variables for base ($b$), height ($h$), and area ($a$).
3. **Declare** pointer variables (e.g., `*pb`, `*ph`, `*pa`) and assign them the addresses of $b$, $h$, and $a$ respectively.
4. **Read** the values of base and height from the user using the pointers.
5. **Calculate** the area using the formula: $Area = 0.5 \times (*pb) \times (*ph)$.
6. **Store** the result in the memory location pointed to by `pa`.
7. **Display** the calculated area using the pointer.
8. **Stop** the program.

## Program:
```c
#include <stdio.h>
int main() {
    float b, h, a;
    float *pb, *ph, *pa;
    pb = &b;
    ph = &h;
    pa = &a;
    printf("Enter base of triangle: ");
    scanf("%f", pb);
    printf("Enter height of triangle: ");
    scanf("%f", ph);
    *pa = 0.5 * (*pb) * (*ph);
    printf("Area of Triangle: %.2f\n", *pa);
    return 0;
}
```

## Output:
```text
Enter base of triangle: 10
Enter height of triangle: 5
Area of Triangle: 25.00
```

## Result:
Thus the program was executed and the output was verified successfully.

---
Would you like me to show you how to perform this same calculation using a **function that accepts pointers as arguments**?
