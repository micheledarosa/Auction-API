# 🔨 Auction API

Desenvolvimento de uma aplicação back-end em C# com .NET realizada durante o evento NLW Expert da [Rocketseat](https://www.rocketseat.com.br). 

![Imgur](https://i.imgur.com/N0TaeBP.png)

O projeto trata-se de uma API para leilões, onde foi aplicado os conceitos de:
- Controladores, Entidades, Repositórios e Casos de uso
- DB Browser for SQLite pra visualização do banco de dados
- Uso do ORM Entity Framework para traduzir entidade em query
- Criação de testes unitários com dados mockados e gerados com Moq e Bogus

## 💠 Endpoints utilizados:

### GET

Usado para recuperar dados, onde o objetivo desse endpoint é obter o leilão atual.

Pode retornar um objeto do tipo Auction com o código de _status 200 (OK)_ e também um código de _status 204 (No Content)_ caso não haja leilão atual.

<table>
    <tr>
        <td>
            <img src="https://i.imgur.com/tGH1R1u.jpg" alt="HTTP Cat status 200(OK)">
        </td>
        <td>
            <img src="https://i.imgur.com/FrcFySF.jpg" alt="HTTP Cat status 204(No Content)">
        </td>
    </tr>
</table>

### POST

Usado para criar novos recursos no servidor, passando o ID do item e os dados da oferta como parâmetros. Isso executa a lógica de negócios para criar uma nova oferta relacionada ao item especificado.

Se a oferta for criada com sucesso, o método retorna um código de _status 201 (Created)_.

<img height="250" src="https://http.cat/images/201.jpg" alt="HTTP Cat status 201(Created)">

## 👨‍🚀 Postman

Para testar e interagir com a minha API durante o desenvolvimento, utilizei o [Postman](https://www.postman.com), uma ferramenta que permite enviar solicitações HTTP para endpoints da API. Assim pude garantir que a autenticação estivesse funcionando corretamente.

O token para teste foi gerado utilizando o site [Base64Enconde.org](https://www.base64encode.org/pt/)

![Imgur](https://i.imgur.com/cev5hFb.png)

## 🗃️ SQLite

O DB Browser for SQLite é uma ferramenta valiosa para visualização, análise e gerenciamento de bancos de dados.

![Imgur](https://i.imgur.com/v99Cjza.png)

## 🧪 Testes unitários

Para finalizar o projeto, foram criados testes unitários com xUnit para garantir o correto funcionamento das diferentes partes do código.

Foram utilizados dados mockados gerados com as bibliotecas Moq e Bogus, e asserções mais expressivas foram escritas com a biblioteca FluentAssertions.

### 📘 Moq 

Moq é uma biblioteca de mocking para .NET que permite criar objetos simulados (mocks) de interfaces e classes.

- Ajuda a isolar o código sob teste de suas dependências reais.
- Facilita a criação de testes unitários mais focados e confiáveis.

### 📙 Bogus

Bogus é uma biblioteca para geração de dados fictícios (mock data) em C#. 

- Permite definir regras para a geração de dados, como faixas de valores ou padrões de texto.
- Facilita a criação de dados de teste variados e realistas.

### 📗 FluentAssertions

FluentAssertions é uma biblioteca de asserções para testes unitários em .NET que fornece uma sintaxe fluente e legível para escrever asserções.

- Ajuda a escrever testes mais claros e concisos.
- Melhora a legibilidade e manutenibilidade do código de teste.

![Imgur](https://i.imgur.com/ckXD4oE.png)