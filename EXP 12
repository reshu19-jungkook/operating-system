#include <stdio.h>
#include <pthread.h>
#include <semaphore.h>

sem_t chopstick[5];

void* philosopher(void* num) {
    int id = *(int*)num;

    sem_wait(&chopstick[id]);
    sem_wait(&chopstick[(id+1)%5]);

    printf("Philosopher %d is eating\n", id);

    sem_post(&chopstick[id]);
    sem_post(&chopstick[(id+1)%5]);

    return NULL;
}

int main() {
    pthread_t ph[5];
    int i, id[5];

    for(i = 0; i < 5; i++)
        sem_init(&chopstick[i], 0, 1);

    for(i = 0; i < 5; i++) {
        id[i] = i;
        pthread_create(&ph[i], NULL, philosopher, &id[i]);
    }

    for(i = 0; i < 5; i++)
        pthread_join(ph[i], NULL);

    return 0;
}
output:
Philosopher 0 is eating
Philosopher 2 is eating
Philosopher 3 is eating
Philosopher 1 is eating
Philosopher 4 is eating
