## DATE: 28-03-2026

## AIM:
To write a C program to count the total number of even elements in an array using dynamic memory allocation via `calloc()`.

## Algorithm
1. **Start** the program.
2. **Declare** an integer pointer (`*arr`) and variables for size (`n`), loop counter (`i`), and a `count` initialized to 0.
3. **Read** the number of elements from the user.
4. **Allocate** memory dynamically for `n` integers using `calloc(n, sizeof(int))`.
5. **Input** the elements into the dynamically allocated memory.
6. **Iterate** through the array:
    * Check if `arr[i] % 2 == 0`.
    * If true, increment the `count`.
7. **Display** the total count of even elements.
8. **Free** the allocated memory and **Stop** the program.

## Program:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, i, count = 0;
    int *arr;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    arr = (int*)calloc(n, sizeof(int));
    if (arr == NULL) {
        printf("Memory not allocated.\n");
        return 0;
    }
    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) {
        scanf("%d", arr + i);
    }
    for (i = 0; i < n; i++) {
        if (*(arr + i) % 2 == 0) {
            count++;
        }
    }
    printf("Total number of even elements: %d\n", count);
    free(arr);
    return 0;
}
```

## Output:
```text
Enter number of elements: 5
Enter 5 elements: 12 7 8 20 15
Total number of even elements: 3
```

## Result:
Thus the program was executed and the output was verified successfully.

---
Would you like me to explain the difference between **malloc()** and **calloc()** regarding how they initialize memory?
