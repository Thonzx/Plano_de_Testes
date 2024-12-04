### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste foi validar a funcionalidade de cadastro de usuário, garantindo que:
- Usuários possam se cadastrar corretamente ao preencher todos os campos obrigatórios.
- Mensagens de erro adequadas sejam exibidas para cenários de senhas diferentes e emails já cadastrados.

---

### **2. Escopo**
- Funcionalidade testada: **Cadastro de Usuário**
- Testes realizados:
  - Cadastro bem-sucedido com todos os campos preenchidos.
  - Tentativa de cadastro com senhas diferentes.
  - Tentativa de cadastro com email já existente.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL Workbench  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**                       | **Status** | **Observações**                                                                 |
|--------------------|-----------------------------------------------------|------------|---------------------------------------------------------------------------------|
| CT-02.1            | Cadastro com todos os campos preenchidos            | Falhou     | Redirecionamento não ocorreu. Mensagem "Usuário cadastrado com sucesso!" não exibida. |
| CT-02.2            | Cadastro com senhas diferentes                      | Falhou     | Mensagem "As senhas não coincidem" não exibida.                                |
| CT-02.3            | Cadastro com email já existente                     | Falhou     | Mensagem "Email já cadastrado" não exibida.                                    |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-02.1: Cadastro com Todos os Campos Preenchidos**
- **Descrição:** Testar se o sistema permite cadastro com todos os campos obrigatórios preenchidos corretamente.  
- **Entradas:** 
  - Nome: `João`  
  - Sobrenome: `Silva`  
  - Email: `joao2.silva@teste.com`  
  - Telefone: `999999999`  
  - WhatsApp: `999999999`  
  - Senha: `senha123`  
  - Confirmar Senha: `senha123`  
- **Resultados Esperados:** 
  - Redirecionamento para `/sucesso`.  
  - Mensagem "Usuário cadastrado com sucesso!" exibida.  
- **Resultado Obtido:** Falhou  
- **Evidência:** Cypress indicou que a URL não foi redirecionada, e a mensagem esperada não estava presente.  

---

#### **CT-02.2: Cadastro com Senhas Diferentes**
- **Descrição:** Testar o comportamento do sistema ao tentar cadastrar com senhas diferentes.  
- **Entradas:** 
  - Senha: `senha123`  
  - Confirmar Senha: `senhaErrada`  
- **Resultados Esperados:** 
  - Mensagem "As senhas não coincidem" exibida no formulário de cadastro.  
- **Resultado Obtido:** Falhou  
- **Evidência:** Cypress indicou que a mensagem esperada não foi exibida após o clique no botão de cadastro.  

---

#### **CT-02.3: Cadastro com Email já Existente**
- **Descrição:** Testar o comportamento do sistema ao tentar cadastrar com um email já cadastrado.  
- **Entradas:** 
  - Email: `wellythonsouza105@gmail.com`  
- **Resultados Esperados:** 
  - Mensagem "Email já cadastrado" exibida no formulário de cadastro.  
- **Resultado Obtido:** Falhou  
- **Evidência:** Cypress indicou que a mensagem esperada não foi exibida após o clique no botão de cadastro.
  ![CT_02](https://drive.google.com/uc?export=view&id=1Es9UmJwWqcSj53IKc-TK0vGkg7bM41gL)

---

### **6. Bugs Identificados**

| **ID do Bug** | **Descrição**                                  | **Impacto**      | **Status**       |
|---------------|------------------------------------------------|------------------|------------------|
| BUG-002       | Sistema não redireciona para `/sucesso` após cadastro bem-sucedido. | Alto             | Aberto           |
| BUG-003       | Mensagem "As senhas não coincidem" não exibida quando senhas são diferentes. | Médio            | Aberto           |
| BUG-004       | Mensagem "Email já cadastrado" não exibida para emails duplicados. | Alto             | Aberto           |

---

### **7. Conclusão**
Com base nos testes realizados:
- **Status Geral:** Reprovado  
- O sistema não atendeu aos critérios esperados de funcionalidade para o cadastro de usuários.

---

### **8. Recomendações**
- Verificar o backend para garantir que as validações sejam retornadas corretamente para o frontend.  
- Testar as rotas e exibições das mensagens de erro no frontend.  
- Validar as respostas do banco de dados para emails já cadastrados.  

---
