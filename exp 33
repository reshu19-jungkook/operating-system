#include <stdio.h>

int main() {
    int p[20],f[10],n,m,i,j,k,hit,pos,fault=0,far,next;

    printf("Enter number of pages: ");
    scanf("%d",&n);

    printf("Enter pages: ");
    for(i=0;i<n;i++) scanf("%d",&p[i]);

    printf("Enter number of frames: ");
    scanf("%d",&m);

    k=0;

    for(i=0;i<n;i++) {
        hit=0;

        for(j=0;j<m;j++)
            if(f[j]==p[i]) hit=1;

        if(!hit) {
            if(k<m) pos=k++;
            else {
                far=-1;
                for(j=0;j<m;j++) {
                    for(next=i+1;next<n;next++)
                        if(f[j]==p[next]) break;

                    if(next>far)
                        far=next,pos=j;
                }
            }
            f[pos]=p[i];
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
Page Faults = 5
