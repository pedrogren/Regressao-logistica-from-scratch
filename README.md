# Regressão Logística do Zero
Implementação didática do algoritmo de Regressão Logística em Python, desenvolvida do zero sem o uso de bibliotecas de Machine Learning como Scikit-Learn.

Funcionamento
A estrutura da classe LogisticRegression é dividida nas seguintes etapas:

init: Configura os hiperparâmetros de entrada, sendo o número de épocas (padrão: 100) e a taxa de aprendizado (padrão: 0.5).

fit: Inicializa os pesos e o viés zerados, realiza a combinação linear e aplica a função Sigmoide. Utiliza np.clip para evitar problemas numéricos no cálculo do erro e otimiza os parâmetros via Gradient Descent.

predict: Aplica os parâmetros ajustados aos novos dados e retorna a classificação final (0 ou 1) adotando um limiar de 0.5.

# Ferramentas

Python

NumPy

Pandas

# Exemplo de uso:
```python
X = pd.DataFrame({'f1': [1.0, 2.0, 3.0, 4.0], 'f2': [0.5, 1.0, 1.5, 2.0]})
y = pd.Series([0, 0, 1, 1])

modelo = LogisticRegression(epocas=100, lr=0.1)
modelo.fit(X, y)
previsoes = modelo.predict(X)
```
