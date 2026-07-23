#include <stdio.h>

int main() {
    int nb, np, i, j;
    printf("Enter number of blocks: ");
    scanf("%d", &nb);

    printf("Enter number of processes: ");
    scanf("%d", &np);

    int block[nb], process[np];

    for(i = 0; i < nb; i++) scanf("%d", &block[i]);
    for(i = 0; i < np; i++) scanf("%d", &process[i]);

    for(i = 0; i < np; i++) {
        for(j = 0; j < nb; j++) {
            if(block[j] >= process[i]) {
                printf("Process %d allocated to block %d\n", i+1, j+1);
                block[j] -= process[i];
                break;
            }
        }
    }

    return 0;
}
output:
Enter number of blocks: 5
Enter number of processes: 4
Enter block sizes:
100 200 500 600 300
Enter process sizes:
212 417 112 426
Process 1 allocated to block 3
Process 2 allocated to block 4
Process 3 allocated to block 2
Process 4 not allocated
