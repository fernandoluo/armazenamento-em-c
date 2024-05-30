#include <stdio.h>
#include <string.h>

// Estrutura para armazenar os dados de cada item
struct Item {
    int id;
    char nome[50];
    float unitario;
    int qtde;
    float total_item;
};

int main() {
    // Solicita ao usuário o número de itens que ele deseja inserir
    int numItens;
    printf("Digite o número de itens que você deseja inserir: ");
    scanf("%d", &numItens);

    // Cria um array de structs para armazenar os dados dos itens
    struct Item itens[numItens];

    // Loop para inserir os dados de cada item
    for(int i = 0; i < numItens; i++) {
        printf("\nInsira o item %d:\n", i+1);
        printf("ID: ");
        scanf("%d", &itens[i].id);

        // Verifica se o ID já foi inserido
        for(int j = 0; j < i; j++) {
            if(itens[j].id == itens[i].id) {
                printf("Erro: Este ID já foi inserido. Tente novamente.\n");
                i--;
                break;
            }
        }

        printf("Nome: ");
        scanf("%s", itens[i].nome);

        printf("Valor Unitário: ");
        scanf("%f", &itens[i].unitario);

        printf("Quantidade: ");
        scanf("%d", &itens[i].qtde);

        // Calcula o total do item
        itens[i].total_item = itens[i].unitario * itens[i].qtde;
    }

    // Imprime a lista dos itens com seus respectivos preços
    printf("\nCODIGO     NOME                 QTDE   UNIT    TOTAL\n");
    for(int i = 0; i < numItens; i++) {
        printf("%05d %s %d %.2f %.2f\n", itens[i].id, itens[i].nome, itens[i].qtde, itens[i].unitario, itens[i].total_item);
    }

    // Calcula e imprime o total dos preços de todos os itens
    float totalFinal = 0;
    for(int i = 0; i < numItens; i++) {
        totalFinal += itens[i].total_item;
    }
    printf("\n TOTAL FINAL %.2f\n", totalFinal);

    return 0;
}
