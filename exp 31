#include <stdio.h>

int main() {
    int p[20], f[10], n,m,i,j,k=0,hit,fault=0;

    printf("Enter number of pages: ");
    scanf("%d",&n);

    printf("Enter pages: ");
    for(i=0;i<n;i++) scanf("%d",&p[i]);

    printf("Enter number of frames: ");
    scanf("%d",&m);

    for(i=0;i<n;i++) {
        hit=0;
        for(j=0;j<m;j++)
            if(f[j]==p[i]) hit=1;

        if(!hit) {
            f[k]=p[i];
            k=(k+1)%m;
            fault++;
        }
    }

    printf("Page Faults = %d\n",fault);
    return 0;
}

input:
Enter number of pages: 7
Enter pages: 1 2 3 1 4 2 5
Enter number of frames: 3
output:
Page Faults = 6
