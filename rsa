#include <stdio.h>
#include <stdlib.h>

void factorize(int revnumber) {
    if (revnumber % 2 == 0) {
        printf("%d=%d*%d\n", revnumber, revnumber / 2, 2);
        return;
    }
    
    int i = 3;
    while (i < revnumber / 2) {
        if (revnumber % i == 0) {
            printf("%d=%d*%d\n", revnumber, revnumber / i, i);
            return;
        }
        i = i + 2;
    }
    
    if (i == (revnumber / 2) + 1) {
        printf("%d=%d*%d\n", revnumber, revnumber, 1);
    }
}

int main(int argc, char *argv[]) {
    if (argc != 2) {
        return (1);
    }

    FILE *file = fopen(argv[1], "r");
    if (file == NULL) {
        return (1);
    }

    char line[256];
    while (fgets(line, sizeof(line), file) != NULL) {
        int revnumber = atoi(line);
        factorize(revnumber);
    }

    fclose(file);

    return (0);
}
