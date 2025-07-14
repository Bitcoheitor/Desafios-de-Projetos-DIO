## Descrição
Neste desafio, você irá simular um carrinho de compras. O usuário informará quantos produtos ele deseja adicionar ao carrinho e, em seguida, será solicitado que ele insira os nomes desses produtos. O programa deve encerrar automaticamente quando o número de produtos informados for atingido e exibir a lista final de itens no carrinho.

O programa deve se comportar da seguinte forma:

#### 1 - O usuário informa o número de produtos que deseja adicionar ao carrinho.
#### 2 - O programa solicita o nome de cada produto.
Após adicionar o número de produtos indicado, o programa deve exibir a lista final dos produtos no carrinho.

### Entrada
A entrada será composta por dois passos:

O primeiro número será a quantidade de produtos que o usuário deseja adicionar ao carrinho.
Após isso, o programa solicitará os nomes dos produtos, um por um, até que o número de produtos informado seja atingido.
### Saída
O programa deve exibir a lista final de produtos no carrinho no seguinte formato:

### Carrinho final: produto1, produto2
Exemplos
A tabela abaixo apresenta exemplos com alguns dados de entrada e suas respectivas saídas esperadas. Certifique-se de testar seu programa com esses exemplos e com outros casos possíveis.

| Entrada	| Saída |
| :---: | ----- |
| 2 | arroz  |
| 2 | feijão |
#### Carrinho final: arroz, feijão

| Entrada	| Saída |
| :---: | ----- |
| 3 | pão |
| 3 | leite |
| 3 | açúcar |
#### Carrinho final: pão, leite, açúcar

| Entrada	| Saída |
| :---: | ----- |
| 4 | arroz  |
| 4 | feijão  | 
| 4 | macarrão  |
| 4 | sal |
#### Carrinho final: arroz, feijão, macarrão, sal

~~~~
// IMPORTANTE: Na DIO, as funções "gets" e "print" são acessíveis globalmente, onde:
// - "gets": lê UMA linha com dado(s) de entrada (inputs) do usuário;
// - "print": imprime um texto de saída (output) e pula uma linha ("\n") automaticamente.

// O número de produtos a ser adicionado
let numeroDeProdutos = parseInt(gets());

// Crie um array para armazenar os produtos:
let carrinho = [];

// Leia os produtos e os adicione ao carrinho:
for (let i = 0; i < numeroDeProdutos; i++) {
    let produto = gets();
    carrinho.push(produto);
}

// Exiba o carrinho final no formato esperado;
print("Carrinho final: " + carrinho.join(", "));
~~~~
