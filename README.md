# 🎮 Análise e Clusterização de Jogos da Steam

Este projeto realiza **análise exploratória, preparação de dados e clusterização** em um conjunto com mais de **41 milhões de avaliações de jogos** da plataforma **Steam**, utilizando algoritmos como **K-Means** e **DBSCAN**, além de **PCA** para redução de dimensionalidade.  
O objetivo é identificar **padrões de jogos**, entender a **popularidade**, **qualidade percebida** e **perfil de mercado** na plataforma.

## 📌 Objetivos
- Explorar e preparar dados de jogos disponíveis na Steam.
- Aplicar técnicas de clusterização para identificar grupos com características semelhantes.
- Avaliar a qualidade dos agrupamentos usando métricas como **Silhouette Score**.
- Gerar insights úteis para **análise de mercado** e **decisões estratégicas**.

## 📊 Dataset
- **Fonte:** [Kaggle - Game Recommendations on Steam](https://www.kaggle.com/datasets/antonkozyriev/game-recommendations-on-steam)
- **Período:** 15/10/2010 a 31/12/2022  
- **Arquivos principais:**
  - `games.csv` → Informações sobre os jogos (preço, avaliações, plataformas, etc.).
  - `recommendations.csv` → Avaliações dos jogos.
  - `users.csv` → Perfil dos usuários que avaliaram.
  - `games_metadata.json` → Descrição e tags dos jogos.

## 🛠️ Metodologia
1. **Data Understanding**
   - Análise exploratória (EDA) com visualizações e estatísticas descritivas.
   - Identificação de variáveis relevantes.
2. **Data Preparation**
   - Limpeza de dados e conversão de tipos.
   - **One-Hot Encoding** de variáveis categóricas (ex.: ratings).
   - Testes com inclusão e exclusão de tags.
3. **Modelagem**
   - **Normalização** dos dados (`StandardScaler`).
   - **PCA** para redução de dimensionalidade.
   - **K-Means** → Testes com diferentes valores de `k`.
   - **DBSCAN** → Ajuste de parâmetros (`eps`, `min_samples`).
4. **Avaliação**
   - **Silhouette Score** para medir separação dos clusters.
   - Análise qualitativa dos grupos formados.

## 🚀 Principais Resultados
- Melhor desempenho com **dados numéricos do `games.csv` e ratings**, resultando em **Silhouette Score ≈ 0.62**.
- Identificação de **10 clusters** com perfis distintos, como:
  - Jogos **excelentes e populares**.
  - Jogos **muito mal avaliados, mas famosos**.
  - **Boas oportunidades escondidas** (alta avaliação, baixa popularidade).
  - Jogos **com ótimo custo-benefício** (bom desconto e avaliação positiva).
- Inclusão das tags não melhorou os resultados de clusterização.

## 📈 Exemplos de Insights
- Alta correlação entre **crescimento de jogos indie** e **redução de preço médio**.
- Jogos para **Steam Deck** estão entre os mais bem avaliados.
- Preço médio dos jogos aumentou significativamente após 2021.

