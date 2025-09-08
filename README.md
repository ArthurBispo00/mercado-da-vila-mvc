# Projeto: Gestão do Mercado da Vila (Fases 1 e 2)

Este repositório contém a **Parte 2** do projeto da disciplina de Spring Framework, focada na construção de uma aplicação web completa com interface gráfica (UI) para o sistema de gerenciamento "Mercado da Vila".

---
## 👨‍💻 Integrantes

-   **Arthur Bispo de Lima** - RM: 557568
-   **João Paulo Moreira dos Santos** - RM: 557808

---
##  FASE 2: Aplicação Web com Spring MVC e Thymeleaf (Projeto Atual)

Nesta fase, evoluímos o conceito original de uma API para uma aplicação web interativa e visualmente agradável, permitindo que um usuário gerencie o estoque de produtos diretamente pelo navegador.

### Objetivo
O objetivo foi construir uma interface web (frontend) robusta e intuitiva sobre a base de backend que já havíamos criado. A aplicação permite o controle total do catálogo de produtos através de operações CRUD (Create, Read, Update, Delete) visuais, com botões e formulários, proporcionando uma experiência de usuário completa.

### 🏛️ Arquitetura e Tecnologias
A aplicação segue o padrão **MVC (Model-View-Controller)**, utilizando as seguintes tecnologias:

- **Linguagem:** Java 17
- **Framework:** Spring Boot
- **Interface com o Usuário (View):**
    - **Thymeleaf:** Para conectar os dados do backend Java com as páginas HTML de forma dinâmica.
    - **Bootstrap 5:** Para criar um layout moderno, bonito e responsivo (que funciona em celulares).
- **Controlador (Controller):**
    - **Spring Web MVC (`@Controller`):** Para gerenciar a navegação entre as páginas e responder às ações do usuário.
- **Modelo e Persistência (Model):**
    - **Spring Data JPA & Oracle:** Para mapear os objetos Java para o banco de dados e gerenciar a persistência dos dados.
- **Containerização e Deploy:**
    - **Docker:** Para empacotar a aplicação em um ambiente consistente para testes e deploy.
    - **Render:** Plataforma de nuvem utilizada para hospedar a aplicação online.

---
### 📖 Roteiro de Uso: Um Teste de CRUD Completo

A seguir, demonstramos um fluxo de uso completo da aplicação, cobrindo todas as operações de CRUD (Create, Read, Update, Delete) diretamente pela interface web.

#### **1. Visualizando o Estoque Inicial (Read)**
Ao acessar a aplicação, a primeira tela que vemos é a "Nossa Despensa", que lista todos os produtos atualmente cadastrados no banco de dados. Esta tela representa a operação de **Leitura (Read)** de todos os itens.

---
#### **2. Cadastrando um Novo Produto (Create)**
Vamos adicionar um novo item ao nosso mercado: "Suco de Laranja Natural".

**Ação:**
1.  Na tela principal, clicamos no botão **"Adicionar Novo Produto"**.
2.  Somos direcionados para o formulário de cadastro.
3.  Preenchemos os campos e clicamos em **"Salvar Produto"**.


---
#### **3. Atualizando o Preço do Produto (Update)**
Recebemos uma nova remessa e o preço do suco aumentou. Vamos atualizar o valor.

**Ação:**
1.  Na lista de produtos, encontramos o "Suco de Laranja Natural".
2.  Clicamos no botão **"Editar"** na mesma linha.
3.  Alteramos o campo **Preço** de `12.50` para `13.99` e salvamos.


---
#### **4. Removendo o Produto do Estoque (Delete)**
O lote de "Suco de Laranja Natural" esgotou e não vamos mais vendê-lo.

**Ação:**
1.  Na lista de produtos, encontramos o "Suco de Laranja Natural".
2.  Clicamos no botão **"Excluir"** na mesma linha.


---
### 🔗 Link do Deploy (Parte 2)

A aplicação web está no ar e pode ser acessada através do seguinte link:

**[https://gestao-da-vila.onrender.com/produtos](https://gestao-da-vila.onrender.com/produtos)**

*(Observação: a URL base é `https://gestao-da-vila.onrender.com`, e o caminho `/produtos` leva à página principal da aplicação).*

---
### 🎥 Vídeo Explicativo da Aplicação

Um vídeo de 5 minutos foi produzido para demonstrar todas as funcionalidades da aplicação em tempo real, navegando pela versão em deploy.

**[https://youtu.be/UiaqxHEwJOk](https://youtu.be/UiaqxHEwJOk)**

---
<br>

## FASE 1: API RESTful com Spring Boot (Base do Projeto)

A Parte 2 foi construída sobre a base sólida da **Parte 1**, que consistiu na criação de uma API RESTful pura, sem interface gráfica. Esta API serviu como o "motor" inicial do nosso sistema.

O código-fonte e a documentação completa da Parte 1 estão disponíveis em um repositório separado.

- **Link para o Repositório da Parte 1:** [https://github.com/ArthurBispo00/mercado-da-vila](https://github.com/ArthurBispo00/mercado-da-vila)

### O que foi Feito na Parte 1?
-   Desenvolvimento de endpoints REST para todas as operações CRUD (`GET`, `POST`, `PUT`, `DELETE`).
-   Implementação do nível 3 de maturidade de Richardson com **HATEOAS**.
-   Testes realizados através do **Postman**.
-   Deploy da API na nuvem, respondendo com dados em formato **JSON**.

---
## O que foi atualizado e implementado na Parte 2?

- **✅ Interface Gráfica (UI):** A principal evolução foi a adição de uma camada visual com **Thymeleaf** e **Bootstrap**, transformando a API em uma aplicação web utilizável por qualquer pessoa.
- **✅ Novo Controlador Web:** Foi criado um `ProdutoWebController` (`@Controller`) para gerenciar a renderização das páginas HTML.
- **✅ Experiência do Usuário (UX):** As operações de CRUD agora são feitas de forma intuitiva, através de botões e formulários no navegador.
- **✅ Containerização com Docker:** O projeto foi configurado com um **Dockerfile**, permitindo testes locais consistentes e um processo de deploy mais robusto no Render.
- **✅ Vídeo Demonstrativo:** Foi criado um vídeo de 5 minutos apresentando o fluxo completo de uso da aplicação web online.