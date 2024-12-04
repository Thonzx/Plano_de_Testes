### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste foi validar o fluxo de negociação de livros, incluindo o redirecionamento para a área de negociação e posteriormente para o WhatsApp, garantindo que a funcionalidade esteja operando conforme o esperado.

---

### **2. Escopo**
- **Funcionalidade testada:** Fluxo de Compra com Negociação  
- **Testes realizados:**
  - Redirecionamento para a área de negociação ao clicar no botão "Comprar".
  - Redirecionamento para o WhatsApp ao clicar no botão "Negociar".

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**                                           | **Status** | **Observações**                                   |
|--------------------|-------------------------------------------------------------------------|------------|--------------------------------------------------|
| CT-10.1            | Redirecionar para a área de negociação ao clicar em "Comprar".         | Aprovado   | Comportamento conforme esperado.                |
| CT-10.2            | Redirecionar para o WhatsApp ao clicar no botão de negociação.         | Reprovado  | O teste não capturou a URL esperada no redirecionamento. |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-10.1: Redirecionar para a Área de Negociação ao Clicar em "Comprar"**
- **Descrição:** Verificar se o sistema redireciona para a página de negociação ao clicar no botão "Comprar" de um livro.
- **Entradas:** Botão "Comprar" na página inicial.
- **Resultados Esperados:**  
  - O usuário é redirecionado para a página `/livro/{id}` do livro selecionado.  
- **Resultados Obtidos:**  
  - **Status:** Aprovado  
  - **Observação:** Redirecionamento realizado corretamente para a página de negociação.  

#### **CT-10.2: Redirecionar para o WhatsApp ao Clicar no Botão de Negociação**
- **Descrição:** Verificar se o sistema redireciona para o WhatsApp ao clicar no botão "Negociar" na página de detalhes do livro.
- **Entradas:** Botão "Negociar" na página `/livro/{id}`.
- **Resultados Esperados:**  
  - O usuário é redirecionado para a URL `https://wa.me/` com o número de contato configurado.  
- **Resultados Obtidos:**  
  - **Status:** Reprovado  
  - **Observação:** O redirecionamento foi realizado, mas a URL capturada pelo Cypress estava vazia, resultando em falha no teste.
- **Evidência:** 
  ![CT_10](https://drive.google.com/uc?export=view&id=1FQblN747CC1ygzVyKkf54HAp_mNJBcfw)

---

### **6. Bugs Identificados**

| **ID do Bug** | **Descrição**                                       | **Impacto** | **Status** |
|---------------|-----------------------------------------------------|-------------|------------|
| BUG-010.1     | O teste não capturou a URL de redirecionamento para o WhatsApp. | Médio       | Aberto     |

---

### **7. Conclusão**
Os testes realizados para o fluxo de compra e negociação apresentaram resultados mistos. O redirecionamento para a área de negociação funcionou corretamente. Entretanto, o teste para redirecionamento ao WhatsApp falhou devido à captura inadequada da URL redirecionada.  

**Status Geral:** Parcialmente Aprovado  

---

### **8. Recomendações**
1. Revisar a configuração do botão "Negociar" e garantir que o redirecionamento ocorre de forma síncrona para evitar atrasos na captura da URL pelo Cypress.
2. Validar o comportamento de redirecionamento no ambiente real para garantir consistência.
3. Atualizar o teste Cypress para capturar corretamente o redirecionamento usando comandos como `cy.window()` para observar as mudanças na URL.

---
