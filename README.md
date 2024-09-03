# 📝 Filtrando Inadimplentes

Este projeto tem como objetivo filtrar apenas clientes inadimplentes de uma listagem com todas as vendas realizadas que está em formato HTML, cruzando os dados com uma planilha de logins para identificar o setor cada cliente inadimplente pertence. O resultado final é exportado em formato Excel.

## 🛠️ Estrutura do Projeto

1. **📚 Importação de Bibliotecas**:
   - O projeto utiliza a biblioteca `pandas` para manipulação e análise de dados.

2. **📂 Importação de Dados**:
   - **🔐 Logins**: A planilha contendo os logins dos vendedores é importada de uma planilha do Google Sheets.
   - **📑 Inadimplentes**: A base de dados de inadimplentes é importada de um arquivo HTML.

3. **⚙️ Processamento dos Dados**:
   - Verifica-se a quantidade de tabelas na base de inadimplentes.
   - Seleciona-se a tabela correspondente às viagens.
   - Realiza-se limpeza de dados, removendo linhas e colunas desnecessárias.
   - Cria-se um `merge` entre a base de inadimplentes e a planilha de logins para associar cada vendedor ao seu setor.
   - Remove-se linhas sem setor, que representam transações incompletas.

4. **🔍 Validação e Reorganização**:
   - Verifica-se se a data mais recente na base de dados corresponde à data atual.
   - As colunas são reorganizadas em uma ordem específica.

5. **💾 Exportação**:
   - O resultado final é exportado para um arquivo Excel (`inadimplentes_atual.xlsx`).

## 🚀 Como Usar

1. **🔧 Configuração Inicial**:
   - Certifique-se de que todas as bibliotecas necessárias estejam instaladas (`pandas`).
   - Insira o `ID` da planilha do Google Sheets na variável `sheet_id`.

2. **▶️ Execução do Código**:
   - Execute cada célula do notebook na sequência, seguindo as instruções fornecidas.

3. **📤 Saída**:
   - O arquivo final com os inadimplentes filtrados será salvo como `inadimplentes_atual.xlsx` no diretório de trabalho.

## 💡 Observações

- O código foi desenvolvido para ser executado no Google Colab, mas pode ser adaptado para outros ambientes Python.
- Certifique-se de que o arquivo HTML e a planilha do Google Sheets estejam devidamente acessíveis e formatados conforme as expectativas do código.
