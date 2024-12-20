

### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste foi validar a funcionalidade de remoção de livros no sistema, verificando os seguintes cenários:
- Remoção bem-sucedida de um livro existente.
- Garantia de que livros removidos não apareçam na lista de livros do usuário.
- Impedimento da remoção de livros pertencentes a outros usuários.

---

### **2. Escopo**
- **Funcionalidade testada:** Remoção de Livros  
- **Testes realizados:**
  - Remoção de um livro pertencente ao usuário autenticado.
  - Verificação da ausência do livro removido na lista de livros do usuário.
  - Validação de erro ao tentar remover um livro que pertence a outro usuário.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**                                    | **Status** | **Observações**                                   |
|--------------------|------------------------------------------------------------------|------------|--------------------------------------------------|
| CT-09.1            | Remover um livro existente                                     | Aprovado   | O livro foi removido com sucesso.               |
| CT-09.2            | Verificar se o livro removido não aparece mais na lista        | Aprovado   | O livro não aparece mais na lista de "Meus Livros". |
| CT-09.3            | Impedir a remoção de um livro que não pertence ao usuário      | Reprovado  | O sistema permitiu a remoção retornando `200 OK` em vez de `403 Forbidden`. |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-09.1: Remover um Livro Existente**
- **Descrição:** Verificar se o sistema permite que o usuário autenticado remova um livro de sua propriedade.
- **Entradas:** Ação de remoção no primeiro livro listado.
- **Resultados Esperados:**  
  - Livro removido com sucesso.  
  - Exibição da mensagem "Livro removido com sucesso".  
- **Resultados Obtidos:**  
  - **Status:** Aprovado  
  - **Observação:** A funcionalidade de remoção foi executada corretamente, e a mensagem foi exibida.  

---

#### **CT-09.2: Verificar se o Livro Removido Não Aparece Mais na Lista**
- **Descrição:** Garantir que o livro removido não aparece mais na lista de livros do usuário.
- **Entradas:** Lista de "Meus Livros".
- **Resultados Esperados:**  
  - O livro removido não aparece mais na lista de "Meus Livros".  
- **Resultados Obtidos:**  
  - **Status:** Aprovado  
  - **Observação:** O livro foi corretamente removido da interface.  

---

#### **CT-09.3: Impedir a Remoção de Livro que Não Pertence ao Usuário**
- **Descrição:** Validar se o sistema impede a remoção de livros que não pertencem ao usuário autenticado.
- **Entradas:** Requisição para remover o livro com ID `999`, pertencente a outro usuário.
- **Resultados Esperados:**  
  - Resposta do backend com status `403 Forbidden`.  
  - Mensagem de erro "Você não tem permissão para remover este livro".  
- **Resultados Obtidos:**  
  - **Status:** Reprovado  
  - **Observação:** A requisição retornou `200 OK`, permitindo a remoção. Isso indica uma falha no controle de permissões no backend.  
- **Evidências:**
  ![CT_09](https://drive.google.com/uc?export=view&id=1-LEK2_OYXLM4_Fi1gmMVZ28kty85IDQU)

  
---

### **6. Bugs Identificados**

| **ID do Bug** | **Descrição**                                       | **Impacto** | **Status** |
|---------------|-----------------------------------------------------|-------------|------------|
| BUG-009.1     | O sistema permitiu a remoção de um livro que não pertence ao usuário autenticado. | Alto        | Aberto     |

---

### **7. Conclusão**
Os testes realizados demonstraram que a funcionalidade de remoção de livros opera corretamente para livros pertencentes ao usuário, mas falha ao validar permissões para remoção de livros de outros usuários. O controle de permissões no backend não está funcionando conforme esperado, permitindo ações indevidas.

**Status Geral:** Reprovado  

---

### **8. Recomendações**
1. Revisar a lógica de validação de permissões no backend para garantir que apenas o proprietário de um livro possa removê-lo.
2. Adicionar testes unitários e de integração para validar o comportamento esperado do backend.
3. Garantir que o frontend exiba mensagens claras e consistentes em caso de falha nas permissões.

---
