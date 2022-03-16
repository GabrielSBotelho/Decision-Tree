# Árvore de Decisão

A árvore de decisão é um algoritmo supervisionado (ou seja, os dados estão rotulados) , sendo usado principalmente para problemas de classificação.  A árvore de decisão tem como característica o processo de *dividir para conquistar.* Ela segue a abordagem *de cima para baixo*, pois ela é construída do nó pai indo até os nós terminais. A árvore de decisão faz parte dos algoritmos *greedy*, pois ela tem como foco apenas a divisão atual sem se preocupar com a próxima.  Uma árvore de decisão tem a seguinte representação

- Nó raiz: população inteira ou amostra
- Nó de decisão: contém um teste para algum atributo
- Nó de término (nó folha): está associado a uma classe (no caso de classificação) ou a um valor contínuo (no caso de regressão).

### Árvore de Regressão

- Variável dependente contínua
- O valor obtido pelos nós terminais nos dados de treinamento é a resposta média **(por padrão, podendo ser alterado para mediana) da observação que caí nessa região.

### Árvore de Classificação

- Variável dependente categórica
- O valor (classe) obtido pelo nó terminal nos dados de treinamento é a moda das observações que caem nessa região.

## Construção de uma Árvore de Decisão

A construção da árvore de decisão tem como objetivo executar uma sequência de divisões de cima para baixo a fim de criar nós terminais em que as classes estão bem separadas (classificação) ou o erro quadrático médio é pequeno (regressão). Desta forma, para construir uma árvore de decisão é necessário seguir os seguintes passos

1. Escolher um atributo
2. Estender a árvore adicionando ramos de acordo com a partição.
3. Passar os exemplos para os nós (tendo em conta o valor do atributo escolhido)
4. Avaliar o critério de parada

### Critérios para escolha do atributo

O critério utilizado para realizar as partições é o da utilidade do atributo para a classificação/regressão. Tendo em vista que um atributo que não realiza boas divisões, atrapalha o desempenho do modelo.

### Medidas de Partição

A maioria dos algoritmos de indução de árvores de decisão trabalha com funções de divisão univariável, ou seja, cada nó interno da árvore é dividido de acordo com um único atributo. Os critérios de seleção para a melhor divisão são baseados em diferentes medidas, tais como, impureza, distância e dependência.
