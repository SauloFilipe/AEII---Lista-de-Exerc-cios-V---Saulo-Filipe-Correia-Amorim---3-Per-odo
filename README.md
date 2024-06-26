#include <stdio.h>
#include <string.h>

struct Carro {
    char marca[50];
    char modelo[50];
    int anoFabricacao;
};

int mesmoModelo(struct Carro carro1, struct Carro carro2) {

    if (strcmp(carro1.modelo, carro2.modelo) == 0) {
        return 1;
    } else {
        return 0;
    }
}

int main() {

    struct Carro carro1 = {"Koenigsegg", "Jesko", 2019};
    struct Carro carro2 = {"Skyline", "GTR-R35", 2007};
    struct Carro carro3 = {"Lamborghini", "Aventador", 2011};

    if (mesmoModelo(carro1, carro2)) {
        printf("carro1 e carro2 sao do mesmo modelo.\n");
    } else {
        printf("carro1 e carro2 nao sao do mesmo modelo.\n");
    }

    if (mesmoModelo(carro1, carro3)) {
        printf("carro1 e carro3 sao do mesmo modelo.\n");
    } else {
        printf("carro1 e carro3 nao sao do mesmo modelo.\n");
    }

    return 0;
}
