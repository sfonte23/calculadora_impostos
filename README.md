# Atividade - Cálculo de Impostos

Este projeto em C# simula o pagamento de impostos para pessoas físicas e jurídicas. O sistema permite inserir informações do cliente, calcular o imposto devido e exibir um resumo da compra, incluindo o valor total a ser pago.

## Funcionalidades

- **Cadastro de Pessoa Física**: Insira nome, endereço, CPF, RG e o valor da compra. O sistema calcula automaticamente o imposto (10% do valor da compra) e exibe o total a pagar.
  
- **Cadastro de Pessoa Jurídica**: Insira nome, endereço, CNPJ, IE e o valor da compra. O imposto é calculado (20% do valor da compra) e o total a pagar é exibido.

## Estrutura do Projeto

- `Clientes.cs`: Classe base para armazenar dados comuns a todos os clientes e calcular o imposto.
- `Pessoa_Fisica.cs`: Herda de `Clientes` e implementa os atributos específicos de Pessoa Física (CPF e RG).
- `Pessoa_Juridica.cs`: Herda de `Clientes` e implementa os atributos específicos de Pessoa Jurídica (CNPJ e IE). Sobrescreve o método para cálculo do imposto com alíquota de 20%.
- `Program.cs`: Contém o método `Main`, responsável por coletar os dados do cliente, calcular o imposto e exibir as informações.

## Tecnologias Utilizadas

- **Linguagem**: C#
- **Framework**: .NET 6.0

## Como Executar

1. Clone o repositório.
2. Compile e execute o projeto utilizando o .NET 6.0 SDK.
3. O programa solicitará as seguintes informações:
   - Nome e endereço do cliente.
   - Tipo de cliente: Pessoa Física ou Jurídica.
   - Para Pessoa Física: CPF, RG e valor da compra.
   - Para Pessoa Jurídica: CNPJ, IE e valor da compra.

Após inserir os dados, o sistema calculará o imposto e exibirá o total a pagar.

## Exemplo de Uso

```
Informar Nome: João Silva
Informar Endereço: Rua das Flores, 123
f - Pessoa Física ou j - Pessoa Jurídica: f
Informe o CPF: 123.456.789-00
Informe o RG: 12.345.678-9
Informe o valor da compra: 100.00

----- Pessoa Física -----
Nome.............: João Silva
Endereço.........: Rua das Flores, 123
CPF..............: 123.456.789-00
RG...............: 12.345.678-9
Valor da Compra..: R$100,00
Imposto..........: R$10,00
Total a Pagar....: R$110,00
```