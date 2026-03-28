## DATE: 28-03-2026

## AIM:
To write a C program to check whether a given character is a vowel or consonant using a pointer.

## Algorithm
1. **Start** the program.
2. **Declare** a character variable `ch` and a character pointer `*ptr`.
3. **Read** a character from the user and assign the address of `ch` to `ptr`.
4. **Check** the value at the pointer (`*ptr`) using an `if` statement:
    * Compare it against both uppercase and lowercase vowels ($a, e, i, o, u$).
5. **Display** "Vowel" if it matches any of the conditions, otherwise display "Consonant" (ensuring the input is an alphabet).
6. **Stop** the program.

## Program:
```c
#include <stdio.h>
int main() {
    char ch, *ptr;
    printf("Enter a character: ");
    scanf("%c", &ch);
    ptr = &ch;
    if ((*ptr >= 'a' && *ptr <= 'z') || (*ptr >= 'A' && *ptr <= 'Z')) {
        if (*ptr == 'a' || *ptr == 'e' || *ptr == 'i' || *ptr == 'o' || *ptr == 'u' ||
            *ptr == 'A' || *ptr == 'E' || *ptr == 'I' || *ptr == 'O' || *ptr == 'U') {
            printf("%c is a Vowel.\n", *ptr);
        } else {
            printf("%c is a Consonant.\n", *ptr);
        }
    } else {
        printf("Invalid input. Please enter an alphabet.\n");
    }
    return 0;
}
```

## Output:
**Case 1:**
```text
Enter a character: E
E is a Vowel.
```

**Case 2:**
```text
Enter a character: z
z is a Consonant.
```

## Result:
Thus the program was executed and the output was verified successfully.

---
Would you like me to show you how to use a **switch case** with pointers to handle this logic more cleanly?
