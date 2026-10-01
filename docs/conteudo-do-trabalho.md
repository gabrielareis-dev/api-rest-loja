# I Love Donuts - Desenvolvimento Web Back-End

## 1. Descrição do estudo de caso

A I Love Donuts é uma loja especializada na produção e venda de donuts artesanais. Para organizar e automatizar o controle básico das vendas, foi desenvolvido um sistema para gerenciamento de clientes, produtos e pedidos.

A cliente Gabriela Loura Falcão Reis, RU 5174948, realizou seu cadastro no sistema. O produto principal da loja é o Donut de Glacê Rosa, vendido por R$ 8,50 a unidade e disponível em estoque. Em determinado momento, Gabriela realizou um pedido de 3 unidades. O sistema registrou o cliente, o produto e a quantidade solicitada.

## 2. Diagrama de caso de uso

O arquivo editável [diagrama-casos-de-uso.puml](diagrama-casos-de-uso.puml) representa o ator Usuário da API e as operações de cadastro, listagem, consulta por ID e remoção para as três entidades. Renderize o arquivo no PlantUML e inclua a imagem nesta seção do PDF final.

## 3. Especificação da API

### Cliente

| Campo | Tipo | Descrição |
|---|---|---|
| id | Long | Identificador gerado pelo banco |
| nome | String | Nome completo, incluindo RU no cenário |
| clienteDesde | LocalDate | Data do cadastro (formato ISO `AAAA-MM-DD`) |

### Produto

| Campo | Tipo | Descrição |
|---|---|---|
| id | Long | Identificador gerado pelo banco |
| nome | String | Nome do produto |
| preco | BigDecimal | Preço unitário |
| estoque | Boolean | Disponibilidade em estoque |

### Pedido

| Campo | Tipo | Descrição |
|---|---|---|
| id | Long | Identificador gerado pelo banco |
| clienteId | Long | ID do cliente cadastrado |
| produtoId | Long | ID do produto cadastrado |
| quantidade | Integer | Quantidade comprada (maior que zero) |

### Endpoints implementados

| Método e rota | Operação |
|---|---|
| `POST /clientes` | Cadastra cliente |
| `GET /clientes` | Lista clientes |
| `GET /clientes/{id}` | Consulta cliente por ID |
| `DELETE /clientes/{id}` | Remove cliente |
| `POST /produtos` | Cadastra produto |
| `GET /produtos` | Lista produtos |
| `GET /produtos/{id}` | Consulta produto por ID |
| `DELETE /produtos/{id}` | Remove produto |
| `POST /pedidos` | Registra pedido com cliente, produto e quantidade |
| `GET /pedidos` | Lista pedidos |
| `GET /pedidos/{id}` | Consulta pedido por ID |
| `DELETE /pedidos/{id}` | Remove pedido |

## 4. Evidências do Postman

Após iniciar a API e executar as requisições da coleção `postman/I-Love-Donuts.postman_collection.json`, inserir capturas reais do Postman que mostrem:

1. POST Cliente, POST Produto e POST Pedido com os dados do caso.
2. GET geral de Cliente, Produto e Pedido.
3. GET por ID de Cliente, Produto e Pedido.
4. DELETE bem-sucedido de Cliente, Produto e Pedido.

As capturas são requisito obrigatório do enunciado e precisam ser produzidas no Postman após as chamadas. Não foram substituídas por imagens simuladas.

## 5. Repositório

Inserir aqui o link do repositório GitHub ou similar após publicar o código-fonte.
