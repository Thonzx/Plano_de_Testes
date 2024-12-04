### **Relatório de Teste**

**Nome do Projeto:** Bookstore - Sistema de Troca e Venda de Livros  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias.  
**Ferramentas Utilizadas:** Cypress (Automação de Testes)  

---

### **1. Objetivo**
O objetivo do teste é validar a funcionalidade de login no sistema, garantindo que:
- Usuários consigam acessar suas contas com credenciais válidas.
- Mensagens de erro adequadas sejam exibidas para tentativas de login inválidas, incluindo senhas incorretas e usuários inexistentes.

---

### **2. Escopo**
- Funcionalidade testada: **Login**
- Testes realizados:
  - Login com credenciais válidas.
  - Login com senha incorreta.
  - Login com usuário inexistente.

---

### **3. Ambiente de Teste**
- **Sistema Operacional:** Windows 11 Home  
- **Navegador:** Electron  
- **Ferramenta de Automação:** Cypress  
- **Banco de Dados:** MySQL Workbench  

---

### **4. Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**       | **Status** | **Observações**                                    |
|--------------------|-------------------------------------|------------|---------------------------------------------------|
| CT-01             | Login com credenciais válidas       | Passou     | Login realizado com sucesso e redirecionado para `/usuario`. |
| CT-02             | Login com senha incorreta           | Passou     | Mensagem "Senha incorreta." exibida corretamente. |
| CT-03             | Login com usuário inexistente       | Passou     | Mensagem "Usuário não encontrado." exibida corretamente. |

---

### **5. Detalhamento dos Casos de Teste**

#### **CT-01: Login com Credenciais Válidas**
- **Descrição:** Testar se o sistema permite login com email e senha corretos.  
- **Entradas:** 
  - Email: `wellythonsouza105@gmail.com`  
  - Senha: `110706`  
- **Resultados Esperados:** 
  - O usuário é redirecionado para a rota `/usuario`.
  - A página contém o texto "Meu Perfil".  
- **Resultado Obtido:** Passou  
- **Evidência:**  
  ![CT_01](https://drive.google.com/uc?export=view&id=19hX0E2LqZt39ntWKkgloCjJhrc21o5ZD)

---

#### **CT-02: Login com Senha Incorreta**
- **Descrição:** Testar o comportamento do sistema quando a senha informada está incorreta.  
- **Entradas:** 
  - Email: `wellythonsouza105@gmail.com`  
  - Senha: `senhaErrada`  
- **Resultados Esperados:** 
  - Mensagem "Senha incorreta." visível no formulário de login.  
- **Resultado Obtido:** Passou  
- **Evidência:**  
  [Adicione prints da tela ou logs do Cypress]

---

#### **CT-03: Login com Usuário Inexistente**
- **Descrição:** Testar o comportamento do sistema quando o email fornecido não está cadastrado.  
- **Entradas:** 
  - Email: `naoexiste@teste.com`  
  - Senha: `senha123`  
- **Resultados Esperados:** 
  - Mensagem "Usuário não encontrado." visível no formulário de login.  
- **Resultado Obtido:** Passou  
- **Evidência:**  
  [Adicione prints da tela ou logs do Cypress]

---

### **6. Bugs Identificados**
| **ID do Bug** | **Descrição**                | **Impacto**    | **Status**       |
|---------------|------------------------------|----------------|------------------|
| -             | Nenhum bug identificado.     | -              | -                |

---

### **7. Conclusão**
Com base nos testes realizados:
- **Status Geral:** Aprovado  
- O sistema passou nos principais testes de funcionalidade relacionados ao login.

---

### **8. Recomendações**
- Melhorar a exibição das mensagens de erro, como adicionar animações ou destaques.
- Garantir testes em diferentes navegadores para verificar compatibilidade.
- Adicionar logs de auditoria para tentativas de login bem-sucedidas e falhas.

---
