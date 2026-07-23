#include <stdio.h>
#include <string.h>

int main() {
    int i, j, u;
    printf("Enter number of users: ");
    scanf("%d", &u);

    char user[u][20], file[u][10][20];
    int f[u];

    for(i = 0; i < u; i++) {
        printf("Enter user name: ");
        scanf("%s", user[i]);

        printf("Enter number of files: ");
        scanf("%d", &f[i]);

        for(j = 0; j < f[i]; j++) {
            printf("Enter file name: ");
            scanf("%s", file[i][j]);
        }
    }

    printf("\nDirectory Structure:\n");
    for(i = 0; i < u; i++) {
        printf("%s:\n", user[i]);
        for(j = 0; j < f[i]; j++) {
            printf("  %s\n", file[i][j]);
        }
    }

    return 0;
}
output:
Enter number of users: 2
Enter user name: U1
Enter number of files: 2
Enter file name: a.fxl
Enter file name: b.fxl
Enter user name: U2
Enter number of files: 3
Enter file name: x.fxl
Enter file name: y.fxl
Enter file name: z.fxl

Directory Structure:
U1:
  a.fxl
  b.fxl
U2:
  x.fxl
  y.fxl
  z.fxl
