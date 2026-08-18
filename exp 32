#include <stdio.h>

int main() {
    int p[20],f[10],t[10],n,m,i,j,k=0,min,pos,fault=0,hit;

    printf("Enter number of pages: ");
    scanf("%d",&n);

    printf("Enter pages: ");
    for(i=0;i<n;i++) scanf("%d",&p[i]);

    printf("Enter number of frames: ");
    scanf("%d",&m);

    for(i=0;i<n;i++) {
        hit=0;

        for(j=0;j<m;j++)
            if(f[j]==p[i]) {
                hit=1;
                t[j]=i;
            }

        if(!hit) {
            if(k<m) pos=k++;
            else {
                min=t[0]; pos=0;
                for(j=1;j<m;j++)
                    if(t[j]<min) min=t[j],pos=j;
            }
            f[pos]=p[i];
            t[pos]=i;
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
