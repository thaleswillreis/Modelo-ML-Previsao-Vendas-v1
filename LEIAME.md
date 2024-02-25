# Modelo de Regressão Linear para o cálculo de Score de Crédito de Clientes

Projeto destinado a criação, teste e avaliação de um exemplo de modelo SVM (Support Vector Machine) que poderá ser utilizado para prever a efetivação de compras no varejo online.

## Fases do projeto

1. Análise exploratória dos dados

   * Verificação das características gerais dos dados;
   * Verificação de dados faltantes;
   * Verificação de dados inconsistentes;
   * Engenharia de atributos.
2. Visualização dos dados

   * Criação de tabelas e gráficos;
3. Transformação dos dados

   * Criação de novas colunas de dados;
   * Tratamento de dados nulos ou incorretos;
   * Exclusão de dados irrelevantes;
   * One Hot Encoding (adequação de tipos de acordo com o algorítimo);
   * Balanceamento da variável alvo;
   * Separação dos dados de treinamento e de teste;
   * Normalização e/ou Padronização dos dados;
4. Criação, Teste e Avaliação dos Modelos de Regressão Linear

   * Criação dos modelos
     1 - Modelo SVM com Kernel Linear;
     2 - Modelo SVM com Kernel Linear e Dados Padronizados
     3 - Modelo SVM com Kernel RBF e Dados Padronizados
     4 - Modelo SVM com Kernel Polinomial e Dados Padronizados
   * Treinamento dos modelos;
   * Teste dos modelos;
   * Avaliação dos modelos;

## Tecnologias Utilizadas

Esse projeto foi executado utilizando a linguagem Python no formato Jupyter Notebook. Foram utilizadas as bibliotecas Pandas (Carregamento, Limpeza e Análise dos Dados), Matplotlib e Seaborn (Visualização de dados e geração de gráficos), Sklearn (Criação, treinamento e avaliação do modelo de Machine Learning), Git (Versionamento de código) e a IDE escolhida foi o Visual Studio Code, rodando em um Debian Linux.

**Links relacionados:**

* [Debian Linux](https://www.debian.org/index.pt.html)
* [VSCode](https://code.visualstudio.com/)
* [Python](https://www.python.org/)
* [Jupyter](https://jupyter.org/)
* [Pandas](https://pandas.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/#)
  [Sklearn](https://scikit-learn.org/stable/)
* [Git](https://git-scm.com/)

### Dependências e Versões Necessárias

Os softwares e bibliotecas utilizados no projetos tinham a seguintes versões:

* Python - Versão: 3.11.5
* Pandas - Versão: 2.2.0
* Matplotlib - Versão: 3.8.3 (matplotlib-inline: 0.1.6)
* Seaborn - Versão: 0.13.2
* Scikit-learn - Versão: 1.4.1

**Obs:** para mais detalhes consulte o aquivo **"requirements.txt"**

## Como rodar o projeto

Para rodar o projeto os seguintes métodos podem ser utilizados:

#### *Método 1:* Fazer o download do projeto

**Passo 1:**

Na pagina principal do projeto [https://github.com/thaleswillreis/Modelo-ML-Previsao-Vendas-v1.git](https://github.com/thaleswillreis/Modelo-ML-Previsao-Vendas-v1.git), busque pelo botão verde contendo o nome "<> Code".

**Passo 2:**

Clique em "Download ZIP"

**Passo 3:**

Descompacte a pasta que você terminou de baixar.

**Passo 4:**

Abra os projetos contendo a extensão ".ipynb".

#### *Método 2:* Clonar o repositório

Obs: Antes de proceder com esse processo, certifique-se de que o GitHub está devidamente configurado no seu computador.

**Passo 1:**

Crie uma pasta na qual você tenha permissão de escrita.

**Passo 2:**

Abra um terminal a partir da pasta recém criada ou navegue até ela pelo terminal.

**Passo 3:**

Na pagina principal do projeto [https://github.com/thaleswillreis/Modelo-ML-Previsao-Vendas-v1.git](https://github.com/thaleswillreis/Modelo-ML-Previsao-Vendas-v1.git), busque pelo botão verde contendo o nome "<> Code".

**Passo 4:**

Copie a URL do repositório.

**Passo 5:**

No terminal digite:

```
git Clone https://github.com/thaleswillreis/Modelo-ML-Previsao-Vendas-v1.git
```

Aguarde a clonagem do repositório terminar.

**Passo 6:**

Abra os projetos contendo a extensão ".ipynb".

## Problemas enfrentados

O código poderá enfrentar problemas ao ser executado utilizando versões diferentes de linguagem e bibliotecas. Certifique-se de que as versões listadas no item "Dependências e Versões Necessárias" estão corretamente instaladas.

Caso já exista um ambiente de desenvolvimento com versões diferentes em uso na máquina utilizada, uma boa alternativa seria a criação de uma ambiente virtual de desenvolvimento. Em caso de dúvida, segue o link da documentação.
[Ambientes virtuais e pacotes](https://docs.python.org/pt-br/3/tutorial/venv.html)

## Resultados Obtidos (Métricas de Avalização)

![alt text](Dados/resultadosML_SVM.png)

## Métricas de Avaliação:

#### **SVM_Modelo_1 (Linear):**

* **Kernel:** Linear
* **Dados:** Não padronizados
* **Métricas:**

  * **Precision:** 0.87
  * **Recall:** 0.79
  * **F1 Score:** 0.83
  * **Acurácia:** 0.82
  * **AUC:** 0.82

**A respeito do resultado:** Este modelo linear não padronizado parece ter um bom desempenho geral, com uma acurácia de 82%. A precisão é relativamente alta, indicando que a maioria das instâncias previstas como positivas realmente é positiva. No entanto, o recall é um pouco mais baixo do que os demais modelos testados, sugerindo que o modelo pode perder algumas instâncias positivas.

#### **SVM_Modelo_2 (Linear com Dados Padronizados):**

* **Kernel:** Linear
* **Dados:** Padronizados
* **Métricas:**

  * **Precision:** 0.77
  * **Recall:** 0.88
  * **F1 Score:** 0.83
  * **Acurácia:** 0.84
  * **AUC:** 0.84

**A respeito do resultado:** Ao padronizar os dados, houve uma melhoria notável no recall (sensibilidade), indicando que o modelo consegue capturar mais instâncias positivas. No entanto, a precisão diminuiu, sugerindo que pode haver mais falsos positivos.

#### **SVM_Modelo_3 (RBF com Dados Padronizados):**

* **Kernel:** RBF (Radial Basis Function)
* **Dados:** Padronizados
* **Métricas:**

  * **Precision:** 0.83
  * **Recall:** 0.89
  * **F1 Score:** 0.86
  * **Acurácia:** 0.87
  * **AUC:** 0.87

**A respeito do resultado:** O modelo RBF com dados padronizados apresenta uma boa combinação de precisão e recall, resultando em um F1 Score e AUC sólidos. Isso sugere que o modelo é capaz de identificar positivos com alta sensibilidade e ainda mantém uma boa precisão.

#### **SVM_Modelo_4 (Polinomial com Dados Padronizados):**

* **Kernel:** Polinomial
* **Dados:** Padronizados
* **Métricas:**

  * **Precision:** 0.81
  * **Recall:** 0.89
  * **F1 Score:** 0.85
  * **Acurácia:** 0.85
  * **AUC:** 0.85

**A respeito do resultado:** O modelo polinomial com dados padronizados tem um desempenho sólido, com uma acurácia de 85%. A precisão é boa, indicando que a maioria das previsões positivas é correta. O recall é alto, sugerindo que o modelo é capaz de identificar a maioria das instâncias positivas.

## Conclusão

A partir dos resultados obtidos, podemos deduzir que a escolha entre os modelos pode depender dos requisitos específicos do problema. Se a ênfase estiver em evitar falsos positivos, o SVM_Modelo_3 (RBF) pode ser preferível. Se o foco for em um equilíbrio geral, SVM_Modelo_4 (Polinomial) pode ser uma escolha sólida. Já a padronização dos dados, parece ser bastante benéfica para o desempenho geral dos modelos SVMs testados. E o ajuste fino dos hiperparâmetros utilizando Grid Search parece ter contribuído para melhorar o desempenho dos modelos.

## Considerações Finais

Caso esse conteúdo seja útil para você, tenha alguma dúvida ou queira contribuir com alguma melhoria, deixe seu comentário ou contribua com o projeto.
