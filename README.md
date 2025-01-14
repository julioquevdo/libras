# Reconhecimento de Letras em Libras com Rede Neural Convolucional

Este repositório apresenta um projeto de reconhecimento de letras do alfabeto em Libras utilizando uma Rede Neural Convolucional (CNN) desenvolvida com TensorFlow e Keras. O modelo é treinado com imagens de mãos representando diferentes letras e tem como objetivo traduzir sinais de Libras para texto escrito.

---

## **Estrutura do Repositório**

```
├── dataset/
│   ├── train/  # Imagens para treinamento
│   ├── test/   # Imagens para teste
├── modelo_libras.h5  # Modelo treinado salvo
├── notebooks/
│   ├── treinamento_modelo.ipynb  # Notebook para treinamento
│   ├── visualizacao_graficos.ipynb  # Notebook para visualização de gráficos
├── README.md
```

---

## **Funcionalidades**

- **Treinamento do Modelo**: Rede Neural Convolucional configurada para identificar letras do alfabeto em Libras a partir de imagens.
- **Avaliação de Desempenho**: Cálculo de acurácia e matriz de confusão para avaliar o modelo.
- **Visualizações**: Gera gráficos para interpretação do desempenho e distribuição do conjunto de dados.

---

## **Requisitos**

- Python 3.9+
- TensorFlow 2.17.1
- Bibliotecas adicionais:
  - NumPy
  - Matplotlib
  - Seaborn
  - Scikit-learn
  - Pandas

---

## **Configuração do Ambiente**

1. **Crie um ambiente Conda**:

   ```bash
   conda create --name libras_env python=3.10.12
   conda activate libras_env
   ```

2. **Instale as Dependências**:

   ```bash
   pip install tensorflow==2.17.1 numpy matplotlib seaborn scikit-learn pandas
   ```

3. **Execute os Notebooks**:
   Navegue até a pasta `notebooks/` e abra os notebooks no Jupyter ou Google Colab.

---

## **Treinamento do Modelo**

O modelo é treinado utilizando o conjunto de dados organizado em duas pastas: `train` e `test`. Cada pasta contém subpastas correspondentes a cada letra do alfabeto em Libras.

**Exemplo de Treinamento:**

```python
history = model.fit(
    train_dataset,
    validation_data=validation_dataset,
    epochs=10
)
```

O modelo treinado é salvo em `modelo_libras.h5` e pode ser carregado posteriormente para inferência, sem a necesidade de um treinamento novamente.

---

## **Gráficos Gerados**

1. **Matriz de Confusão**:
   Ajuda a visualizar erros e acertos do modelo por classe.

2. **Acurácia ao Longo do Treinamento**:
   Registra como o modelo se comportou ao longo do treino e validação.

3. **Proporção de Acertos e Erros**:
   Mostra a taxa de sucesso do modelo.


---

## **Uso do Modelo Treinado**

Para carregar e usar o modelo salvo:

```python
from tensorflow.keras.models import load_model

# Carregar o modelo
modelo = load_model("modelo_libras.h5")

# Fazer previsões
predicoes = modelo.predict(novas_imagens)
```

Certifique-se de que a versão do TensorFlow seja compatível com o modelo salvo.

---

## **Contribuições**

Contribuições são bem-vindas! Caso deseje adicionar novas funcionalidades ou melhorar o código, sinta-se à vontade para criar um pull request.

---

## **Licença**

Este repositório está licenciado sob a MIT License. Veja o arquivo `LICENSE` para mais detalhes.

---