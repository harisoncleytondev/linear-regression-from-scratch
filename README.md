# Calculadora de Regressão Linear

Olá! 👋

Eu criei este projeto para realmente entender como a Regressão Linear Simples funciona "por baixo dos panos". Em vez de usar bibliotecas de Machine Learning prontas (como o `scikit-learn`), eu decidi construir todo o modelo do zero, usando apenas as fórmulas matemáticas puras.

Foi um desafio divertido para provar que eu entendia a teoria por trás da estatística. O resultado é esta calculadora de regressão totalmente funcional, que usa apenas a biblioteca `pandas` para organizar os dados.

---

## O que este modelo faz?

O script calcula os 5 componentes principais de uma Regressão Linear Simples:

* **Coeficiente `b` (Inclinação):** Mostra o quanto `Y` muda para cada unidade de `X`.
* **Coeficiente `a` (Intercepto):** O ponto onde a linha "começa" no eixo Y.
* **Coeficiente `R` (Correlação):** Mede a *força* da relação entre `X` e `Y` (de -1 a +1).
* **Coeficiente `R²` (Determinação):** A "nota" de precisão do modelo. Diz quantos % da variação em `Y` são explicados por `X`.
* **Previsão:** Permite que você digite um novo valor de `X` e receba a previsão de `Y`.

---

## Arquivos do Projeto

* **`regressao.ipynb`**: O Notebook (Jupyter/Colab) com toda a minha análise, desenvolvimento e o processo passo a passo.
* **`regressao.py`**: O script Python final e limpo, pronto para ser executado e fazer previsões.
* **`dados-80.csv`**: O conjunto de dados de exemplo que eu usei para treinar e testar o modelo.

---

## As Fórmulas por Trás do Código

O núcleo deste projeto foi traduzir estas equações estatísticas para código Python:

### Inclinação (Coeficiente `b`)
$$ b = \frac{n(\sum xy) - (\sum x)(\sum y)}{n(\sum x^2) - (\sum x)^2} $$

### Intercepto (Coeficiente `a`)
$$ a = \bar{y} - b\bar{x} $$

### Correlação (Coeficiente `R`)
$$ R = \frac{n(\sum xy) - (\sum x)(\sum y)}{\sqrt{ [n(\sum x^2) - (\sum x)^2] \cdot [n(\sum y^2) - (\sum y)^2] }} $$

### Determinação (Coeficiente `R²`)
$$ R^2 = (R)^2 $$

### Previsão (Y-previsto)
$$ \hat{y} = a + bx $$
