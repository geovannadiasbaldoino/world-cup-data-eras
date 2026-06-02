# world-cup-data-eras
Histórico da Copa do Mundo - Agrupamento e Análise de Eras (K-Means & Hierárquico)
Este projeto aplica algoritmos de Aprendizado Não Supervisionado para analisar a evolução histórica das edições da Copa do Mundo da FIFA. O objetivo principal é identificar e segmentar as diferentes "Eras" do torneio com base em métricas de dinâmica e estrutura de performance do futebol.

- O que o projeto faz (Resumo Técnico)
A partir de dados históricos consolidados de cada edição da Copa do Mundo (extraídos via kagglehub), o script limpa, padroniza e processa as informações para descobrir padrões ocultos na evolução do esporte.

O modelo foca em três variáveis estruturais fundamentais por edição:

Gols Marcados (Volume de bola na rede)

Partidas Jogadas (Duração e tamanho do torneio)

Seleções Participantes (Grau de abertura e expansão da FIFA)

- Etapas de Ciência de Dados Implementadas
Pré-processamento Crítico: Engenharia de atributos com tratamento de strings e aplicação de StandardScaler para garantir que variáveis de escalas diferentes (ex: 170 gols vs 13 seleções) tenham o mesmo peso no cálculo das distâncias euclidianas.

Mapeamento de Perfis (K-Means): Utilização do Método do Cotovelo (Elbow Method) e validação pelo Silhouette Score para definir matematicamente o agrupamento ideal em 4 grandes "Eras Históricas" estáveis do futebol.

Agrupamento Hierárquico: Construção de uma árvore de decisão (Dendrograma) utilizando o critério de Ward e validação de consistência via Coeficiente de Correlação Cofenética, permitindo enxergar a linha do tempo das fusões de perfis de Copas.

Análise de Negócio e Interpretabilidade: Geração de mapas de calor (Heatmaps) dos centróides e desvios padrão para decodificar o perfil médio de cada grupo, além de uma visualização volumétrica 3D interativa em Plotly para exploração dos clusters.

- Principais Insights Encontrados
O algoritmo reconstrói a história do futebol sem qualquer viés humano, dividindo o torneio em:

Era Romântica: Copas antigas com poucos jogos, poucas seleções, mas altíssima média de gols por partida.

Era de Ouro da Estabilização: O formato consolidado de 16 seleções.

Era de Expansão Global: A abertura do torneio para 24 seleções.

Era dos Megaeventos Modernos: O formato atual de 32 seleções, caracterizado por estabilidade de partidas (64) e volume total de gols esmagador.

- Tecnologias Utilizadas: Python, Pandas & NumPy, Scikit-Learn (KMeans, StandardScaler, PCA, Silhouette Score), SciPy (Linkage, Dendrogram, Cophenet), Matplotlib, Seaborn & Plotly (Visualização 3D)
