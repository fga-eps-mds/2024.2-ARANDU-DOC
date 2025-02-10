# Planejamento de qualidade

## Histórico de versões

| Versão |   Data   |                Alteração                            |        Responsável              |
| :----: | :------: | :-------------------------------------:             |   :------------------------:    |
| 1.0.0  | 08/12/24 |                 Criação                             | André Corrêa e Gabriel Mariano  |
| 1.0.0  | 09/12/24 |      estruturação do documento                      | André Corrêa |
| 1.1.0  | 09/02/25 |      atualização do documento                      | André Corrêa |

## 1. Introdução

Esse documento visa apresentar o planejamento de qualidade do projeto, explicando como vai ser acompanhado a qualidade durante o semestre.

## 2. Descrição

O objetivo de ser descrito o planejamento de qualidade é para que, desde de o início do desenvolvimento, seja claro o que é a qualidade de software e como ela é avaliada no contexto do nosso projeto.

Para garantir tal qualidade, optou-se por seguir algumas estratégias, dentre elas destacam-se a criação de padrões (para uma maior coerencia) e coleta de 12 métricas de qualidade, essas que sendo coletadas desde o início mostram a evolução do software.

### Criação de padroẽs

Optou-se por criar padroẽs para que haja sempre uma coerencia interna no projeto, isso que auxilia na evolução e integração com outros serviços.

os padrões vão desde nomes de arquivos até a estrutura de requisições.

### Coleta de métricas

Para avaliar a qualidade de forma mais quantitativa, estão sendo coletadas métricas de qualidade oriundas do [Sonarcloud](https://sonarcloud.io/login), além de outras 4 métricas vindas do estudo de Q-rapids. essas métricas são coletas a cada merge na branch 'DEV'

Para que essas métricas possam ser avaliadas, estão sendo utilizados 2 notebooks Jupyter encontrados no repositório de documentação deste projeto. Esses notebooks geram gráficos temporais das métricas coletadas, o que ajuda a acompanhar o projeto com uma visão holística.

### Validação e verificação

A fim de termos garantia do que está sendo realizado, também há algumas etapas de verificação e validação, essas que sempre são realizadas com o Cliente, buscando sempre a satisfação do mesmo.

A cada história desenvolvida, será realizada uma validação com um formulário externo para encontrar possíveis problemas e elogios.

### Testes de software

Também devem ser desenvolvidos diversos testes automatizados de software, para que seja possivel garantir a estabilidade do mesmo com a evolução do sistema.

Serão desenvolvidos testes unitários que devem cubrir ao menos **60%** do código fonte.

Esse documento vai ser evoluído com o desenvolvimento do projeto e estruturação da equipe.

### Notebook de métricas

Depois das coletas de métricas, tem-se a execução dos notebooks jupyter, esses que mostram seis métricas de qualidade, sendo elas relacionadas a confiabilidade e manutenibilidade do projeto. Essas medidas servem para direcionar o desenvolvimento quanto os fatores de qualidade.