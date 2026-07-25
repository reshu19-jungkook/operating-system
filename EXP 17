#include <stdio.h>

int main() {
    int n, m, i, j, k;
    int alloc[10][10], max[10][10], need[10][10];
    int avail[10], finish[10] = {0}, safe[10];

    printf("Enter number of processes and resources: ");
    scanf("%d%d", &n, &m);

    printf("Enter Allocation Matrix:\n");
    for(i = 0; i < n; i++)
        for(j = 0; j < m; j++)
            scanf("%d", &alloc[i][j]);

    printf("Enter Maximum Matrix:\n");
    for(i = 0; i < n; i++)
        for(j = 0; j < m; j++)
            scanf("%d", &max[i][j]);

    printf("Enter Available Resources:\n");
    for(i = 0; i < m; i++)
        scanf("%d", &avail[i]);

    // Calculate Need Matrix
    for(i = 0; i < n; i++)
        for(j = 0; j < m; j++)
            need[i][j] = max[i][j] - alloc[i][j];

    k = 0;
    while(k < n) {
        for(i = 0; i < n; i++) {
            if(finish[i] == 0) {
                int flag = 1;
                for(j = 0; j < m; j++) {
                    if(need[i][j] > avail[j]) {
                        flag = 0;
                        break;
                    }
                }

                if(flag) {
                    safe[k++] = i;
                    finish[i] = 1;
                    for(j = 0; j < m; j++)
                        avail[j] += alloc[i][j];
                }
            }
        }
    }

    if(k == n) {
        printf("Safe Sequence: ");
        for(i = 0; i < n; i++)
            printf("P%d ", safe[i]);
    } else {
        printf("System is in Deadlock");
    }

INPUT:
Enter number of processes and resources:
3 3

Enter Allocation Matrix:
0 1 0
2 0 0
3 0 2

Enter Maximum Matrix:
7 5 3
3 2 2
9 0 2

Enter Available Resources:
3 3 2

OUTPUT:
Safe Sequence: P1 P2 P0
    return 0;
}
