
### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias.  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste é validar as funcionalidades de edição de dados do usuário, incluindo a atualização de informações pessoais, alteração de senha e a validação de erro ao inserir senhas incompatíveis.

---

### **2. Escopo**
- Funcionalidade testada: **Edição de Dados do Usuário**
- Testes realizados:
  - Atualização dos dados pessoais.
  - Alteração de senha.
  - Validação de erro ao inserir senhas incompatíveis.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**              | **Status**  | **Observações**                                              |
|--------------------|---------------------------------------------|-------------|-------------------------------------------------------------|
| CT-07.1            | Atualizar os dados pessoais do usuário      | Falhou      | A mensagem de sucesso não foi exibida, e o campo "nome" estava bloqueado pela navbar. |
| CT-07.2            | Alterar a senha do usuário                  | Falhou      | A mensagem "Senha alterada com sucesso" não foi exibida.    |
| CT-07.3            | Exibir erro ao inserir senhas incompatíveis | Passou      | Mensagem "As senhas não coincidem" foi exibida corretamente.|

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-07.1: Atualizar os dados pessoais do usuário**
- **Descrição:** Testar se o sistema permite atualizar informações pessoais do usuário com dados válidos.
- **Entradas:** 
  - Nome: "Wellython Atualizado"
  - Sobrenome: "Souza Atualizado"
  - E-mail: "wellythonsouza105_atualizado@gmail.com"
  - Telefone: "92995338752"
  - WhatsApp: "92995338752"
- **Resultados Esperados:** Redirecionamento para "Meus Livros" com mensagem "Dados atualizados com sucesso".
- **Resultado Obtido:** Falhou
- **Evidência:** Campo "nome" estava bloqueado pela navbar, impossibilitando a edição.

---

#### **CT-07.2: Alterar a senha do usuário**
- **Descrição:** Testar se o sistema permite alterar a senha do usuário.
- **Entradas:** 
  - Nova senha: "novaSenha123"
  - Confirmação de senha: "novaSenha123"
- **Resultados Esperados:** Mensagem "Senha alterada com sucesso" exibida após a ação.
- **Resultado Obtido:** Falhou
- **Evidência:** Mensagem esperada não foi exibida.

---

#### **CT-07.3: Exibir erro ao inserir senhas incompatíveis**
- **Descrição:** Testar se o sistema exibe erro ao inserir senhas incompatíveis.
- **Entradas:** 
  - Nova senha: "novaSenha123"
  - Confirmação de senha: "senhaErrada"
- **Resultados Esperados:** Mensagem "As senhas não coincidem" exibida.
- **Resultado Obtido:** Passou
- **Evidência:** Mensagem de erro exibida corretamente.

---

### **6. Bugs Identificados**

| **ID do Bug** | **Descrição**                                 | **Impacto** | **Status** |
|---------------|-----------------------------------------------|-------------|------------|
| BUG-002       | Campo "nome" bloqueado pela navbar no formulário de edição de usuário. | Alto        | Aberto     |
| BUG-003       | Mensagem "Senha alterada com sucesso" não exibida após atualização bem-sucedida. | Médio       | Aberto     |

---

### **7. Conclusão**
Com base nos testes realizados:
- **Status Geral:** Reprovado  
- Apenas o caso de teste **CT-07.3** passou com sucesso. Os outros casos falharam devido a bugs identificados.

---

### **8. Recomendações**
- Corrigir o posicionamento da navbar para não bloquear campos do formulário.
- Garantir que as mensagens de sucesso sejam exibidas após ações bem-sucedidas.
- Realizar novos testes após as correções para validar o comportamento esperado.

---
