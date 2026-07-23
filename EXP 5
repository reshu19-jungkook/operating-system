#include <stdio.h>

int main() {
    int n, i, j;
    int bt[10], p[10], wt[10], tat[10];

    printf("Enter number of processes: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        printf("Enter Burst Time and Priority of P%d: ", i + 1);
        scanf("%d %d", &bt[i], &p[i]);
    }

    // Sort by Priority (smaller number = higher priority)
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(p[i] > p[j]) {
                int temp;
                temp = p[i]; p[i] = p[j]; p[j] = temp;
                temp = bt[i]; bt[i] = bt[j]; bt[j] = temp;
            }
        }
    }

    wt[0] = 0;
    for(i = 1; i < n; i++)
        wt[i] = wt[i - 1] + bt[i - 1];

    for(i = 0; i < n; i++)
        tat[i] = wt[i] + bt[i];

    printf("\nPriority\tBT\tWT\tTAT\n");
    for(i = 0; i < n; i++)
        printf("%d\t\t%d\t%d\t%d\n", p[i], bt[i], wt[i], tat[i]);

    return 0;

INPUT:
Enter number of processes: 3
Enter Burst Time and Priority of P1: 5 2
Enter Burst Time and Priority of P2: 3 1
Enter Burst Time and Priority of P3: 4 3

OUTPUT:
Priority    BT    WT    TAT
1           3     0     3
2           5     3     8
3           4     8     12
}
