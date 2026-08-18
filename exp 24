#include <stdio.h>
#include <fcntl.h>
#include <unistd.h>

int main() {
    int fd;
    char s[50];

    fd = open("test.txt", O_CREAT|O_RDWR, 0644);

    printf("Enter text: ");
    scanf(" %[^\n]",s);

    write(fd,s,sizeof(s));
    lseek(fd,0,SEEK_SET);

    read(fd,s,sizeof(s));
    printf("File content: %s\n",s);

    close(fd);
    return 0;
}

input:
Enter text: Hello Linux
output:
Enter text: Hello Linux
