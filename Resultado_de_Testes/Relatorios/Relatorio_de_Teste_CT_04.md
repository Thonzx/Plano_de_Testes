### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
Validar a funcionalidade de busca por livros, assegurando que:
- Livros existentes possam ser encontrados pelo título.
- O sistema retorne uma mensagem apropriada caso nenhum resultado seja encontrado.

---

### **2. Escopo**
- Funcionalidade testada: **Busca de Livros**
- Testes realizados:
  - Busca de um livro existente pelo título.
  - Busca de um termo inexistente.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL Workbench  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste** | **Status**  | **Observações**                                   |
|--------------------|--------------------------------|-------------|--------------------------------------------------|
| CT-04.1            | Buscar livro existente pelo título | Passou      | Livro encontrado e resultados exibidos corretamente. |
| CT-04.2            | Buscar termo inexistente      | Passou      | Mensagem de "Nenhum livro encontrado" exibida corretamente. |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-04.1: Buscar Livro Existente por Título**
- **Descrição:** Testar se o sistema permite buscar um livro existente pelo título e exibe os resultados corretamente.
- **Entradas:** 
  - Termo: "Harry Potter e a Pedra Filosofal"
- **Resultados Esperados:** 
  - A URL é redirecionada para `/pesquisar?termo=Harry+Potter+e+a+Pedra+Filosofal`.
  - A mensagem `Resultados para "Harry Potter e a Pedra Filosofal"` é exibida.
  - Os detalhes do livro correspondente são exibidos na página.
- **Resultado Obtido:** Passou
  
---

#### **CT-04.2: Buscar Termo Inexistente**
- **Descrição:** Testar se o sistema exibe a mensagem correta ao buscar um termo inexistente.
- **Entradas:** 
  - Termo: "Livro Inexistente"
- **Resultados Esperados:** 
  - A URL é redirecionada para `/pesquisar?termo=Livro+Inexistente`.
  - A mensagem `Nenhum livro encontrado para "Livro Inexistente"` é exibida.
- **Resultado Obtido:** Passou  
- **Evidência:**
![Descrição da Imagem](https://drive.google.com/uc?export=view&id=1SGLo0D1B_b5VeWqNHth7eEGZEuHJcnEC)

---

### **6. Bugs Identificados**
Nenhum bug identificado.

---

### **7. Conclusão**
Com base nos testes realizados:
- **Status Geral:** Aprovado  
- O sistema passou nos testes de busca por livros, exibindo corretamente os resultados e mensagens para casos inexistentes.

---

### **8. Recomendações**
- Adicionar filtros adicionais (ex.: categoria, autor, faixa de preço) para refinar os resultados de busca.
- Testar a funcionalidade em dispositivos móveis para garantir compatibilidade e responsividade.

---
