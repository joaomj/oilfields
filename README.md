# **Oilfields**
Repo para o desafio de Data Science com poços de petróleo.

# **O Problema**
A Acme Oil, empresa de especializada em extração de petróleo, decidiu iniar um projeto de análise de dados para obter informações que os auxiliem na tomada de decisões estratégicas.

Foi atribuído a você o desenvolvimento de um modelo de correlações de poços. Este consiste em encontrar poços correlatos, ou seja, poços que tenham características semelhantes.

Será fornecido a você um conjunto de dados de um poço de petróleo ("valor de entrada"). Você deve informar uma lista com os poços mais semelhantes ao informado. Desenvolva um modelo treinado nos dados fornecidos que retorne uma lista com os 04 poços mais semelhantes ao poço do valor de entrada.

# **Solução**
Lendo o enunciado, percebe-se que este trata de um problema de **clusterização**, isto é, de agrupamento de itens semelhantes. É muito importante conhecer o tipo de problema antes de começar a programar, pois este reconhecimento vai determinar quais algoritmos de Machine Learning serão usados (e como o dataset será preparado).

De modo geral, a solução do problema seguiu as seguintes etapas:

1. Carregar dados
2. Limpar dados
3. Tratar dados: desbalanceamento, valores nulos, colunas sem variância
4. Feature Engineering: selecionar features mais importantes
5. Modelagem: 
    - escolher métricas de desempenho; 
    - construir modelo baseline;
    - avaliar modelos; 
    - otimizar modelos;
    - testar modelos otimizados;
    - escolher o modelo com a melhor métrica de avaliação.
6. Gravar Modelo Escolhido

# **Resultados**
Os 04 poços mais semelhantes ao poço informado são:

| nome_do_poco | score_similaridade | ranking_similaridade |
|--------------|---------------------|----------------------|
| 6C5G4M       | 1.00                | 1                    |
| 7021KS       | 0.97                | 2                    |
| 553PEG       | 0.95                | 3                    |
| 4BVJOY       | 0.94                | 4                    |

Os 04 poços mais semelhantes segundo o **modelo KNN**: (precision@K = 25%)

| nome_do_poco | similaridade_knn | ranking_similaridade | score_similaridade |
|--------------|-------------------|----------------------|---------------------|
| 6C5G4M       | 1.0000            | 1                    | 1.0000              |
| 091G7D       | 0.6694            | 9                    | 0.9311              |
| E6Q0PD       | 0.6563            | 11                   | 0.9042              |
| 0WFQ56       | 0.6346            | 7                    | 0.9394              |

Poços mais semelhantes ao poço informado, segundo **Similaridade do Cosseno**: (precision@K = 50%)

| nome_do_poco | similaridade_cosseno | ranking_similaridade | score_similaridade |
|--------------|-----------------------|----------------------|---------------------|
| 6C5G4M       | 1.0000                | 1                    | 1.0000              |
| 091G7D       | 0.9919                | 9                    | 0.9311              |
| 4BVJOY       | 0.9878                | 4                    | 0.9450              |
| 0WFQ56       | 0.9874                | 7                    | 0.9394              |


# **Para reproduzir a solução**

1. Clonar este repositório: `git clone https://github.com/joaomj/oilfields.git`
2. Criar ambiente virtual para este projeto. Eu utilizei o Miniconda em conjunto com o WSL: `conda create --name <nome_do_ambiente>`
3. Instalar dependências: `conda install --yes --file requirements.txt`
4. Execute o Jupyter Notebook. Eu utilizei o Jupyter através do VS Code.

**Atenção:** os datasets do desafio não estão publicados neste repositório porque são privados. Para reproduzir a solução, você precisará de dados fictícios.

# **Responsável**
- **Tech Lead:** João Marcos - ([Linkedin](https://www.linkedin.com/in/joaomj))
- Deixe uma **star** para me ajudar!
