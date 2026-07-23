#include <stdio.h>

int main() {
    int n, i, j;
    float avg_wt = 0, avg_tat = 0;

    printf("Enter number of processes: ");
    scanf("%d", &n);

    int bt[n], wt[n], tat[n];

    for(i = 0; i < n; i++) {
        printf("Burst time of P%d: ", i+1);
        scanf("%d", &bt[i]);
    }

 
    for(i = 0; i < n; i++) {
        for(j = i+1; j < n; j++) {
            if(bt[i] > bt[j]) {
                int temp = bt[i];
                bt[i] = bt[j];
                bt[j] = temp;
            }
        }
    }

    wt[0] = 0;

    for(i = 1; i < n; i++) {
        wt[i] = wt[i-1] + bt[i-1];
    }
    
    for(i = 0; i < n; i++) {
        tat[i] = wt[i] + bt[i];

        avg_wt += wt[i];
        avg_tat += tat[i];
    }

    printf("\nProcess\tBT\tWT\tTAT\n");
    for(i = 0; i < n; i++) {
        printf("P%d\t%d\t%d\t%d\n", i+1, bt[i], wt[i], tat[i]);
    }

    avg_wt /= n;
    avg_tat /= n;

    printf("\nAverage Waiting Time = %.2f", avg_wt);
    printf("\nAverage Turnaround Time = %.2f\n", avg_tat);

    return 0;
}
output:
Enter number of processes: 4
Burst time of P1: 5
Burst time of P2: 6
Burst time of P3: 2
Burst time of P4: 9

Process	BT	WT	TAT
P1	2	0	2
P2	5	2	7
P3	6	7	13
P4	9	13	22

Average Waiting Time = 5.50
Average Turnaround Time = 11.00
