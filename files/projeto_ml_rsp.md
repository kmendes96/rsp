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

horas,num_traf,dd_mm_aaaa,ds_fs_ff,00:00,00:15,00:30,00:45,01:00,01:15,01:30,01:45,02:00,02:15,02:30,02:45,03:00,03:15,03:30,03:45,04:00,04:15,04:30,04:45,05:00,05:15,05:30,05:45,06:00,06:15,06:30,06:45,07:00,07:15,07:30,07:45,08:00,08:15,08:30,08:45,09:00,09:15,09:30,09:45,10:00,10:15,10:30,10:45,11:00,11:15,11:30,11:45,12:00,12:15,12:30,12:45,13:00,13:15,13:30,13:45,14:00,14:15,14:30,14:45,15:00,15:15,15:30,15:45,16:00,16:15,16:30,16:45,17:00,17:15,17:30,17:45,18:00,18:15,18:30,18:45,19:00,19:15,19:30,19:45,20:00,20:15,20:30,20:45,21:00,21:15,21:30,21:45,22:00,22:15,22:30,22:45,23:00,23:15,23:30,23:45
D1Y1,1048,01/01/2017,DOM,4,2,3,2,2,2,2,2,2,2,2,2,2,7,4,10,7,10,4,10,9,8,9,8,2,3,7,7,7,7,5,4,7,10,9,3,7,2,9,2,6,10,3,2,9,7,5,6,3,9,5,4,7,5,9,6,10,10,9,2,9,7,4,3,10,7,4,10,9,4,10,9,5,2,10,5,10,5,4,2,9,7,7,6,2,5,6,2,9,4,9,8,4,4,4,6
D2Y1,962,02/01/2017,SEG,3,4,5,2,2,2,2,2,2,2,2,2,2,9,7,8,10,8,8,4,2,4,4,7,2,6,8,9,8,6,8,7,7,8,5,8,7,7,4,10,2,6,4,5,3,6,3,2,7,7,5,8,4,3,5,8,7,6,10,9,10,9,10,6,4,10,5,10,4,9,2,4,5,5,3,10,9,4,2,10,6,6,3,2,5,2,9,9,8,10,9,9,4,3,3,10
D3Y1,1150,03/01/2017,TER,2,4,3,2,2,2,2,2,2,2,2,2,2,7,7,5,3,9,10,3,5,3,6,5,5,4,8,10,8,6,8,6,4,10,5,6,8,3,5,7,8,2,8,2,6,5,4,6,8,7,4,6,4,6,6,7,8,3,6,4,2,6,3,5,10,8,8,3,3,3,5,4,4,8,5,3,4,6,3,9,4,8,4,8,6,7,10,8,4,7,7,5,3,3,2,7
D4Y1,685,04/01/2017,QUA,3,4,4,2,2,2,2,2,2,2,2,2,2,2,9,5,5,8,7,8,10,7,4,4,10,2,5,2,4,8,2,9,8,6,10,7,5,5,7,7,8,3,7,9,10,7,9,2,4,10,8,4,10,3,7,9,8,6,6,8,10,3,7,6,10,7,2,10,3,2,2,8,4,5,4,8,6,8,7,5,8,3,4,2,10,6,6,4,6,6,8,10,5,9,8,5

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
