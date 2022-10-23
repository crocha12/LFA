# AFD
## Relatório Técnico

### Como o Algoritmo foi projetado?
Basicamente o algoritmo teve como base o algoritmo 1, porém foi adicionado uma classe com nome State buscando facilitar a visualização, utilização e implementação dos estados e suas transições, a classe possui os atributos: code que representa o nome do estado, isFinal para identificar se é um estado final e transitions que é um dicionário contendo todas as possíveis transições do estado, onde as chaves são os símbolos e o valor é uma lista de estados, ou seja, uma forma de guardar as possíveis transições. Além disso, ela possui os métodos symbolExists para verificar a existência do símbolo em transitions e addTransition para adicionar as transições.
 
### Estruturas de dados utilizadas

No algoritmo utilizamos listas para guardar os símbolos das palavras e os estados, e o dict para guardar as transições de cada estado.


### Como foi gerenciado o não determinismo?

No algoritmo 1, ou seja, AFD, era feito a mudança de estado com apenas uma variável 'e', já nesse algoritmo foi utilizado uma lista 'E' contendo todos os estados em que o AFN pode se encontrar com base nos símbolos das palavras e seu não determinismo, de forma geral, existe uma lista externa E que inicia com o estado inicial apenas, em seguida entra no laço da palavra que para cada simbolo da palavra é guardado em uma lista auxiliar chamada Next todos os possíveis próximos estados com base nas transições do símbolo, por fim ao término de cada iteração os estados de Next são passados para 'E' e a lista Next é zerada ao término de toda iteração, no final é verificado se alguns dos estados presentes na lista E é reconhecido pelo AFND.
