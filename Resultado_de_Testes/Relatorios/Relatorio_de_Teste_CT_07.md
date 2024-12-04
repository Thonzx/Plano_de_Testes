### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste foi verificar a funcionalidade de listagem e filtros de livros no sistema, assegurando que a lista completa de livros seja exibida, que o filtro por categoria funcione corretamente e que livros relacionados sejam exibidos na página de detalhes de um livro específico.

---

### **2. Escopo**
- **Funcionalidade testada:** Listagem e Filtros de Livros  
- **Testes realizados:**
  - Exibição da lista completa de livros.
  - Filtragem de livros por categoria.
  - Exibição de livros relacionados na página de detalhes.

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
| CT-07.1            | Exibir a lista completa de livros             | Passou     | Lista de livros exibida corretamente.            |
| CT-07.2            | Filtrar livros por categoria                  | Falhou     | Filtro não exibiu resultados corretos (categoria "Romance"). |
| CT-07.3            | Exibir livros relacionados na página de detalhes | Falhou  | Página de detalhes do livro não encontrada (erro 404). |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-07.1: Exibir a Lista Completa de Livros**
- **Descrição:** Verificar se o sistema exibe todos os livros cadastrados na página de categorias.
- **Entradas:** Acessar a página `/categoria`.  
- **Resultados Esperados:**  
  - Exibição da lista completa de livros cadastrados.  
- **Resultados Obtidos:**  
  - **Status:** Passou  
  - **Observação:** Todos os livros cadastrados foram exibidos corretamente na tela de listagem.  

#### **CT-07.2: Filtrar Livros por Categoria**
- **Descrição:** Verificar se o sistema filtra corretamente os livros da categoria "Romance".
- **Entradas:**  
  - Acessar a página `/categoria`.  
  - Selecionar a categoria "Romance".  
- **Resultados Esperados:**  
  - Apenas livros da categoria "Romance" são exibidos.  
- **Resultados Obtidos:**  
  - **Status:** Falhou  
  - **Observação:** O filtro não retornou resultados consistentes para a categoria "Romance".  
    - **Evidências:**  
      A lista exibiu todos os livros em vez de restringir à categoria selecionada.  

#### **CT-07.3: Exibir Livros Relacionados na Página de Detalhes**
- **Descrição:** Verificar se a página de detalhes de um livro exibe livros relacionados da mesma categoria.
- **Entradas:**  
  - Acessar a página `/livro/1`.  
- **Resultados Esperados:**  
  - Exibição da seção "Livros Relacionados" com livros da mesma categoria.  
- **Resultados Obtidos:**  
  - **Status:** Falhou  
  - **Observação:** O sistema retornou erro 404 ao tentar acessar a página de detalhes do livro.
- **Evidências:**
  ![CT_07](https://drive.google.com/uc?export=view&id=1sMxfN4Dh7V0at2epemCMzGjE-RerOuQJ)


---

### **6. Bugs Identificados**

| **ID do Bug** | **Descrição**                                       | **Impacto** | **Status** |
|---------------|-----------------------------------------------------|-------------|------------|
| BUG-007.1     | O filtro de categoria não funciona corretamente.    | Alto        | Aberto     |
| BUG-007.2     | A página de detalhes do livro com ID `1` não foi encontrada. | Alto        | Aberto     |

---

### **7. Conclusão**
Os testes realizados para a funcionalidade de listagem e filtros de livros apresentaram falhas. Enquanto a listagem completa de livros funcionou corretamente, o filtro por categoria e a exibição de livros relacionados falharam devido a problemas na lógica de filtro e na configuração de rotas.

**Status Geral:** Reprovado  

---

### **8. Recomendações**
1. Revisar a lógica de filtro no backend para garantir que os resultados retornados sejam filtrados corretamente pela categoria.
2. Verificar a existência e configuração das rotas para acessar a página de detalhes de um livro.
3. Realizar testes adicionais após corrigir os erros para validar as alterações implementadas.

--- 
