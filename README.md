Arquitetura do Framework para Sorteios de Negativados

1. Camadas Principais

Camada de Apresentação (Frontend)

Interface Web (Streamlit ou Flask)

Dashboard para visualizar sorteios e estatísticas

Camada de Aplicação (Backend)

Gerenciamento do baralho e sorteios

Lógica de cálculo de desconto e atualização de dívida

Camada de Persistência (Banco de Dados)

Armazenamento das pessoas negativadas e seus dados financeiros

Registro dos sorteios e descontos aplicados

Fluxo do Sistema

Cadastro de Pessoas

Inserção de novos usuários negativados no banco de dados.

Informações armazenadas: Nome, CPF, Valor da Dívida.

Execução do Sorteio

Seleção aleatória de uma pessoa negativada.

Sorteio de um desconto aleatório do baralho de descontos.

Aplicação do Desconto

Cálculo do novo valor da dívida após o desconto.

Registro do sorteio no banco de dados.

Exibição do Resultado

Visualização via interface gráfica ou API.

Possível envio de notificação ao usuário.

+----------------------------------------------------------+
|                     Interface Web (Flask/Streamlit)      |
|          - Exibe sorteios e estatísticas                |
|          - Permite cadastro de negativados              |
+---------------------------+-----------------------------+
                            |
                            v
+---------------------------+-----------------------------+
|                     Backend (Python)                    |
| - Gerencia sorteios e lógica de descontos               |
| - Calcula novo valor da dívida                          |
| - Expõe API para frontend (caso necessário)             |
+---------------------------+-----------------------------+
                            |
                            v
+----------------------------------------------------------+
|                     Banco de Dados (PostgreSQL/MySQL)    |
| - Tabela de pessoas negativadas                         |
| - Tabela de sorteios realizados                         |
| - Registro de históricos de desconto                    |
+----------------------------------------------------------+

