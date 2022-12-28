# Plano de gestão de riscos

## 1. Histórico de versão

| Versão |    Data    |             Comentário             |            Autor(es)            |
| :----: | :--------: | :--------------------------------: | :-----------------------------: |
|  1.0   | 09/12/2022 |        Criação do documento        | Kleidson Alves, Lucas Rodrigues |
|  2.0   | 12/12/2022 |        Classificação do EAR        | Kleidson Alves, Lucas Rodrigues |
|  2.1   | 23/12/2022 | Priorização e prevenção dos riscos | Kleidson Alves, Lucas Rodrigues |

### 2. Resumo

Esse documento busca identificar possíveis riscos que possivelmente o projeto poderá enfrentar, além de analisar e planejar medidas possíveis para mitigar esses riscos uma vez que eles podem causar danos ao desenvolvimento do projeto

### 3. Estrutura Analítica de Riscos (EAR)

EAR é uma ferramenta por meio da qual os riscos apresentados ao projeto são organizados em categorias, sendo que cada categoria pode ser separada em outros níveis para detalhar a fonte do risco para o projeto. Abaixo estão apresentadas as categorias levantadas pela equipe.

![](https://i.imgur.com/OwLS04i.jpg)

### 4. Definições

#### Definição de probabilidade

| Nº  | Probabilidade | % de certeza |
| --- | ------------- | ------------ |
| 1   | Muito Baixa   | 0 a 20%      |
| 2   | Baixa         | 21 a 40%     |
| 3   | Média         | 41 a 60%     |
| 4   | Alta          | 61 a 80%     |
| 5   | Muito Alta    | > 80%        |

#### Definição de impacto

| Impacto     | Descrição                                      | Peso |
| ----------- | ---------------------------------------------- | ---- |
| Muito Baixo | Quase que imperceptível ao projeto             | 1    |
| Baixo       | Pouca influência no desenvolvimento do projeto | 2    |
| Médio       | Notável ao projeto                             | 3    |
| Alto        | Dificulta o desenvolvimento do projeto         | 4    |
| Muito Alto  | Impossibilita o prosseguimento do projeto      | 5    |

### 5. Riscos levantados

| ID  |                     Descrição                      |          Categoria EAR           |  Impacto   | Probabilidade |                                  Consequência                                   |
| :-: | :------------------------------------------------: | :------------------------------: | :--------: | :-----------: | :-----------------------------------------------------------------------------: |
| R01 |         Desistência de um membro da equipe         |         Externo - saúde          |   baixo    |     baixa     |                Aumento da carga de trabalho para outros membros                 |
| R02 |           Dificuldade com as tecnologias           |       Técnico - tecnologia       | muito alto |     média     | Atraso nas entregas, baixa qualidade do produto ou até a não entrega do produto |
| R03 |                Falta de comunicação                |      Gerência - comunicação      | muito alto |     média     |   dificulta a organização da equipe e compromete o desenvolvimento do projeto   |
| R04 |              Divergência de horários               |     Gerência - planejamento      |   médio    |     alta      |            dificulta a aplicação da técnica de programação em pares             |
| R05 |             Instabilidade da internet              | Externo - provedores de serviços |    alto    |  muito baixa  |                Compromete a participação nas reuniões da sprint                 |
| R06 |                 Mudança de escopo                  |     Gerência - planejamento      |    alto    |     média     |        pode resultar em sobrecarga nas sprints realizadas após a mudança        |
| R07 |             Baixa motivação da equipe              |         Externo - saúde          | muito alto |     baixa     |              Atraso na conclusão das tarefas e baixa produtividade              |
| R08 |         Falta de participação nas reuniões         |     Gerência - planejamento      |   médio    |     baixa     |                        Problemas de integração da equipe                        |
| R09 |              Insatisfação do cliente               |        Externo - cliente         | muito alto |  muito baixa  |                     Pode resultar na desmotivação da equipe                     |
| R10 |        Não conclusão das tarefas da sprint         |     Gerência - planejamento      |    alto    |     média     |        pode resultar em sobrecarga nas sprints realizadas após a mudança        |
| R11 |          Adoecimento de membro da equipe           |         Externo - saúde          |   médio    |     média     |                Aumento da carga de trabalho para outros membros                 |
| R12 | Indisponibilidade do cliente para realizar reunião |        Externo - cliente         | muito alto |     média     |            impossibilita a validação do que foi realizado na semana             |

## 6. Priorização dos riscos

### 6.1 Matriz Probabilidade / Impacto

| P / I           | Muito baixo | Baixo | Médio | Alto | Muito alto |
| --------------- | :---------: | :---: | :---: | :--: | :--------: |
| **Muito Baixo** |      1      |   2   |   3   |  4   |     5      |
| **Baixo**       |      2      |   4   |   6   |  8   |     10     |
| **Média**       |      3      |   6   |   9   |  12  |     15     |
| **Alto**        |      4      |   8   |  12   |  16  |     20     |
| **Muito Alto**  |      5      |  10   |  15   |  20  |     25     |

### 6.2. Priorização dos riscos levantados

| Risco | Pontuação na matriz | Prioridade |
| :---: | :-----------------: | :--------: |
|  R01  |          4          |   Baixa    |
|  R02  |         15          |    Alta    |
|  R03  |         15          |    Alta    |
|  R04  |         12          |    Alta    |
|  R05  |          4          |   Baixa    |
|  R06  |         12          |    Alta    |
|  R07  |         10          |    Alta    |
|  R08  |          6          |   Média    |
|  R09  |          5          |   Baixa    |
|  R10  |         12          |    Alta    |
|  R11  |          9          |   Média    |
|  R12  |          8          |   Média    |

## 7. Gerenciamento dos Riscos Priorizados

| ID  |                                               Prevenção                                               |                                                                           Ação                                                                           |
| :-: | :---------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------: |
| R02 |                      Realização de dojos para o compartilhamento de conhecimento                      | Estudo e pesquisa sobre as tecnologias a serem utilizadas. Pareamento para desenvolvimento da tarefa. Ajuda dos membros que conhecem melhor a tecnologia |
| R03 |         Definição de data e horário das reuniões, bem como dos meios de comunicação da equipe         |                                                      Reavaliar o processo de comunicação em equipe                                                       |
| R06 |                                                   -                                                   |                                                                Adaptação do planejamento                                                                 |
| R10 |                                    Planjeamento realista da sprint                                    |                                Adaptar o planejamento da próxima sprint para encaixar a realização das tarefas pendentes                                 |
| R04 |                           Criação e análise do quadro de horários da equipe                           |                                                           Realização das tarefas em pareamento                                                           |
| R07 |                                    Criar um ambiente descontraído                                     |                                          Ajudar membros que estiverem com dificuldade na realização das tarefas                                          |
| R11 |                                                   -                                                   |                                                           Redistribuição das tarefas da sprint                                                           |
| R12 |                                                   -                                                   |                                        Remarcar o dia e horário da reunião. Comunicação assíncrona com o cliente                                         |
| R08 | Definição de data e horário das reuniões. Encorajar a participação dos membros da equipe nas reuniões |                                                       Constante comunicação por meios assíncronos                                                        |
| R09 |                                          Entregas constantes                                          |                                               Boa comunicação com o cliente e alinhamento de expectativas                                                |
| R01 |                                                   -                                                   |                                                 Redistribuição de atividades dentro do escopo do projeto                                                 |
| R05 |                                                   -                                                   |                                                         Alterar horário de realização da tarefa                                                          |

## Referências

Gerência de riscos em desenvolvimento de software. Disponível em: https://www.devmedia.com.br/gerencia-de-riscos-em-desenvolvimento-de-software/28506. Acesso em: 23/12/2022

Objetivo do Plano de gerenciamento dos riscos. Disponível em:
https://escritoriodeprojetos.com.br/downloads/send/8-modelos/129-plano-de-gerenciamento-dos-riscos. Acesso em: 23/12/2022
