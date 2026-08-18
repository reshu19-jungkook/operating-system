#include <stdio.h>

int main() {
    int b[10], p[10], n, m, i, j;

    printf("Enter number of blocks: ");
    scanf("%d",&m);
    printf("Enter block sizes: ");
    for(i=0;i<m;i++) scanf("%d",&b[i]);

    printf("Enter number of processes: ");
    scanf("%d",&n);
    printf("Enter process sizes: ");
    for(i=0;i<n;i++) scanf("%d",&p[i]);

    for(i=0;i<n;i++) {
        for(j=0;j<m;j++) {
            if(b[j] >= p[i]) {
                printf("Process %d -> Block %d\n",i+1,j+1);
                b[j] -= p[i];
                break;
            }
        }
        if(j==m) printf("Process %d -> Not Allocated\n",i+1);
    }
    return 0;
}

input:
Enter number of blocks: 3
Enter block sizes: 100 500 200
Enter number of processes: 3
Enter process sizes: 212 417 112
output:
Process 1 -> Block 2
Process 2 -> Not Allocated
Process 3 -> Block 1
