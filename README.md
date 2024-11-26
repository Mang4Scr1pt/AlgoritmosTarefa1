#include <stdio.h>

int main() {
    int n, i, j;
    
    printf("Digite o tamanho da matriz: ");
    scanf("%d", &n);

    int mat[n][n];

    for (i = 0; i < n; i++) {
        for (j = 0; j < n; j++) {
            if (i < j) {
                mat[i][j] = i + 1;
            } else if (i == j) {
                mat[i][j] = i + 1;
            } else {
                mat[i][j] = 0;
            }
        }
    }

    printf("Matriz:\n");
    for (i = 0; i < n; i++) {
        for (j = 0; j < n; j++) {
            printf("%d ", mat[i][j]);
        }
        printf("\n");
    }

    return 0;
}![IMG_7390](https://github.com/user-attachments/assets/891d5687-2f53-41ad-abe9-d41bd45cbd4f)
