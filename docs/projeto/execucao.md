# **Instruções de Execução e Endopoints**

| **Versão** | **Data** | **Modificação** | **Responsável** |
| :-: | :-: | :-: | :-: |
| 0.1 | 09/02/25 | Criação do documento | Gabriel Mariano |

*Tabela 1: Versionamento*

---

## **Introdução**

O projeto é constituído por quatro serviços, sendo cada um destes disponibilizado em um repositório diferente, como pode ser visto abaixo:

- **Aplicativo**: [**2024.2-ARANDU-APP**](https://github.com/fga-eps-mds/2024.2-ARANDU-APP);
- **Front End**: [**2024.2-ARANDU-Frontend**](https://github.com/fga-eps-mds/2024.2-ARANDU-Frontend);
- **User Service**: [**2024.2-ARANDU-UserService**](https://github.com/fga-eps-mds/2024.2-ARANDU-UserService);
- **Studio Maker**: [**2024.2-ARANDU-StudioMaker**](https://github.com/fga-eps-mds/2024.2-ARANDU-StudioMaker).

Este documento visa apresentar uma visão geral relativa à execução dos mesmos, para além de apresentar a forma de acesso ao *Swagger* dos microsserviços responsáveis pelo *back-end* da aplicação, onde estão dispostas as documentações dos *endpoints* destas.

## **Aplicativo**

Inicialmente, clone o repositório em sua máquina:

```bash
git clone https://github.com/fga-eps-mds/2024.2-ARANDU-APP.git
```

Vá para o diretório do repositório:

```bash
cd ./2024.2-ARANDU-APP/
```

Agora, baixe as dependências e tecnologias necessárias para executar o projeto, que envolvem, entre elas, o *Flutter* e o *Android Studio*. Um tutorial para tal pode ser encontrado em: [**Documentação do Flutter**](https://docs.flutter.dev/get-started/install/linux/android). Após instaladas as dependências, rode o seguinte comando:

```bash
flutter run
```

## **Front End**

Inicialmente, clone o repositório em sua máquina:

```bash
git clone https://github.com/fga-eps-mds/2024.2-ARANDU-Frontend.git
```

Vá para o diretório do repositório:

```bash
cd ./2024.2-ARANDU-Frontend/
```

Faça uma cópia do arquivo *.env*:

```bash
cp .env.dev.template .env
```

Preencha as configurações da *.env* com as informações necessárias.

Tendo as ferramentas do *Docker* e *Docker Compose* instaladas, rode o seguinte comando:

```bash
make run
```

## **User Service**

Inicialmente, clone o repositório em sua máquina:

```bash
git clone https://github.com/fga-eps-mds/2024.2-ARANDU-UserService.git
```

Vá para o diretório do repositório:

```bash
cd ./2024.2-ARANDU-UserService/
```

Faça uma cópia do arquivo *.env*:

```bash
cp .env.dev.template .env
```

Preencha as configurações da *.env* com as informações necessárias.

Tendo as ferramentas do *Docker* e *Docker Compose* instaladas, rode o seguinte comando:

```bash
make run
```

## **Studio Maker**

Inicialmente, clone o repositório em sua máquina:

```bash
git clone https://github.com/fga-eps-mds/2024.2-ARANDU-StudioMaker.git
```

Vá para o diretório do repositório:

```bash
cd ./2024.2-ARANDU-StudioMaker/
```

Faça uma cópia do arquivo *.env*:

```bash
cp .env.dev.template .env
```

Preencha as configurações da *.env* com as informações necessárias.

Tendo as ferramentas do *Docker* e *Docker Compose* instaladas, rode o seguinte comando:

```bash
make run
```

## **Swagger**

Para acessar o *Swagger* com a documentação dos *endpoints* nos serviços *User Service* e *Studio Maker*, basta acessar as seguintes rotas (tendo os projetos em execução):

### **User Service**

```
localhost:3000/api
```

### **Studio Maker**

```
localhost:3002/api
```

## **Execução Local**

Para a execução dos serviços localmente, basta seguir as instruções de execução de projetos desenvolvidos em *NextJs* ou *NestJs*. Isto é, com os comandos:

### **Front End**

```bash
npm run dev
```

### **User Service e Studio Maker**

```bash
npm run start:dev
```

## **Possíveis Melhorias**

Uma evolução a ser realizada em todos os arquivos *Dockerfile* de desenvolvimento é a adição do suporte ao *hot reload* nos mesmos.
