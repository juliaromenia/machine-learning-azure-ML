# Configuração no Azure para ML Automatizado

## **1. Configurar a Conta Azure Machine Learning**

### **1.1 Criar um Workspace no Azure**
1. Acesse o [Portal do Azure](https://portal.azure.com/).
2. No menu de navegação à esquerda, clique em **"Criar um recurso"** ou procure por **"Machine Learning"** na barra de pesquisa.
3. Preencha os dados necessários para a criação:
   - **Assinatura**: Selecione a assinatura que será usada para pagar os recursos.
   - **Grupo de Recursos**: Escolha um grupo existente ou clique em **"Criar novo"** para criar um novo grupo de recursos.
     - *Dica*: Um grupo de recursos é um contêiner lógico para organizar e gerenciar todos os serviços relacionados ao projeto.
   - **Nome do Workspace**: Escolha um nome exclusivo para o espaço de trabalho.
   - **Região**: Escolha a região onde os recursos serão hospedados (por exemplo, "East US" ou "Brazil South").
   - **Conta de Armazenamento**: Use as configurações padrão ou escolha uma conta de armazenamento existente.
   - **Azure Key Vault**: O Azure Key Vault gerencia credenciais e chaves de segurança. Use a configuração padrão ou crie uma nova conta.
   - **Application Insights**: Habilite para monitorar os recursos e a performance do workspace.
4. Após preencher todos os campos, clique em **"Revisar + Criar"**.
5. Revise as configurações e clique em **"Criar"**.
6. Aguarde a conclusão da criação.
7. Clique em **"Ir para o recurso"** para acessar o workspace.

---

## **2. Configurar um Trabalho de ML Automatizado**

### **2.1 Acessar o Azure Machine Learning Studio**
1. Acesse o [Azure Machine Learning Studio](https://ml.azure.com/).
2. No painel do workspace, clique em **"ML Automatizado"** no menu lateral esquerdo.

### **2.2 Criar um Novo Trabalho**
1. Clique no botão **"+ Novo trabalho de ML automatizado"**.
2. Preencha as configurações básicas:
   - **Nome do Trabalho**: Escolha um nome descritivo.
   - **Nome do Experimento**: Dê um nome para o experimento.
   - **Descrição**: Adicione uma breve descrição do trabalho.

---

## **3. Configurar as Tarefas do ML Automatizado**

### **3.1 Tipo de Tarefa**
- Escolha o tipo de tarefa conforme o objetivo:
  - **Classificação**: Para prever categorias (ex.: verdadeiro/falso).
  - **Regressão**: Para prever valores numéricos contínuos (ex.: preços).
  - **Forecasting**: Para prever séries temporais (ex.: demanda futura).

### **3.2 Criar o Ativo de Dados**
1. Clique em **"Criar ativo de dados"** e preencha as informações:
   - **Nome**: Defina um nome para o ativo de dados.
   - **Descrição**: Opcional, mas útil para identificar o dataset.
   - **Tipo**: Escolha o tipo apropriado (ex.: tabela).
2. **Fonte de Dados**:
   - Selecione **"De arquivos da Web"**.
   - Insira a **URL da Web** que contém o arquivo de dados.
3. Conclua a configuração do ativo de dados.

### **3.3 Configurações de Tarefas**
- **Coluna de Destino**: Escolha a coluna que será o alvo da previsão.
- **Limites** (opcional): Configure limites de treinamento, como tempo máximo ou número de iterações.
- **Validação e Teste**:
   - Configure métodos de validação para o treinamento do modelo.

---

## **4. Configurar Recursos de Computação**

1. Escolha ou crie um recurso de computação:
   - Use um **Cluster de Computação** existente ou clique em **"Criar novo"**.
   - Configure os recursos, como número de CPUs e memória (o padrão geralmente é suficiente).
2. Conclua a configuração.

---

## **5. Examinar e Enviar o Trabalho**
1. Revise todas as configurações na aba **"Examinar"**.
2. Clique em **"Enviar trabalho de treinamento"**.

---

## **6. Acompanhar o Treinamento**

1. No painel **"Tarefas"**, localize o trabalho enviado.
2. Clique no trabalho para acompanhar o progresso:
   - Status de carregamento.
   - Logs de execução.
   - Resultados parciais.

---

## **7. Visualizar Métricas**
1. Após o treinamento ser concluído, acesse a aba **"Métricas"** para visualizar:
   - Gráficos de desempenho.
   - Métricas calculadas (ex.: acurácia, erro médio, etc.).
2. Identifique o modelo com melhor desempenho para uso futuro.

---

[documentação oficial do Azure](https://learn.microsoft.com/azure/machine-learning).
