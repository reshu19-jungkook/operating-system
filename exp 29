#include <stdio.h>
#include <pthread.h>
#include <semaphore.h>

int buffer, full=0;
sem_t empty, mutex;

void *producer(void *x) {
    sem_wait(&empty);
    sem_wait(&mutex);

    buffer=10;
    printf("Produced: %d\n",buffer);

    sem_post(&mutex);
    return 0;
}

void *consumer(void *x) {
    sem_wait(&mutex);

    printf("Consumed: %d\n",buffer);
    sem_post(&empty);
    return 0;
}

int main() {
    pthread_t p,c;

    sem_init(&empty,0,1);
    sem_init(&mutex,0,1);

    pthread_create(&p,NULL,producer,NULL);
    pthread_join(p,NULL);

    pthread_create(&c,NULL,consumer,NULL);
    pthread_join(c,NULL);

    return 0;
}

output:
Produced: 10
Consumed: 10
