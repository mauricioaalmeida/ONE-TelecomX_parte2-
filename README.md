# Telecom X - Análise de Evasão de Clientes - Parte 2


<p align="left">
  <img src="https://img.shields.io/static/v1?label=&message=Python&color=blue&style=for-the-badge&logo=python"/>
  <img src="https://img.shields.io/static/v1?label=&message=Pandas&color=blue&style=for-the-badge&logo=pandas"/>
  <img src="https://img.shields.io/static/v1?label=&message=matplotlib&color=blue&style=for-the-badge&logo=matplotlib"/>
  <img src="https://img.shields.io/static/v1?label=&message=seaborn&color=blue&style=for-the-badge&logo=seaborn"/>
  <img src="https://img.shields.io/static/v1?label=&message=Scikit-Learn&color=blue&style=for-the-badge&logo=Scikit-Learn"/>
  <img src="https://img.shields.io/static/v1?label=&message=Colab&color=blue&style=for-the-badge&logo=googlecolab"/>
  <img src="http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge"/>
</p>

Este projeto faz parte do desafio de Data Science do programa Oracle Next Education (ONE) e tem como objetivo desenvolver modelos preditivos para identificar clientes com maior propensão a cancelar os serviços da Telecom X.

## 📋 Descrição do Projeto

A evasão de clientes (churn) é um dos maiores desafios para empresas de telecomunicações. Antecipar quais clientes estão propensos a cancelar serviços permite ações estratégicas para retenção e aumento de receita. Este projeto consiste na construção de um pipeline robusto para a etapa de modelagem preditiva, usando dados previamente tratados e analisados na Parte 1 do projeto.

- [Parte 1 - Análise Exploratória e Pré-processamento dos Dados](https://github.com/mauricioaalmeida/ONE-TelecomX)

## 🎯 Objetivos do Desafio

1. **Preparar os dados para a modelagem** (tratamento, encoding, normalização).
2. **Análise de correlação e seleção de variáveis**.
3. **Treinar dois ou mais modelos de classificação**.
4. **Avaliar o desempenho dos modelos com métricas apropriadas**.
5. **Interpretar os resultados**, incluindo análise de importância das variáveis.
6. **Conclusão estratégica** destacando os principais fatores que influenciam a evasão.

## 🧰 Ferramentas Utilizadas

- Google Colab
- Python 3
- Pandas
- Numpy
- Scikit-Learn
- Matplotlib
- Seaborn

## 🤖 Técnicas e Modelos de Machine Learning

Este projeto utilizou um pipeline completo de Machine Learning, aplicando as seguintes técnicas e modelos:

### **Transformações e Pré-processamento**
- **OneHotEncoder:** Aplicado para transformar variáveis categóricas em variáveis numéricas, facilitando o uso em modelos.
- **Normalização:** Normalização dos dados numéricos para melhorar a performance dos algoritmos.
- **Pipelines do Scikit-Learn:** Toda a preparação dos dados (encoding, normalização, seleção de variáveis) foi estruturada com o uso de `Pipeline` e `ColumnTransformer`, garantindo reprodutibilidade e organização.

### **Validação e Otimização**
- **KFold Cross-Validation:** Utilização de validação cruzada com múltiplos folds (KFold) para avaliação robusta dos modelos, minimizando o risco de overfitting e garantindo maior generalização.
- **GridSearchCV:** Busca em grade para otimizar hiperparâmetros dos modelos, garantindo a melhor configuração possível para cada algoritmo.

### **Modelos de Classificação Aplicados**
- **Logistic Regression (Regressão Logística)**
- **Random Forest Classifier (Floresta Aleatória)**
- **SVM: Support-Vector Machine (Máquina de Vetores de Suporte)**

### **Seleção de Variáveis**
- **Análise de Correlação:** Seleção de features com maior influência no churn.
- **Importância das Variáveis:** Cálculo da importância das features, principalmente via Random Forest.

## 📂 Estrutura do Projeto

```
.
├── data/
│   ├── bronze/    # Dados brutos
│   ├── prata/     # Dados tratados (exemplo: TelecomX_Data.parquet)
│   └── ouro/      # Dados prontos para modelagem
├── Images/        # Imagens geradas nas análises
├── ONE_TelecomX_BR_Parte2.ipynb  # Notebook principal deste repositório
└── README.md
```

## 📑 Dicionário de Dados

**Colunas Originais (Inglês):**
- customerID: número de identificação único de cada cliente
- Churn: se o cliente deixou ou não a empresa
- gender: gênero (masculino e feminino)
- SeniorCitizen: cliente tem 65 anos ou mais
- Partner: possui parceiro(a)
- Dependents: possui dependentes
- tenure: meses de contrato
- PhoneService: assinatura de serviço telefônico
- MultipleLines: múltiplas linhas de telefone
- InternetService: provedor de internet
- OnlineSecurity: segurança online
- OnlineBackup: backup online
- DeviceProtection: proteção de dispositivo
- TechSupport: suporte técnico
- StreamingTV: TV a cabo
- StreamingMovies: streaming de filmes
- Contract: tipo de contrato
- PaperlessBilling: fatura online
- PaymentMethod: forma de pagamento
- Charges.Monthly: gasto mensal
- Charges.Total: gasto total

**Colunas Renomeadas (Português):**
- ID_Cliente: número de identificação único
- Churn: cliente deixou ou não a empresa
- Genero: gênero
- Idoso: 65 anos ou mais
- Casal: possui parceiro(a)
- Dependentes: possui dependentes
- Tempo_Contrato: meses de contrato
- Servico_Telefone: serviço telefônico
- Servico_MultiplasLinhas: múltiplas linhas de telefone
- Servico_Internet: provedor de internet
- Opt_OnlineSecurity: segurança online
- Opt_OnlineBackup: backup online
- Opt_DeviceProtection: proteção de dispositivo
- Opt_TechSupport: suporte técnico
- Opt_StreamingTV: TV a cabo
- Opt_StreamingMovies: streaming de filmes
- Tipo_Contrato: tipo de contrato
- FaturaOnline: fatura online
- Forma_Pagto: forma de pagamento
- Conta_Mensal: gasto mensal
- Conta_Diarias: gasto diário (novo campo)
- Conta_Total: gasto total

## 🚀 Como Executar

1. **Abra o notebook em Google Colab:**
   - [Colab Link](https://colab.research.google.com/github/mauricioaalmeida/ONE-TelecomX_parte2-/blob/main/ONE_TelecomX_BR_Parte2.ipynb)
2. **Execute as células sequencialmente.** O notebook está organizado em etapas, desde a importação dos dados até a avaliação dos modelos.
3. **Os dados são baixados automaticamente** do repositório [ONE-TelecomX](https://github.com/mauricioaalmeida/ONE-TelecomX) na camada prata.

** Para usar o modelo treinado e salvo:**
1. Baixe o arquivo do modelo em: 'data/models/Random_Forest-7.pkl'
2. Execute o seguinte código:
```python
import pickle

# Carregar um modelo salvo
model_filename = 'data/models/Random_Forest-7.pkl'
with open(model_filename, 'rb') as file:
  loaded_model = pickle.load(file)

# Usar o modelo carregado para previsões
y_pred = loaded_model.predict(x_test)
print(f"Previsões com o modelo {model_name}:", y_pred)
```   

## 📊 Principais Resultados

- Pipeline de preparação de dados com tratamento, encoding e normalização.
- Seleção de variáveis relevantes via análise de correlação.
- Treinamento e avaliação de múltiplos modelos de classificação.
- Otimização de hiperparâmetros com GridSearchCV.
- Validação cruzada com KFold.
- Interpretação dos fatores mais relevantes para o churn.
- Visualizações gráficas para apoiar o entendimento dos resultados.

## 📈 Exemplos de Gráficos

Algumas visualizações geradas no notebook incluem:

- Curva ROC dos modelos
  
![Grafico](https://github.com/mauricioaalmeida/ONE-TelecomX_parte2-/blob/main/data/Images/Grafico_ROC.png)
 
- Matriz de confusão
  
![Grafico](https://github.com/mauricioaalmeida/ONE-TelecomX_parte2-/blob/main/data/Images/Grafico_Confusao.png)

- Importância das variáveis
  
![Grafico](https://github.com/mauricioaalmeida/ONE-TelecomX_parte2-/blob/main/data/Images/Grafico_Features_SHAD.png)


## 💡 Conclusão Estratégica

O projeto identifica os principais fatores que levam à evasão de clientes, permitindo à empresa criar ações direcionadas de retenção e melhorar a experiência do cliente.

Os modelos treinados podem ajudar a identificar clientes com potencial de Churn e algumas das ações abaixo podem ser tomadas para previnir a evasão de clientes (Churn), de forma individual ou combinada:

1- Priorizar contratos de longo prazo: Oferecer descontos progressivos, e/ou recursos adicionais nos contratos com maior prazo para fidelizar clientes.

2- Clientes com contratos a mais tempo, tendem a evadir, portanto, é importante estabelecer estratégias de Marketing, oferecer facilidades ou descontos a clientes que tem contratos com tempo acima da média.

3- Clientes com serviços de Fibra Ótica podem estar insatisfeitos com os serviços prestados, pois há indicações altas de probabilidade de Churn nestes casos.

4- Clientes com contratos mensais tem maior evasão, como no caso 1, priorizar contratos mais longos pode previnir a evasão.

5- Clientes com contas mais altas tem mais probabilidade de evasão.

6- Clientes com os serviços opcionais: OnlineSecurity e TechSupport tem maior evasão, indicando provaveis problemas com este serviço ou custos elevados dos mesmos.

7- Clientes com pagamentos do tipo Eletronic Check tem maior probabilidade de evasão, pode ser interessante oferecer descontos para pagamentos automáticos via cartão de crédito por exemplo.

8 - Clientes sem contrato de serviço de telefone tem maior probabilidade de Churn: Oferecer esse serviço em combos com a Internet de Fibra pode prevenir a evasão.

Em resumo, sugerimos identificar os clientes com potêncial de Churn com os modelos treinados e estabelecer uma estratégia de marketing direcionada aos mesmos com um combo de serviços que inclua:

    Contrato de 2 anos
    Internet de Fibra com Linha de Telefone
    Pagamento eletronico automático com Cartão de Crédito ou Débito automático

Dessa forma fidelizaremos os clientes mais propensos a evasão e podemos ainda utilizar essa estratégia para atrair e reter mais clientes.


## 👨‍💻 Autor

- **Mauricio Almeida**  
  [GitHub](https://github.com/mauricioaalmeida)

---

Projeto desenvolvido para fins educacionais no programa ONE Oracle Next Education em parceria com a ALURA.
