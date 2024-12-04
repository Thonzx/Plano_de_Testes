### **Relatório de Teste**

**Nome do Projeto:** Sistema BookStore - Login  
**Equipe de Testes:** Wellython Salmo, Carlos Breno, Bruna Miranda e Julia Farias  
**Ferramentas Utilizadas:** Cypress
---

### **Objetivo**
Validar a funcionalidade de login no sistema, garantindo que:
- Usuários consigam acessar suas contas com credenciais válidas.
- Mensagens de erro adequadas sejam exibidas para tentativas de login inválidas, incluindo senhas incorretas e usuários inexistentes.

---

### **Resumo dos Casos de Teste**

| **Identificador** | **Descrição do Caso de Teste**               | **Status**  | **Observações**                                      |
|--------------------|---------------------------------------------|-------------|-----------------------------------------------------|
| CT-01             | Login com credenciais válidas               | **Passou**  | Login realizado com sucesso, redirecionado para `/usuario`. |
| CT-02             | Login com senha incorreta                   | **Passou**  | Mensagem "Senha incorreta." exibida corretamente.   |
| CT-03             | Login com usuário inexistente               | **Passou**  | Mensagem "Usuário não encontrado." exibida corretamente. |

---

### **Detalhamento dos Casos de Teste**

#### **CT-01: Login com Credenciais Válidas**
- **Descrição:** Testar se o sistema permite login com email e senha corretos.
- **Entradas:** 
  - Email: `wellythonsouza105@gmail.com`
  - Senha: `110706`
- **Resultados Esperados:** 
  - O usuário é redirecionado para a rota `/usuario`.
  - A página contém o texto "Meu Perfil".
- **Resultado Obtido:** **Passou.**
- **Evidência:**  
  - Redirecionamento bem-sucedido para `/usuario`.
  - Elemento "Meu Perfil" visível na página.

---

#### **CT-02: Login com Senha Incorreta**
- **Descrição:** Testar o comportamento do sistema quando a senha informada está incorreta.
- **Entradas:** 
  - Email: `wellythonsouza105@gmail.com`
  - Senha: `senhaErrada`
- **Resultados Esperados:** 
  - Mensagem "Senha incorreta." visível no formulário de login.
- **Resultado Obtido:** **Passou.**
- **Evidência:**  
  - Mensagem "Senha incorreta." exibida corretamente.

---

#### **CT-03: Login com Usuário Inexistente**
- **Descrição:** Testar o comportamento do sistema quando o email fornecido não está cadastrado.
- **Entradas:** 
  - Email: `naoexiste@teste.com`
  - Senha: `senha123`
- **Resultados Esperados:** 
  - Mensagem "Usuário não encontrado." visível no formulário de login.
- **Resultado Obtido:** **Passou.**
- **Evidência:**  
  - Mensagem "Usuário não encontrado." exibida corretamente.

---

### **Análise Geral**
Os testes de login foram realizados com sucesso. O sistema respondeu conforme o esperado para todas as condições:
- Credenciais válidas permitiram acesso ao sistema.
- Mensagens de erro claras foram exibidas para credenciais inválidas ou não registradas.

---

### **Recomendações**
- **Melhoria de usabilidade:** Considere adicionar uma opção para "Mostrar senha" ao campo de entrada de senha para facilitar a correção de erros.
- **Logs de auditoria:** Verifique se as tentativas de login (bem-sucedidas ou falhas) estão sendo registradas no sistema para fins de segurança.

---
