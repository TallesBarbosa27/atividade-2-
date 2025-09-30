# atividade 2 
 #include <stdio.h>
#include <time.h>
#include <stdlib.h>

int main() {
    int numero_secreto, palpite, tentativas = 0;

    srand(time(NULL));
    numero_secreto = rand() % 100 + 1;  

    printf(" Jogo de Adivinhação\n");
    printf("Tente adivinhar o número entre 1 e 100\n");
    do {
        printf("Digite seu palpite: ");
        scanf("%d", &palpite);
        tentativas++;

        if (palpite < numero_secreto) {
            printf("Maior...\n");
        } else if (palpite > numero_secreto) {
            printf("Menor...\n");
        } else {
            printf("Parabéns! Você acertou em %d tentativa(s)!\n", tentativas);
        }

    } while (palpite != numero_secreto);

    return 0;
}
