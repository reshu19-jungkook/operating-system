#include <stdio.h>

int main()
{
    int n, bt[10], wt[10], tat[10], i;

    printf("Enter number of processes: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++)
    {
        printf("Burst Time P%d: ", i + 1);
        scanf("%d", &bt[i]);
    }

    wt[0] = 0;
    for(i = 1; i < n; i++)
        wt[i] = wt[i - 1] + bt[i - 1];

    for(i = 0; i < n; i++)
        tat[i] = wt[i] + bt[i];

    printf("\nP\tBT\tWT\tTAT\n");
    for(i = 0; i < n; i++)
        printf("P%d\t%d\t%d\t%d\n", i + 1, bt[i], wt[i], tat[i]);

    return 0;
}

OUTPUT:

Input:Enter number of processes: 3
Burst Time P1: 5
Burst Time P2: 3
Burst Time P3: 2

output:
P	BT	WT	TAT
P1	5	0	5
P2	3	5	8
P3	2	8	10
=== Code Execution Successful ===
