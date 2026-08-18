#include <stdio.h>
#include <stdlib.h>

int main() {
    int a[20],n,head,size,i,j,temp,total=0;

    printf("Enter number of requests: ");
    scanf("%d",&n);

    printf("Enter requests: ");
    for(i=0;i<n;i++) scanf("%d",&a[i]);

    printf("Enter initial head: ");
    scanf("%d",&head);

    printf("Enter disk size: ");
    scanf("%d",&size);

    for(i=0;i<n;i++)
        for(j=i+1;j<n;j++)
            if(a[i]>a[j])
                temp=a[i],a[i]=a[j],a[j]=temp;

    for(i=0;i<n;i++)
        if(a[i]>=head) break;

    for(j=i;j<n;j++)
        total+=abs(head-a[j]),head=a[j];

    total+=size-1-head;
    head=0;

    total+=size-1;

    for(j=0;j<i;j++)
        total+=abs(head-a[j]),head=a[j];

    printf("Total Head Movement = %d\n",total);
    return 0;
}

input:
Enter number of requests: 5
Enter requests: 82 170 43 140 24
Enter initial head: 50
Enter disk size: 200
output:
Total Head Movement = 391
