#include <stdio.h>

int mutex = 1, shared = 0;

void lock() {
    if (mutex == 1)
        mutex = 0;
    else
        printf("Mutex Locked\n");
}

void unlock() {
    mutex = 1;
}

int main() {
    printf("Before Critical Section: %d\n", shared);

    lock();              // Acquire mutex lock
    shared++;            // Critical section
    printf("Inside Critical Section: %d\n", shared);
    unlock();            // Release mutex lock

    printf("After Critical Section: %d\n", shared);

    return 0;
}

OUTPUT:

Before Critical Section: 0
Inside Critical Section: 1
After Critical Section: 1
