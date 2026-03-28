## DATE: 28-03-2026

## AIM:
To write a C program to store and display the name, ID, age, and salary of multiple employees using an array of structures.

## Algorithm
1. **Start** the program.
2. **Define** a structure named `Employee` with members: `name` (string), `id` (int), `age` (int), and `salary` (float).
3. **Declare** an array of structures of type `Employee` to store data for multiple individuals.
4. **Input** the number of employees ($n$) and use a `for` loop to **Read** the details (name, id, age, salary) for each employee.
5. **Use** another `for` loop to **Display** the stored details of all employees in a formatted manner.
6. **Stop** the program.

## Program:
```c
#include <stdio.h>

struct Employee {
    char name[50];
    int id;
    int age;
    float salary;
};

int main() {
    struct Employee emp[100];
    int n, i;
    printf("Enter the number of employees: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);
        printf("Name: ");
        scanf("%s", emp[i].name);
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Age: ");
        scanf("%d", &emp[i].age);
        printf("Salary: ");
        scanf("%f", &emp[i].salary);
    }
    printf("\n--- Employee Details ---\n");
    for (i = 0; i < n; i++) {
        printf("ID: %d | Name: %s | Age: %d | Salary: %.2f\n", 
                emp[i].id, emp[i].name, emp[i].age, emp[i].salary);
    }
    return 0;
}
```

## Output:
```text
Enter the number of employees: 2

Enter details for Employee 1:
Name: Alice
ID: 101
Age: 28
Salary: 55000.50

Enter details for Employee 2:
Name: Bob
ID: 102
Age: 32
Salary: 62000.75

--- Employee Details ---
ID: 101 | Name: Alice | Age: 28 | Salary: 55000.50
ID: 102 | Name: Bob | Age: 32 | Salary: 62000.75
```

## Result:
Thus the program was executed and the output was verified successfully.

---
Would you like me to show you how to use **nested structures** to include an employee's address or date of joining?
