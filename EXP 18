#include <stdio.h>

int mutex = 1, full = 0, empty = 3, x = 0;

void producer() {
    if ((mutex == 1) && (empty != 0)) {
        mutex = 0;
        full++;
        empty--;
        x++;
        printf("Producer produces item %d\n", x);
        mutex = 1;
    } else {
        printf("Buffer is Full\n");
    }
}

void consumer() {
    if ((mutex == 1) && (full != 0)) {
        mutex = 0;
        full--;
        empty++;
        printf("Consumer consumes item %d\n", x);
        x--;
        mutex = 1;
    } else {
        printf("Buffer is Empty\n");
    }
}

int main() {
    int ch;

    do {
        printf("\n1. Producer\n2. Consumer\n3. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &ch);

        switch(ch) {
            case 1: producer(); break;
            case 2: consumer(); break;
            case 3: break;
            default: printf("Invalid Choice");
        }
    } while(ch != 3);

INPUT:
1
1
2
2
3
OUTPUT:

1. Producer
2. Consumer
3. Exit
Enter your choice: 1
Producer produces item 1

1. Producer
2. Consumer
3. Exit
Enter your choice: 1
Producer produces item 2

1. Producer
2. Consumer
3. Exit
Enter your choice: 2
Consumer consumes item 2

1. Producer
2. Consumer
3. Exit
Enter your choice: 2
Consumer consumes item 1
    return 0;
}
