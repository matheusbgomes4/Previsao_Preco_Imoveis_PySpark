# 🏡 Previsão de Preço de Imóveis com PySpark (Regressão)

Este projeto utiliza técnicas de regressão com **PySpark (MLlib)** para prever o preço de venda de imóveis com base em variáveis como número de quartos, área útil, localização, entre outras.  
Trata-se de um projeto hands-on desenvolvido no **Google Colab**, simulando um caso real de precificação no setor imobiliário.

---

## 🎯 Objetivo

Construir um modelo de regressão, utilizando **Random Forest** e validação cruzada para prever o preço de imóveis, com base em dados estruturados.

---

## 📁 Variáveis Utilizadas (exemplo)

| Variável           | Tipo    | Descrição                       |
|--------------------|---------|---------------------------------|
| `bedrooms`         | int     | Número de quartos               |
| `bathrooms`        | float   | Número de banheiros             |
| `sqft_living`      | int     | Área útil do imóvel (pés²)      |
| `sqft_lot`         | int     | Tamanho do terreno (pés²)       |
| `floors`           | float   | Número de andares               |
| `zipcode`          | string  | Localização do imóvel (CEP)     |
| `price` (target)   | float   | Valor do imóvel (em dólares)    |

---

## ⚙️ Tecnologias e Ferramentas

- Python 3.x  
- PySpark (Spark MLlib)  
- Google Colab  
- RandomForestRegressor  
- ParamGridBuilder + CrossValidator  
- Regressão com avaliação via RMSE, MAE e R²

---

## 🛠️ Etapas do Pipeline

1. **Pré-processamento**
   - Conversão de tipos
   - `StringIndexer` para variáveis categóricas (`zipcode`)
   - `VectorAssembler` e `StandardScaler`
2. **Modelagem**
   - `RandomForestRegressor`
   - Ajuste de hiperparâmetros com `ParamGridBuilder`
   - Validação cruzada com `CrossValidator` (k=3)
3. **Avaliação**
   - Métricas de desempenho: RMSE, MAE e R²

---

## 📊 Resultados do Modelo

| Métrica | Resultado aproximado |
|---------|-----------------------|
| RMSE    | 131 837               |
| MAE     | 80 832                |
| R²      | 0.70                  |

---
