# world-cup-data-eras
# Evolução Histórica da Copa do Mundo: Análise de Eras

Este projeto aplica conceitos de **Aprendizado Não Supervisionado** para analisar a evolução histórica de todas as edições da Copa do Mundo da FIFA. O objetivo foi identificar e segmentar as diferentes "Eras" do torneio com base na dinâmica e estrutura de performance do futebol ao longo do tempo.

### O que eu fiz e por quê?
Em vez de analisar a história do futebol por intuição humana, deixei que os dados contassem a história. Utilizando dados históricos consolidados (via Kaggle), processei métricas fundamentais de cada edição: **volume de gols marcados**, **total de partidas jogadas** e a **quantidade de seleções participantes**.

Após tratar e padronizar os dados com `StandardScaler` (essencial para equilibrar variáveis com escalas tão diferentes), apliquei os algoritmos **K-Means** e **Agrupamento Hierárquico (Dendrograma)** para descobrir padrões ocultos na evolução do esporte. Para validar os clusters, utilizei métodos matemáticos como o *Elbow Method*, *Silhouette Score* e o *Coeficiente de Correlação Cofenética*.

### Resultados e Insights
O algoritmo reconstruiu com precisão a linha do tempo do futebol, dividindo o torneio de forma orgânica em 4 grandes Eras:

* **Era Romântica:** Edições antigas com pouquíssimos jogos e seleções, mas com uma média de gols por partida avassaladora.
* **Era de Ouro da Estabilização:** O clássico e longevo formato consolidado com 16 seleções.
* **Era de Expansão Global:** A transição e abertura do torneio para o formato de 24 seleções.
* **Era dos Megaeventos Modernos:** O modelo de 32 seleções (64 partidas), caracterizado por uma estrutura massiva de entretenimento e alto volume total de gols.

O projeto traz análises visuais ricas, incluindo mapas de calor (*Heatmaps*) dos centróides de cada grupo e uma **visualização interativa em 3D** (via Plotly) para explorar o posicionamento de cada Copa do Mundo dentro de seu respectivo cluster.

---
*Tecnologias utilizadas: Python, Pandas, Scikit-Learn (KMeans, PCA), SciPy (Dendrogram), Seaborn e Plotly.*
