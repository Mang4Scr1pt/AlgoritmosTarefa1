#include <stdio.h>

int main() {
    int pontuacoes[3][5] = {
        {10, 20, 15, 30, 25},
        {20, 30, 25, 40, 35},
        {15, 95, 20, 30, 25}
    };

    int i, j, maior_pontuacao = 0, jogador_campeao = 0;

    for (i = 0; i < 3; i++) {
        int pontuacao_total = 0;

        for (j = 0; j < 5; j++) {
            pontuacao_total += pontuacoes[i][j];
        }

        if (pontuacao_total > maior_pontuacao) {
            maior_pontuacao = pontuacao_total;
            jogador_campeao = i;
        }
    }

    printf("\nO jogador campeão foi o %d com %d pontos\n", jogador_campeao + 1, maior_pontuacao);

    return 0;
}![IMG_7391](https://github.com/user-attachments/assets/53aed44c-b4e5-449a-9bdc-5ad45fe382ec)
