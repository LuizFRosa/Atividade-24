# Atividade-24

#include <stdio.h>  
#include <math.h>  

int main() {
    
	long long binarionum, decimalNum = 0, i = 0, restante;

    // Solicita ao usuário que insira um número binário
    printf("Digite um numero binario: ");
    scanf("%lld", &binarionum);  // Lê o número binário fornecido pelo usuário

    // Converte o número binário em decimal
    while (binarionum != 0) {  // Continua o loop enquanto houver dígitos no número binário
        restante = binarionum % 10;  // Obtém o último dígito do número binário
        decimalNum += restante * pow(2, i);  // Converte o dígito binário em decimal e soma ao total
        binarionum /= 10;  // Remove o último dígito do número binário
        i++;  // Incrementa a potência de 2
    }

    // Exibe o número decimal equivalente
    printf("O decimal equivalente e: %lld\n", decimalNum);

    return 0;  // Indica que o programa terminou com sucesso
}
