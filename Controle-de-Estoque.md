# Descrição
Você está simulando um controle simples de estoque. O sistema começa com um estoque inicial de 5 unidades.

O usuário pode escolher entre duas opções:
#### 1 - Adicionar uma quantidade ao estoque.
#### 2 - Retirar uma quantidade do estoque.
O sistema realiza a operação e exibe o estoque atualizado. Caso o usuário tente retirar uma quantidade maior do que o estoque disponível, o sistema deve exibir a mensagem Estoque insuficiente e manter o estoque inalterado.

## Entrada
A entrada será composta por dois números inteiros, na seguinte ordem:

O primeiro número representa a operação desejada:
1 para adicionar ao estoque.
2 para retirar do estoque.
O segundo número representa a quantidade da operação.

## Saída
O programa deve exibir uma das seguintes saídas:

O estoque atualizado após a operação.
Ou a mensagem Estoque insuficiente, caso a tentativa de retirada seja maior que o estoque atual.
Exemplos
A tabela abaixo apresenta exemplos com alguns dados de entrada e suas respectivas saídas esperadas. Certifique-se de testar seu programa com esses exemplos e com outros casos possíveis.

| Entrada	| Saída |
| :-----: |  -----  |
| 1  |	8  |
| 3  |	8  |
| 2 | 1  |
| 4 | 1  |
| 2 |  Estoque insuficiente |	
| 6 |  Estoque insuficiente |	  
| 1 |	10  |
| 5 |	10  |

~~~~
// IMPORTANTE: Na DIO, as funções "gets" e "print" são acessíveis globalmente, onde:
// - "gets": lê UMA linha com dado(s) de entrada (inputs) do usuário;
// - "print": imprime um texto de saída (output) e pula uma linha ("\n") automaticamente.

let operacao = parseInt(gets());
let quantidade = parseInt(gets());

let estoque = 5;

// Verifica se a operação é para adicionar ao estoque (1)
if (operacao === 1) {
    estoque += quantidade;
    print(estoque);
}
// Se a operação for para retirar do estoque (2)
else if (operacao === 2) {
    // Se a quantidade a ser retirada for maior que o estoque disponível, exibe mensagem de erro
    if (quantidade > estoque) {
        print("Estoque insuficiente");
    } else {
        // Caso contrário, retira a quantidade do estoque e exibe o valor atualizado
        estoque -= quantidade;
        print(estoque);
    }
}
~~~~
