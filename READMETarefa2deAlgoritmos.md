#include <stdio.h>
#include <stdbool.h>

// Função para verificar se um número é primo
bool primo(int num) {
    if (num < 2) return false;
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) return false;
    }
    return true;
}

// Função para somar os N primeiros números primos
int somaPrimos(int n) {
    int soma = 0, contador = 0, numero = 2;

    while (contador < n) {
        if (primo(numero)) {
            soma += numero;
            contador++;
        }
        numero++;
    }

    return soma;
}

int main() {
    int n;

    // Entrada do número de primos a somar
    printf("Digite o número de primos a somar: ");
    scanf("%d", &n);

    // Cálculo e exibição do resultado
    int resultado = somaPrimos(n);
    printf("A soma dos %d primeiros números primos é: %d\n", n, resultado);

    return 0;
}
