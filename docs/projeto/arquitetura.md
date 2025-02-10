# Documentação de Arquitetura

## Versionamento

| **Versão** | **Data** | **Modificação** | **Responsável** |
| :-: | :-: | :-: | :-: |
| 0.1 | 09/12/24 | Criação do documento | Gabriel Mariano |
| 1.0 | 09/12/24 | atualização do documento | André Corrêa |
| 2.0 | 20/12/24 | atualização do documento | André Corrêa |
| 2.1 | 09/02/25 | atualização do documento | André Corrêa |

*Tabela 1: Versionamento*

---

## Objetivo

A documentação de arquitetura visa apresentar uma visão técnica da estutura organizacional do produto de software a ser desenvolvido, apresentando elementos como o *stack* da aplicação, a organização dos serviços, a estrutura da camada de persistência, os *endpoints* definidos e também instruções para a execução do projeto.

## Stack

Foram definidas as seguintes tecnologias para o projeto:

| **Tecnologia** | **Serviço (s)** | **Objetivo** |
| :-: | :-: | :-: |
| *NestJs* | UserService e StudioMaker | Back-End do Sistema |
| *NextJs* | FrontEnd | Front-End do Sistema |
| *Flutter* | APP | Aplicativo Móvel |
| *Swagger* | UserService e StudioMaker | Documentação das Rotas do Back-End |
| *Docker* | UserService, StudioMaker e FrontEnd | Conteinerização da Aplicação |

*Tabela 2: Stack do Sistema*

## Representação Arquitetural

### Diagrama de Relações

<iframe frameborder="0" style="width:100%;height:308px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio&page-id=I-6fpici55m38HMQ_MQw#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>
**Autor:** Calculus Team 2024.1

A arquitetura de microsserviços adotada no *Arandu* segue uma abordagem onde a aplicação é composta por serviços menores, implementados de forma independente e com baixo acoplamento. Esses serviços, organizados por domínios de negócios, comunicam-se entre si, principalmente por meio de APIs. Essa arquitetura promove um desenvolvimento mais ágil e facilita a escalabilidade da aplicação. Cada microsserviço possui sua própria base de dados independente, assegurando isolamento e robustez.

### Serviços

#### User Service

O *User Service* é responsável pela gestão completa dos usuários da aplicação. Suas funcionalidades incluem registro, autenticação, atualização de informações, gerenciamento de permissões e controle de acesso, garantindo uma experiência segura e personalizada para cada usuário.

#### Studio Maker Service

O *Studio Maker Service* é responsável pela criação e gestão de conteúdo na plataforma. Esse serviço lida com todas as funcionalidades necessárias para que os usuários autenticados possam criar, editar e organizar conteúdos de forma eficiente, permitindo uma gestão eficaz do material disponibilizado na plataforma.

#### Front-end

O *Front-end* é responsável pela interface visual do usuário com o sistema de forma WEB, permitindo toda a interação necessária, como visualização e edição de dados.

#### APP

O *APP* é responsável pela interface visual do usuário com o sistema de forma mobile, permitindo toda a interação necessária, como visualização e edição de dados.

## Visão Lógica

### Diagrama de Pacotes

#### Introdução

O Diagrama de Pacotes organiza as classes do projeto em grupos lógicos chamados pacotes, oferecendo uma visão de alto nível especialmente útil em sistemas complexos. No *Arandu*, seguimos uma arquitetura de microsserviços, onde o pacote principal representa o sistema. Dentro dele, a camada de front-end realiza requisições que são processadas pela camada de back-end, composta pelos microsserviços principais: *User Service*, *Studio Maker Service* e *Gamification Service*, que interagem com os bancos de dados para armazenamento e recuperação de dados.

<iframe frameborder="0" style="width:100%;height:553px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>


**Autor:** *Calculus* Team 2024.1

### Diagrama de Implantação

O Diagrama de Implantação oferece uma visão detalhada de como os componentes do sistema *Arandu* estão distribuídos em diferentes máquinas ou servidores dentro da infraestrutura de TI. Ele demonstra como os serviços são implantados em contêineres, como a comunicação ocorre entre eles e como os dados são armazenados e acessados.

No *Arandu*, a implantação é realizada com o auxílio de contêineres Docker, orquestrados pelo Kubernetes. Esta abordagem garante que cada serviço, como o *User Service* e o *Studio Maker Service*, possa ser escalado de forma independente, mantendo a alta disponibilidade e eficiência operacional. Além disso, o Kubernetes gerencia a distribuição de cargas de trabalho e proporciona resiliência, assegurando que os serviços permaneçam acessíveis mesmo em caso de falhas.

<iframe frameborder="0" style="width:100%;height:513px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio&page-id=nR3126rXf9x62OpuHPoS#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>


**Autor:** *Calculus* Team 2024.1

### Diagrama de Arquitetura
O Diagrama de Arquitetura mostra a estrutura planejada do projeto Arandu, enfatizando a arquitetura de microsserviços. Ele destaca a individualização dos bancos de dados NoSQL para cada serviço, o que garante maior robustez e organização. Cada microsserviço opera de forma independente, permitindo escalabilidade e flexibilidade no desenvolvimento e na manutenção do sistema. A comunicação entre os microsserviços ocorre diretamente, sem a necessidade de um ponto de entrada centralizado.

<iframe style="border:none" width="1600" height="900" src="https://whimsical.com/embed/Ltup7BCojXTtkku7Hzi4V2"></iframe>
 
**Autor:** *Calculus* Team 2024.2

## Deploy

O *deploy* da aplicação foi realizado na plataforma **Render** e pode ser encontrado [NESSE LINK](https://arandu.onrender.com/).

## Documentação Anterior

Por se tratar de um sistema legado de outra equipe de desenvolvimento, grande parte da documentação de arquitetura foi reaproveitada do semestre anterior e pode ser encontrada em sua originalidade na [Documentação de Arquitetura do Projeto Calculus 2024-1](https://fga-eps-mds.github.io/2024.1-CALCULUS-DOC/organizacoes/documento_arquitetura/).

## Referências Bibliográficas

> [1] EQUIPE ALECTRION 2022-2. Documento de Arquitetura. Disponível em: https://fga-eps-mds.github.io/2022-2-Alectrion-DOC/#/./Documentos/arquitetura.  
> [2] SOARES, João Pedro; ESTANISLAU, Matheus. Documento de Arquitetura. Disponível em: https://fga-eps-mds.github.io/2022-1-Alectrion-DOC/documentation/Documentos/documento-arquitetura.html.