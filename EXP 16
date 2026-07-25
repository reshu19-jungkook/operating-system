#include <stdio.h>

struct Employee {
    int id;
    char name[20];
    float salary;
};

int main() {
    FILE *fp;
    struct Employee e;
    int n, i, pos;

    fp = fopen("employee.dat", "wb+");

    printf("Enter number of employees: ");
    scanf("%d", &n);

    // Write employee details
    for(i = 0; i < n; i++) {
        printf("\nEmployee %d\n", i + 1);
        printf("ID: ");
        scanf("%d", &e.id);
        printf("Name: ");
        scanf("%s", e.name);
        printf("Salary: ");
        scanf("%f", &e.salary);

        fwrite(&e, sizeof(e), 1, fp);
    }

    // Random access
    printf("\nEnter employee record number to view (1-%d): ", n);
    scanf("%d", &pos);

    fseek(fp, (pos - 1) * sizeof(e), SEEK_SET);
    fread(&e, sizeof(e), 1, fp);

    printf("\nEmployee Details\n");
    printf("ID: %d\n", e.id);
    printf("Name: %s\n", e.name);
    printf("Salary: %.2f\n", e.salary);

    fclose(fp);

INPUT:
Enter number of employees: 2

Employee 1
ID: 101
Name: Ram
Salary: 25000

Employee 2
ID: 102
Name: Ravi
Salary: 30000

Enter employee record number to view (1-2): 2

OUTPUT:
Employee Details
ID: 102
Name: Ravi
Salary: 30000.00

    return 0;
}
