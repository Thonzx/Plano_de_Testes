
### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste foi verificar as funcionalidades de notificações e destaque de livros, garantindo que os usuários possam marcar e desmarcar livros como destaque e que os livros destacados apareçam na página inicial.

---

### **2. Escopo**
- **Funcionalidade testada:** Notificações e Destaques  
- **Testes realizados:**
  - Marcar um livro como destaque.
  - Desmarcar um livro como destaque.
  - Verificar se livros destacados aparecem na página principal.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**                      | **Status** | **Observações**                                                                 |
|--------------------|----------------------------------------------------|------------|---------------------------------------------------------------------------------|
| CT-08.1            | Marcar um livro como destaque                     | Falhou     | Botão de "Marcar Destaque" está bloqueado por outro elemento.                  |
| CT-08.2            | Desmarcar um livro como destaque                  | Falhou     | O botão de "Desmarcar Destaque" não foi encontrado na página.                  |
| CT-08.3            | Verificar livros destacados na página principal   | Falhou     | Nenhum livro destacado foi encontrado na seção "Destaques".                    |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-08.1: Marcar um Livro como Destaque**
- **Descrição:** Verificar se o sistema permite marcar um livro como destaque.  
- **Entradas:** Ação no botão "Marcar Destaque" para um livro listado na página do usuário.  
- **Resultados Esperados:**  
  - Livro é marcado como destaque.  
  - O botão muda para "Desmarcar Destaque".  
- **Resultados Obtidos:**  
  - **Status:** Falhou  
  - **Observação:** O botão "Marcar Destaque" foi bloqueado por outro elemento na interface.  

#### **CT-08.2: Desmarcar um Livro como Destaque**
- **Descrição:** Verificar se o sistema permite desmarcar um livro como destaque.  
- **Entradas:** Ação no botão "Desmarcar Destaque" para um livro destacado na página do usuário.  
- **Resultados Esperados:**  
  - Livro é removido dos destaques.  
  - O botão muda para "Marcar Destaque".  
- **Resultados Obtidos:**  
  - **Status:** Falhou  
  - **Observação:** O botão "Desmarcar Destaque" não foi encontrado na página, indicando que o livro não estava destacado.  

#### **CT-08.3: Verificar Livros Destacados na Página Principal**
- **Descrição:** Verificar se os livros destacados aparecem corretamente na seção de destaques da página principal.  
- **Entradas:** Acessar a página inicial após marcar um livro como destaque.  
- **Resultados Esperados:**  
  - A seção "Destaques" exibe pelo menos um livro.  
- **Resultados Obtidos:**  
  - **Status:** Falhou  
  - **Observação:** A seção "Destaques" não exibiu nenhum livro, indicando ausência de livros destacados no banco de dados ou falha na exibição.
- **Evidências:**
  - ![CT_08](https://drive.google.com/uc?export=view&id=18_WMnEi8KG3WiXXngXxO6Dh7_Jdp9OHV)


---

### **6. Bugs Identificados**

| **ID do Bug** | **Descrição**                                                       | **Impacto** | **Status** |
|---------------|---------------------------------------------------------------------|-------------|------------|
| BUG-008.1     | Botão "Marcar Destaque" está bloqueado por outro elemento.          | Alto        | Aberto     |
| BUG-008.2     | Botão "Desmarcar Destaque" não é exibido após marcar um destaque.   | Médio       | Aberto     |
| BUG-008.3     | Seção "Destaques" na página inicial não exibe livros destacados.    | Alto        | Aberto     |

---

### **7. Conclusão**
Os testes relacionados à funcionalidade de notificações e destaque de livros falharam. Os problemas incluem elementos bloqueados na interface, ausência de elementos esperados e falha na exibição dos destaques na página inicial.  

**Status Geral:** Reprovado  

---

### **8. Recomendações**
1. **Corrigir o layout** para garantir que os botões "Marcar Destaque" e "Desmarcar Destaque" não sejam bloqueados por outros elementos.
2. Verificar a lógica no backend para garantir que o estado dos livros destacados seja atualizado corretamente.
3. Revisar a funcionalidade de exibição de livros destacados na página principal, incluindo consulta ao banco de dados e renderização no frontend.
4. Realizar testes adicionais após corrigir os problemas relatados.

---
