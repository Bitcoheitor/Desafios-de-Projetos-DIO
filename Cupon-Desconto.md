# Descrição

Em algumas promoções de e-commerce, os clientes têm a opção de aplicar cupons de desconto. A missão é criar uma função que calcule o valor final da compra após aplicar um desconto, caso o cupom seja válido. Os cupons disponíveis são "DESCONTO10" (que aplica um desconto de 10%) e "DESCONTO20" (que aplica um desconto de 20%). Se o código do cupom não for válido, o valor da compra permanece inalterado. O resultado deve ser formatado conforme o padrão monetário brasileiro (R$ XX.XX).

## Entrada
A entrada consiste em dois valores:

Um número decimal representando o valor da compra (por exemplo, 100.00).
Uma string representando o código do cupom (por exemplo, "DESCONTO10" ou "DESCONTO20").

## Saída
A saída deve ser uma string no formato:

"Valor final da compra: R$ XX.XX", onde XX.XX é o valor final após o desconto (caso haja).
Exemplos
A tabela abaixo apresenta exemplos com alguns dados de entrada e suas respectivas saídas esperadas. Certifique-se de testar seu programa com esses exemplos e com outros casos possíveis.

| Entrada	| Saída |
| :------: | ----- |
| 100.00 |
| DESCONTO10	| Valor final da compra: R$ 90.00 |
| 200.00 |
| DESCONTO20	| Valor final da compra: R$ 160.00 |
| 150.00 |
| NENHUM	| Valor final da compra: R$ 150.00 |
| 50.00 |
| DESCONTO10	| Valor final da compra: R$ 45.00 |

~~~~
// TODO: Crie uma função chamada calcularDesconto():
function calcularDesconto() {
    // Lê o valor total da compra e o código do cupom
    let valorCompra = parseFloat(gets().trim());
    let cupom = gets().trim();

    // TODO: Calcule o valor final com base no cupom:
    let valorFinal = valorCompra;
    // TODO: Implemente uma condição para aplicação dos descontos de 10% e 20%
    if (cupom === "DESCONTO10") {
        valorFinal = valorCompra * 0.9;
    } else if (cupom === "DESCONTO20") {
        valorFinal = valorCompra * 0.8;
    }

    // TODO: Imprima o valor final com o desconto, formatado para R$:
    // Garante sempre duas casas decimais no formato brasileiro
    let valorFormatado = `R$ ${valorFinal.toFixed(2).replace('.','.')}`;
    print(`Valor final da compra: ${valorFormatado}`);
}
// Chama a função para calcular o desconto
calcularDesconto();
~~~~
