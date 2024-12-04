# Plano_de_Testes

Este repositório contém a documentação e os resultados dos testes realizados no sistema **Bookstore**. A seguir, está uma visão geral das pastas e arquivos, juntamente com instruções para acessá-los e compreendê-los.

---

### **1. Estrutura do Repositório**

O repositório está organizado em três principais diretórios:

#### **1.1 Casos_de_Teste**
- **Descrição:** Contém os casos de teste planejados, com identificadores e cenários específicos.
- **Arquivos:** Cada arquivo representa um caso de teste específico no formato Markdown (.md), nomeado como `CT_XX.md`, onde `XX` é o identificador do caso de teste.
- **Exemplo:** 
  - `CT_01.md`: Contém o caso de teste para **Verificação de Funcionalidade de Login**.
  - `CT_10.md`: Relacionado ao **Fluxo de Compra e Negociação**.

#### **1.2 Plano_de_Testes**
- **Descrição:** Contém o plano geral de testes realizado para o sistema.
- **Arquivo:** 
  - `Plano_de_Testes.md`: Descreve o escopo dos testes, objetivos, critérios de aceitação, ferramentas utilizadas e a cobertura planejada.

#### **1.3 Resultado_de_Testes**
- **Descrição:** Guarda os resultados dos testes executados, organizados pelo framework utilizado.
- **Subdiretório:**
  - **Cypress:**
    - Contém resultados específicos de testes automatizados, nomeados como `CT_XX.md`.

#### **1.4 Relatorios**
- **Descrição:** Contém relatórios detalhados dos casos de teste executados, incluindo observações, resultados e análises.
- **Arquivos:** Cada relatório é nomeado como `Relatorio_de_Teste_CT_XX.md`, onde `XX` refere-se ao identificador do caso de teste.

---

### **2. Como Navegar nos Arquivos**

#### **2.1 Acessando os Casos de Teste**
1. Entre na pasta `Casos_de_Teste`.
2. Escolha o arquivo correspondente ao identificador do caso de teste que deseja analisar, como `CT_01.md`.

#### **2.2 Acessando o Plano de Testes**
1. Navegue até a pasta `Plano_de_Testes`.
2. Abra o arquivo `Plano_de_Testes.md` para entender o planejamento geral e os objetivos dos testes.

#### **2.3 Visualizando os Resultados dos Testes**
1. Vá para a pasta `Resultado_de_Testes` > `Cypress`.
2. Localize o arquivo do caso de teste desejado, como `CT_06.md`.
3. O arquivo detalha os logs e status do caso de teste específico.

#### **2.4 Relatórios dos Testes**
1. Entre na pasta `Relatorios`.
2. Abra o relatório correspondente ao caso de teste que deseja visualizar, como `Relatorio_de_Teste_CT_08.md`.
3. O relatório fornece detalhes sobre o contexto do teste, resultados esperados e observações encontradas durante a execução.

---

### **3. Convenções Utilizadas**

- **Identificador do Caso de Teste:** Cada teste possui um identificador único no formato `CT_XX`.
- **Formato Markdown:** Todos os arquivos estão no formato `.md` para facilitar a leitura e edição.
- **Estrutura Padronizada:** Os casos de teste, resultados e relatórios seguem um modelo consistente para facilitar o entendimento.

---

### **4. Ferramentas Utilizadas**
- **Framework de Teste:** Cypress.
- **Banco de Dados:** MySQL.
- **Servidor:** Node.js com Express.
- **Frontend:** Handlebars.

---

### **5. Contribuindo**
- Para adicionar novos casos de teste, siga o modelo presente nos arquivos existentes.
- Certifique-se de atualizar o `Plano_de_Testes.md` com qualquer alteração significativa no escopo dos testes.

---

Com esta organização, é possível navegar facilmente pelos testes planejados, executados e seus respectivos relatórios. Para dúvidas ou contribuições, entre em contato com o responsável pelo repositório.
