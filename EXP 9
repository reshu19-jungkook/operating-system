#include <stdio.h>
#include <sys/ipc.h>
#include <sys/shm.h>
#include <string.h>

int main() {
    key_t key = ftok("shmfile", 65);
    int shmid = shmget(key, 1024, 0666 | IPC_CREAT);

    char *str = (char*) shmat(shmid, NULL, 0);

    printf("Enter message: ");
    scanf("%s", str);

    printf("Data written in memory: %s\n", str);

    shmdt(str);

    return 0;
}

output:
Enter message: hello 
Data written in memory: hello
