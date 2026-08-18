#include <stdio.h>

int main() {
    int b[20],n,i;

    printf("Enter number of blocks: ");
    scanf("%d",&n);

    printf("Enter block numbers: ");
    for(i=0;i<n;i++)
        scanf("%d",&b[i]);

    printf("Linked Allocation:\n");

    for(i=0;i<n-1;i++)
        printf("%d -> ",b[i]);

    printf("%d -> NULL\n",b[n-1]);

    return 0;
}
input:
Enter number of blocks: 5
Enter block numbers: 9 16 1 10 25
output:
Linked Allocation:
9 -> 16 -> 1 -> 10 -> 25 -> NULL
