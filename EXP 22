#include <stdio.h>

int main() {
    int b[10], p[10], n, m, i, j, k;

    printf("Blocks: ");
    scanf("%d", &n);
    printf("Processes: ");
    scanf("%d", &m);

    for(i=0;i<n;i++) scanf("%d",&b[i]);
    for(i=0;i<m;i++) scanf("%d",&p[i]);

    for(i=0;i<m;i++) {
        k=-1;
        for(j=0;j<n;j++)
            if(b[j]>=p[i] && (k==-1 || b[j]<b[k]))
                k=j;

        if(k!=-1) {
            printf("P%d -> B%d\n", i+1, k+1);
            b[k]-=p[i];
        } else
            printf("P%d -> Not Allocated\n", i+1);
    }
    return 0;
}

INPUT:
Blocks: 3
Processes: 3
100 500 200
120 100 180

OUTPUT:
P1 -> B3
P2 -> B1
P3 -> B2
