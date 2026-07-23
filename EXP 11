#include <stdio.h>
#include <pthread.h>

void* print_msg(void* arg) {
    printf("Thread executing\n");
    return NULL;
}

int main() {
    pthread_t t1, t2;

    pthread_create(&t1, NULL, print_msg, NULL);
    pthread_create(&t2, NULL, print_msg, NULL);

    pthread_join(t1, NULL);
    pthread_join(t2, NULL);

    return 0;
}

output
Thread executing
Thread executing
