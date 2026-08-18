#include <stdio.h>
#include <fcntl.h>
#include <unistd.h>
#include <sys/stat.h>
#include <dirent.h>

int main() {
    int fd;
    struct stat st;
    DIR *d;
    struct dirent *e;

    fd=open("test.txt",O_RDWR|O_CREAT,0644);

    printf("File descriptor: %d\n",fd);

    lseek(fd,0,SEEK_END);
    printf("Seek successful\n");

    stat("test.txt",&st);
    printf("File size: %ld bytes\n",st.st_size);

    printf("Directory files:\n");
    d=opendir(".");
    while((e=readdir(d))!=NULL)
        printf("%s\n",e->d_name);

    closedir(d);
    close(fd);
    return 0;
}

output:
File descriptor: 3
Seek successful
File size: 25 bytes
Directory files:
.
..
test.txt
program.c
