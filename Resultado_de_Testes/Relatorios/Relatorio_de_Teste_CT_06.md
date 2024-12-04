### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste foi verificar a funcionalidade de edição de livros no sistema, garantindo que apenas os usuários proprietários possam editar seus livros e que as alterações realizadas sejam salvas corretamente no banco de dados.

---

### **2. Escopo**
- **Funcionalidade testada:** Edição de Livro  
- **Testes realizados:**
  - Edição bem-sucedida de um livro existente.
  - Validação de permissão ao tentar editar livros de outros usuários.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**                  | **Status** | **Observações**                                   |
|--------------------|------------------------------------------------|------------|--------------------------------------------------|
| CT-06.1            | Editar livro "O Senhor dos Anéis" com sucesso | Falhou     | Livro não encontrado (erro 404).                |
| CT-06.2            | Tentar editar livro de outro usuário          | Falhou     | Livro não encontrado (erro 404).                |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-06.1: Editar Livro "O Senhor dos Anéis" com Sucesso**
- **Descrição:** Verificar se o sistema permite editar o título de um livro de propriedade do usuário autenticado.
- **Entradas:** 
  - Título: "O Senhor dos Anéis - Edição Atualizada"
- **Resultados Esperados:**  
  - Alteração salva com sucesso.  
  - Exibição da mensagem "Alterações salvas com sucesso".  
- **Resultados Obtidos:**  
  - **Status:** Falhou  
  - **Observação:** O sistema retornou um erro 404 ao acessar a página de edição.  

#### **CT-06.2: Tentar Editar Livro de Outro Usuário**
- **Descrição:** Verificar se o sistema impede a edição de livros que não pertencem ao usuário autenticado.
- **Entradas:**  
  - Acessar o livro com ID 2, pertencente a outro usuário.  
- **Resultados Esperados:**  
  - Exibição da mensagem "Você não tem permissão para editar este livro".  
- **Resultados Obtidos:**  
  - **Status:** Falhou  
  - **Observação:** O sistema retornou um erro 404 ao acessar a página de edição.
    - **Evidências:**
    ![Descrição da Imagem](https://drive.google.com/uc?export=view&id=1gZ321jGvGezc-mJ0YdUq3RO-_zFH2b3N)


---

### **6. Bugs Identificados**

| **ID do Bug** | **Descrição**                                       | **Impacto** | **Status** |
|---------------|-----------------------------------------------------|-------------|------------|
| BUG-006.1     | A página de edição do livro "O Senhor dos Anéis" não foi encontrada. | Alto        | Aberto     |
| BUG-006.2     | A página de edição de livros de outros usuários não foi encontrada. | Médio       | Aberto     |

---

### **7. Conclusão**
Os testes realizados para a funcionalidade de edição de livros falharam. O sistema retornou erro 404 ao acessar as páginas de edição. Isso pode indicar problemas na configuração das rotas ou permissões inadequadas no backend.  

**Status Geral:** Reprovado  

---

### **8. Recomendações**
1. Verificar a configuração das rotas no backend para garantir que as páginas de edição de livros estão acessíveis.
2. Implementar verificações adicionais para identificar se os IDs de livros são válidos e pertencem ao usuário autenticado.
3. Realizar testes adicionais após corrigir os erros para validar as alterações realizadas.

--- 
