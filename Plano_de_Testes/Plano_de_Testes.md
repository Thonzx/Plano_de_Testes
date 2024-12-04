## **Plano de Testes**

### **1. Nome do Projeto**
- **Nome:** Bookstore Master
- **Versão do Plano de Testes:** 1.1
- **Data de Criação:** 16.11.2024
- **Data de Revisão:** 21.11.2024
- **Gerente de Testes:** Wellython Salmo
- **Equipe de Testes:** Carlos Breno, Bruna Miranda, Julia Fárias

---

### **1. Escopo e Objetivo**
**Descrição:**
O sistema tem como objetivo facilitar a troca e venda de livros entre usuários, permitindo cadastro, busca, edição e gerenciamento de acervos literários de forma prática e segura. O escopo deste plano de testes é validar todas as funcionalidades principais do sistema, garantindo que ele atenda aos requisitos funcionais e de usabilidade.

---

### **2. Características do Produto a Serem Testadas**
**Funcionalidades a serem testadas:**
- Registro e login de usuários.
- Edição de dados pessoais do usuário.
- Busca de livros por título, autor e categoria.
- Adição e edição de livros.
- Listagem de livros com filtros por categoria.
- Notificações de ações e destaque de livros.
- Remoção de livros do acervo do usuário.

---

### **3. Abordagem a Ser Utilizada**

| **Item**            | **Descrição**                                                                                     |
|----------------------|---------------------------------------------------------------------------------------------------|
| **Objetivo**         | Validar todas as funcionalidades críticas do sistema.                                             |
| **Técnica**          | ( ) Manual (x) Automática                                                                        |
| **Estágio do Teste** | Integração (x) Sistema ( ) Unidade ( ) Aceitação ( )                                              |
| **Abordagem do Teste** | Caixa Branca ( ) Caixa Preta (x)                                                                |
| **Responsável(is)**  | Wellython Salmo, Carlos Breno, Bruna Miranda, Julia Farias                                                               |

**Tipos de Testes:**
- **Testes Funcionais:** Verificar o comportamento esperado das funcionalidades descritas.
- **Testes de Usabilidade:** Garantir que o sistema é intuitivo e de fácil utilização.
- **Ferramentas Utilizadas:** Cypress (automação de testes).

---

### **4. Itens a Serem Testados**
| **Item**                        | **Descrição**                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------|
| **Login:**                       | Testar login com credenciais válidas e inválidas, mensagens de erro e redirecionamento. |
| **Cadastro de Usuário:**         | Validar o fluxo de criação de novos usuários e restrições de dados duplicados.          |
| **Edição de Dados do Usuário:**  | Testar a atualização de informações pessoais.                                           |
| **Busca de Livros:**             | Verificar filtros de busca por título, autor e categoria.                               |
| **Adição e Edição de Livros:**   | Validar formulários de adição e edição, incluindo mensagens de sucesso/erro.            |
| **Listagem de Livros e Filtros:**| Garantir que os filtros organizam os livros corretamente.                               |
| **Notificações e Destaques:**    | Testar notificações e funcionalidade de destaque de livros.                             |
| **Remoção de Livros:**           | Validar permissões e exclusão de livros.                                                |

---

### **5. Cronograma para o Teste**

| **Semana** | **Atividade**                                                   |
|------------|------------------------------------------------------------------|
| Semana 1   | Revisão do plano de testes e configuração do ambiente de testes. |
| Semana 2   | Criação dos scripts de teste automatizados.                      |
| Semana 3   | Execução de testes de login, cadastro e busca de livros.         |
| Semana 4   | Testes de adição, edição e remoção de livros.                    |
| Semana 5   | Validação de listagem, filtros, notificações e destaques.        |
| Semana 6   | Regressão, correção de bugs e avaliação final.                   |

---

### **6. Pessoal Responsável pelas Diferentes Atividades de Teste**

Lista dos testadores responsáveis por cada atividade ou parte do processo de testes.

| **Atividade**                | **Responsável**                |
|-------------------------------|--------------------------------|
| Testes de Login               | Julia Farias                      |
| Testes de Cadastro de Usuário | Julia Farias                     |
| Testes de Edição de Dados     | Julia Farias                     |
| Testes de Busca de Livros     | Carlos Breno                      |
| Testes de Adição de Livros    | Carlos Breno                     |
| Testes de Edição de Livros    | Bruna Miranda                      |
| Testes de Listagem e Filtros  | Wellython Salmo                |
| Testes de Notificações        | Wellython Salmo                    |
| Testes de Remoção de Livros   | Bruna Miranda                      |

---

### **7. Os Riscos Associados aos Testes**

| **Risco**                                   | **Impacto**                                                                                      | **Mitigação**                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Falhas na Integração com o Banco de Dados   | Dados não persistidos corretamente, causando perda de informações.                              | Garantir que o banco de dados esteja configurado corretamente antes de iniciar os testes. |
| Problemas de Conectividade                  | Ambiente de testes não acessível, prejudicando a execução dos cenários automatizados.           | Configurar ambientes locais replicáveis e independentes de conectividade externa.        |
| Escopo Mal Definido                         | Testes podem ser executados sem cobrir todos os casos críticos do sistema.                      | Revisar detalhadamente o plano de testes e validar o escopo com stakeholders.           |
| Equipe Insuficiente                         | Dificuldade para executar todos os testes no prazo definido.                                    | Alocar recursos extras ou revisar prazos e priorizar casos críticos.                    |
| Erros em APIs ou Serviços Externos          | Funcionalidades dependentes de APIs podem não funcionar corretamente durante os testes.         | Simular APIs com ferramentas como Postman ou Mock Server para independência do sistema. |

---

