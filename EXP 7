#include <stdio.h>

int main() {
    int n, i, j;
    int bt[10], wt[10], tat[10];

    printf("Enter number of processes: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        printf("Enter Burst Time of P%d: ", i + 1);
        scanf("%d", &bt[i]);
    }

    // Sort burst times
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(bt[i] > bt[j]) {
                int temp = bt[i];
                bt[i] = bt[j];
                bt[j] = temp;
            }
        }
    }

    wt[0] = 0;
    for(i = 1; i < n; i++)
        wt[i] = wt[i - 1] + bt[i - 1];

    for(i = 0; i < n; i++)
        tat[i] = wt[i] + bt[i];

    printf("\nBT\tWT\tTAT\n");
    for(i = 0; i < n; i++)
        printf("%d\t%d\t%d\n", bt[i], wt[i], tat[i]);

INPUT:
Enter number of processes: 3
Enter Burst Time of P1: 5
Enter Burst Time of P2: 2
Enter Burst Time of P3: 4

OUTPUT:
BT      WT      TAT
2       0       2
4       2       6
5       6       11

    return 0;
}
