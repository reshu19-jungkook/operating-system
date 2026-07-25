#include <stdio.h>

int mutex = 1, wrt = 1, readcount = 0;

void reader() {
    mutex = 0;
    readcount++;

    if (readcount == 1)
        wrt = 0;

    mutex = 1;

    printf("Reader is reading\n");

    mutex = 0;
    readcount--;

    if (readcount == 0)
        wrt = 1;

    mutex = 1;
}

void writer() {
    if (wrt == 1) {
        wrt = 0;
        printf("Writer is writing\n");
        wrt = 1;
    } else {
        printf("Writer is waiting\n");
    }
}

int main() {
    int ch;

    do {
        printf("\n1. Reader\n2. Writer\n3. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &ch);

        switch(ch) {
            case 1:
                reader();
                break;
            case 2:
                writer();
                break;
            case 3:
                break;
            default:
                printf("Invalid Choice\n");
        }
    } while(ch != 3);

INPUT:
1
2
1
3

OUTPUT:
1. Reader
2. Writer
3. Exit
Enter your choice: 1
Reader is reading

1. Reader
2. Writer
3. Exit
Enter your choice: 2
Writer is writing

1. Reader
2. Writer
3. Exit
Enter your choice: 1
Reader is reading
    return 0;
}
