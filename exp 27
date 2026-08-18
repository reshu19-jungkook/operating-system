#include <stdio.h>
#include <dirent.h>

int main() {
    DIR *d;
    struct dirent *e;

    d=opendir(".");
    if(d==NULL) {
        printf("Cannot open directory");
        return 1;
    }

    while((e=readdir(d))!=NULL)
        printf("%s\n",e->d_name);

    closedir(d);
    return 0;
}
output:
.
..
program.c
data.txt
test.txt
