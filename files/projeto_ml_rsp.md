# Projeto - ML RSP DataLab

O Projeto será desenvolvido com modelo ETL (Extract, Transform, Load) inicialmente nas seguintes etapas:

- Extração
- Transformação
- Carga (load)
- Desenvolvimento do Machine Learning
- Teste e Implementação do Código
- Implementação da interface gráfica para utilização do usuário final


Esse Arquivo deve ser atualizado a cada etapa do projeto.

## Arquitetura / Descrição / Aparência / Formato do DataFrame (DF)

O DataFrame na sua versão final terá aproximadamente um total de 6 meses de dados:
    - 100 colunas
    - 1825 linhas
Os dados serão de 01/01/2023 a 31/05/2023

## Primeiramente iremos buscar um método de extração de dados, utilizando o processo ETL.

ETL é uma sigla em inglês que representa as três fases principais do processo de integração de dados em um sistema de gerenciamento de banco de dados ou em um data warehouse: Extract (Extração), Transform (Transformação) e Load (Carga). É uma abordagem comum para coletar, preparar e carregar dados de várias fontes em um formato consolidado e pronto para análises.

Breve explicação de cada fase do processo ETL:

Extract (Extração): Nesta fase, os dados são coletados de diversas fontes, como bancos de dados, arquivos, APIs ou sistemas externos. Os dados são extraídos dessas fontes e movidos para um ambiente de preparação de dados, geralmente chamado de "área de stage" ou "staging area". A extração pode envolver a leitura de dados brutos ou estruturados, a aplicação de filtros e a validação dos dados para garantir sua integridade.

Transform (Transformação): Após a extração, os dados são transformados para atender aos requisitos de qualidade e integração do sistema de destino. Essa fase pode incluir várias atividades, como limpeza de dados, enriquecimento de dados, padronização de formatos, agregação, normalização, deduplicação e cálculos de derivados. É nesta fase que os dados são preparados para análises e são transformados em um formato adequado para carregamento no sistema de destino.

Load (Carga): Depois de extraídos e transformados, os dados são carregados no sistema de destino, que pode ser um banco de dados, um data warehouse ou outra plataforma de armazenamento. Os dados são inseridos na estrutura de armazenamento apropriada, seja em tabelas, cubos ou outros formatos, para que possam ser acessados e analisados pelos usuários finais.

O processo ETL é fundamental para garantir a integridade, qualidade e consistência dos dados em um sistema de gerenciamento de banco de dados ou data warehouse. Ele permite a coleta, preparação e integração de dados de várias fontes em um formato padronizado e pronto para análises, facilitando a tomada de decisões informadas com base nos dados disponíveis.

Exemplo da Arquitetura Final do DF : https://github.com/cvs2010/rsp/blob/main/files/dataframe_backup.csv

| horas | num_traf | dd_mm_aaaa | ds_fs_ff | 00:00 | 00:15 | 00:30 | ... | 23:30 | 23:45 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| D1Y1 | 1048 | 01/01/2017 | DOM | 4 | 2 | 3 | ... | 2 | 2 |
| D3Y1 | 1001 | 02/01/2017 | SEG | 2 | 2 | 3 | ... | 3 | 2 |
| D2Y1 | 947 | 03/01/2017 | TER | 3 | 2 | 3 | ... | 4 | 4 |

## Com esses dados iremos iniciar o processo de Transformação, onde analisaremos o DF e faremos ajustes de linhas e colunas além de transformação dos dados em códigos int8 int64 , string, etc.

## Por fim, faremos a carga (Load) do DF no google colab para utilizarmos ferramentas de Machine Learning para leitura e aprendizado de máquina.

Após sucesso de no mínimo 90% de rating de acurácia , que é um sucesso razoável, pois o dia tem 24 horas - de 15 em 15 minutos temos 96 colunas, ou seja, um rating de 90% nos dá 86 colunas de previsibilidade correta, sendo que as outras 10 colunas provavelmente a IA errará um peso para cima ou para baixo. Isso dá uma ótima predição a ser utilizada pelo supervisor no dia-a-dia para a distribuição da carga horária da equipe.


Esse Arquivo deve ser atualizado a cada etapa do projeto:
Extração
Transformação
Carga (load)
Desenvolvimento do Machine Learning
Teste e Implementação do Código
Implementação da interface gráfica para utilização do usuário final
