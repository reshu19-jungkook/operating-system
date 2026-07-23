#include <stdio.h>

int main() {
    int n, i, tq, time = 0, remain;
    int bt[10], rt[10], wt[10], tat[10];

    printf("Enter number of processes: ");
    scanf("%d", &n);

    remain = n;

    for(i = 0; i < n; i++) {
        printf("Enter Burst Time of P%d: ", i + 1);
        scanf("%d", &bt[i]);
        rt[i] = bt[i];
    }

    printf("Enter Time Quantum: ");
    scanf("%d", &tq);

    while(remain > 0) {
        for(i = 0; i < n; i++) {
            if(rt[i] > 0) {
                if(rt[i] <= tq) {
                    time += rt[i];
                    rt[i] = 0;
                    tat[i] = time;
                    wt[i] = tat[i] - bt[i];
                    remain--;
                } else {
                    time += tq;
                    rt[i] -= tq;
                }
            }
        }
    }

    printf("\nP\tBT\tWT\tTAT\n");
    for(i = 0; i < n; i++)
        printf("P%d\t%d\t%d\t%d\n", i + 1, bt[i], wt[i], tat[i]);

INPUT:
Enter number of processes: 3
Enter Burst Time of P1: 5
Enter Burst Time of P2: 4
Enter Burst Time of P3: 2
Enter Time Quantum: 2

OUTPUT:
P    BT    WT    TAT
P1   5     6     11
P2   4     6     10
P3   2     4      6

    return 0;
}
