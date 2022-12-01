# Machine learning applied to data prep - exploratory research over sampling techniques

Este repositório contém dados, e notebooks apresentados no curso de Aprendizado de Máquina (AM) do Instituto Militar de 
Engenharia - IME no terceiro trimestre de 2022.

O emprego de AM em grandes volumes de dados (big data) tem um alto custo computacional (armazenamento, processamento e 
transmissão). Para sua completa execução, o uso de métodos de AM implica em atividades de preparação que antecedem o 
desenvolvimento (definição do problema, identificação de recursos, seleção de algortimo, configuração, treino, testes e avaliação de acurácia) de um modelo de AM.

Estes atividades de preparação, em geral, são as seguintes: 1-Limpeza, 2-Transformação, 3-Integração/Enriquecimento, 4-Balanceamento
de um conjunto de dados, 5-Eliminação manual de atributos, 6-Reduções de dimensionalidades e 7-Amostragem.

Foi selecionada a etapa de Amostragem de Dados para este estudo exploratório por impactar diretamente nos custos
computacionais já mencionados. A redução destes custos permite, por exemplo, que um analista de dados execute diversas técnicas
de AM sobre uma mesma amostra, ou realize uma ampla validação cruzada, com tempo e custos reduzidos. Para isto, é necessario que 
a amostra seja confiável, ou seja, estatisticamente representativa e apresente resultados semelhantes de acurácia do conjunto de
dados, quando as mesmas técnicas forem aplicadas.

Para este estudo exploratório, as seguintes atividades foram realizadas:

- 1 - Um levantamento de técnicas de sampling (Amostragem Aleatória Simples (AAS), 
Amostragem Sistemática (AS), Amostragem por Conglomerados ou Clusters (AC), Amostragem Ponderada (AP) Amostragem 
Estratificada (AE)) e seus respectivos códigos em python (1 - Seleção e testes de tecnicas de sampling.ipynb);

- 2 - A seleção de um caso real de aprendizado de máquina que compara diversas técnicas de AM (Support vector regression, Decision tree, Random forest e Layer dense neural network) através de curvas REC 
(Regression Error Characteristic (REC) estimation - Estimativa da Característica de Erro  de Regressão) e erros médios 
quadráticos (RMSE). (2 - Seleção de Casos - 1 - Forrest Fire.ipynb)
#### (A Data Mining Approach to Predict Forest Fires using Meteorological Data. In J. Neves, M. F. Santos and J. Machado Eds., New Trends in Artificial Intelligence, Proceedings of the 13th EPIA 2007 - Portuguese Conference on Artificial Intelligence, December, Guimaraes, Portugal, pp. 512-523, 2007. APPIA, ISBN-13 978-989-95618-0-9 - Acesso em 24.nov.22: http://www.dsi.uminho.pt/~pcortez/fires.pdf - Acesso em 24.nov.22: [Cortez and Morais, 2007].) ####

- 3 - Em seguida, aos dados deste caso real foram aplicados as técnicas de sampling mencionadas (3.1 - Forrest Fire e AMOSTRAGENS.ipynb).

- 4 - Aplicação das técnicas de AM nas amostragens (3.2.0 - Forrest Fire - Original.ipynb, 3.2.1 - Forrest Fire - Amostra Aleatoria Simples - COM reposição.ipynb, 3.2.2 - Forrest Fire - Amostra Aleatoria Simples - SEM reposição.ipynb, 3.2.3 - Forrest Fire - AMOSTRAGEM SISTEMÁTICA (AS).ipynb, 3.2.4 - Forrest Fire - Amostragem por Conglomerados ou Clusters (AC).ipynb, 3.2.5 - Forrest Fire - Amostragem Ponderada.ipynb, 3.2.6 - Forrest Fire - Amostragem Estratificada (AE).ipynb)

- 5 - Comparação das curvas REC e RMSE, entre os resultados das tecnicas de AM no dataset e suas amostras.

Os resultados apontaram, inicialmente, que para cada método de AM há uma técnica de amostragem mostrou-se mais assertiva.

Curvas REC
![curvas rec](https://user-images.githubusercontent.com/69159671/204885003-7d74ee48-9b64-43ed-ae71-4dd4032a8c84.png)

RMSE
![comparativo_RMSE](https://user-images.githubusercontent.com/69159671/204885087-22e9c240-c8e8-4295-94a1-64407e00a268.png)

## Conclusões e sugestões de trabalhos futuros:

Os resultados são preliminares mas possibilitaram alcançar alguns objetivos, conforme abaixo:

##### - Identificação das etapas e sequencia de atividades de preparação de dados
##### - Revisão literária avaliando o uso de diferentes técnicas de amostragem
##### - Aplicação das técnicas selecionadas de amostragem utilizando o Python, em um caso real
##### - Comparação do emprego das técnicas de amostragem em diferentes métodos de AM

Diversos pontos neste trabalho, foram limitados, para atender aos prazos disponbilizados para a execução deste trabalho. Abaixo, algumas sugestões para aprofundar estes estudos:

- Revisão literária mais ampla acerca das etapas e sequencia da preparação de dados
- Revisão das técnicas de amostragem e dos códigos de implantação em Python
- Ampliação dos testes de acurácia para comparação dos resultados da implantação de AM no conjunto de dados e amostras
- Evolução dos codigos de implantação dos métodos de AM para uso de validação cruzada
- Aplicação destes notebooks em outros conjuntos de dados, em especial com maior e menor incidência de outliers e com maior número de registros
- Emprego destes conjunto de técnicas de amostragem e métodos de AM em dados armazenados em NoSQL, com uso de SPARK para procesamento de ML (SparkML)
