#include <stdio.h>

int main() {
    int n, i, time = 0, completed = 0;
    int bt[10], rt[10], at[10], p[10], wt[10], tat[10];
    int min, shortest;

    printf("Enter number of processes: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        printf("Enter Arrival Time, Burst Time and Priority of P%d: ", i + 1);
        scanf("%d %d %d", &at[i], &bt[i], &p[i]);
        rt[i] = bt[i];
    }

    while(completed < n) {
        min = 9999;
        shortest = -1;

        for(i = 0; i < n; i++) {
            if(at[i] <= time && rt[i] > 0 && p[i] < min) {
                min = p[i];
                shortest = i;
            }
        }

        if(shortest == -1) {
            time++;
            continue;
        }

        rt[shortest]--;
        time++;

        if(rt[shortest] == 0) {
            completed++;
            tat[shortest] = time - at[shortest];
            wt[shortest] = tat[shortest] - bt[shortest];
        }
    }

    printf("\nP\tWT\tTAT\n");
    for(i = 0; i < n; i++)
        printf("P%d\t%d\t%d\n", i + 1, wt[i], tat[i]);

INPUT:
Enter number of processes: 3
Enter Arrival Time, Burst Time and Priority of P1: 0 5 2
Enter Arrival Time, Burst Time and Priority of P2: 1 3 1
Enter Arrival Time, Burst Time and Priority of P3: 2 4 3

OUTPUT:
P       WT      TAT
P1      3       8
P2      0       3
P3      6       10
    return 0;
}
