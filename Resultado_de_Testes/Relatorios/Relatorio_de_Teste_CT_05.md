### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros   
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias.  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste é validar a funcionalidade de adição de livros no sistema, garantindo que todos os campos obrigatórios sejam devidamente validados e que os livros sejam cadastrados corretamente com base nos requisitos especificados.

---

### **2. Escopo**
- Funcionalidade testada: **Adicionar Livro**
- Testes realizados:
  - Campos obrigatórios no formulário de adição.
  - Adição bem-sucedida com dados válidos.
  - Comportamento do sistema ao não enviar dados válidos.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home
- **Navegador:** Electron
- **Ferramenta de Automação:** Cypress
- **Banco de Dados:** MySQL Workbench

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**                         | **Status**  | **Observações**                                    |
|--------------------|-------------------------------------------------------|-------------|---------------------------------------------------|
| CT-05.1            | Adicionar livro com todos os campos válidos           | Passou      | Livro adicionado com sucesso.                    |
| CT-05.2            | Verificar validação de campos obrigatórios            | Passou      | Sistema bloqueou a submissão sem preencher campos. |
| CT-05.3            | Inserção de nenhum dado nos campos     | Não retornou mensagem de erro.      | Sistema indicou os campos inválidos corretamente.|

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-05.1: Adicionar Livro com Dados Válidos**
- **Descrição:** Testar se o sistema permite adicionar um livro com todos os campos preenchidos corretamente.
- **Entradas:** 
  - Título: "Livro Teste"
  - Autor: "Autor Teste"
  - Ano: "2024"
  - Preço: "50,00"
  - [Outros campos]
- **Resultados Esperados:** Livro adicionado com sucesso e mensagem "Livro adicionado com sucesso" exibida.
- **Resultado Obtido:** Passou
- **Evidência:**
![CT_05](https://drive.google.com/uc?export=view&id=1jgaeXVFGNiM8HJyhWVwMBObQjF5kWbzo)

---

#### **CT-05.2: Validação de Campos Obrigatórios**
- **Descrição:** Testar se o sistema bloqueia a submissão do formulário quando campos obrigatórios estão vazios.
- **Entradas:** Nenhum campo preenchido.
- **Resultados Esperados:** Submissão bloqueada e campos destacados como inválidos.
- **Resultado Obtido:** [Ex.: Passou]

---

#### **CT-05.3: Dados Inválidos**
- **Descrição:** Testar o comportamento do sistema ao inserir dados inválidos nos campos (ex.: letras no campo "Ano").
- **Entradas:** 
  - Ano: "Texto"
  - Preço: "-50"
- **Resultados Esperados:** Sistema bloqueia submissão e destaca campos inválidos.
- **Resultado Obtido:** Passou


---

### **6. Bugs Identificados**
| **ID do Bug** | **Descrição**                | **Impacto**    | **Status**       |
|---------------|------------------------------|----------------|------------------|
| BUG-001       | Mensagem de erro sobre os campos obrigatórios não preenchidos não foi exibida. | Alto           | Aberto           |

---

### **7. Conclusão**
Com base nos testes realizados:
- **Status Geral:** Aprovado
- O sistema passou nos principais testes de funcionalidade relacionados à adição de livros.

---

### **8. Recomendações**
- Revisar as validações para campos opcionais.
- Melhorar mensagens de erro para maior clareza ao usuário.
- Testar com maior diversidade de navegadores e dispositivos para garantir compatibilidade.
