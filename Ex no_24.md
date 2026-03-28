## DATE: 28-03-2026

## AIM:
To create a C program using structures to read the employee number, department, and basic pay of 3 employees, and calculate their Gross Salary ($Gross = BP + DA + HRA$) where $DA = 10\%$ and $HRA = 30\%$ of Basic Pay.

## Algorithm
1. **Start** the program.
2. **Define** a structure `Employee` with members: `empno` (int), `dept` (string), `bp` (float), and `gross` (float).
3. **Declare** an array of structures for 3 employees.
4. **Use a loop** to input `empno`, `dept`, and `bp` for each employee.
5. **Calculate** the Gross Salary for each employee inside the loop:
    * $DA = 0.10 \times BP$
    * $HRA = 0.30 \times BP$
    * $Gross = BP + DA + HRA$
6. **Use another loop** to display the employee details along with the calculated Gross Salary.
7. **Stop** the program.

## Program:
```c
#include <stdio.h>

struct Employee {
    int empno;
    char dept[30];
    float bp;
    float gross;
};

int main() {
    struct Employee e[3];
    int i;
    float da, hra;
    for (i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
        printf("Employee Number: ");
        scanf("%d", &e[i].empno);
        printf("Department: ");
        scanf("%s", e[i].dept);
        printf("Basic Pay: ");
        scanf("%f", &e[i].bp);
        da = 0.10 * e[i].bp;
        hra = 0.30 * e[i].bp;
        e[i].gross = e[i].bp + da + hra;
    }
    printf("\n%-10s %-15s %-10s %-10s\n", "EmpNo", "Dept", "Basic", "Gross");
    for (i = 0; i < 3; i++) {
        printf("%-10d %-15s %-10.2f %-10.2f\n", 
                e[i].empno, e[i].dept, e[i].bp, e[i].gross);
    }
    return 0;
}
```

## Output:
```text
Enter details for Employee 1:
Employee Number: 1001
Department: IT
Basic Pay: 50000
Enter details for Employee 2:
Employee Number: 1002
Department: HR
Basic Pay: 40000
Enter details for Employee 3:
Employee Number: 1003
Department: Sales
Basic Pay: 30000

EmpNo      Dept            Basic      Gross     
1001       IT              50000.00   70000.00  
1002       HR              40000.00   56000.00  
1003       Sales           30000.00   42000.00  
```

## Result:
Thus the program was executed and the output was verified successfully.

---
Would you like me to show you how to find the employee with the **highest gross salary** from this list?
