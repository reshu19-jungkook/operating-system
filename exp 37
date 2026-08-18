#include <stdio.h>
#include <stdlib.h>

int main() {
    int a[20],n,head,i,total=0;

    printf("Enter number of requests: ");
    scanf("%d",&n);

    printf("Enter requests: ");
    for(i=0;i<n;i++) scanf("%d",&a[i]);

    printf("Enter initial head: ");
    scanf("%d",&head);

    for(i=0;i<n;i++) {
        total += abs(head-a[i]);
        head=a[i];
    }

    printf("Total Head Movement = %d\n",total);
    return 0;
}

input:
Enter number of requests: 5
Enter requests: 82 170 43 140 24
Enter initial head: 50
output:
Total Head Movement = 468
