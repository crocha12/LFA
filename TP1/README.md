# AFD
## Relatório Técnico

### Como o Algoritmo foi projetado?

O algoritmo foi desenvolvido utilizando como ideia o 'Algoritmo para simular AFDs' - do material da disciplina(Slide: Capitulo 2, pagina 26), basicamente o algoritmo é composto por um for que itera sobre cada palavra na lista de palavras, dando início ao laço principal do algoritmo para cada uma das iterações o estado inicial é inferido pelo valor fornecido na entrada de dados em seguida iniciamos o algoritmo verificando cada letra da palavra para ocorrer ou não uma mudança de estado no algoritmo, em caso onde não existe uma transição pré-definida vinculada ao estado entramos no estado de erro, e estando no estado de erro automaticamente o AFD não deve reconhecer a palavra, logo  sairemos do laço das letras contida na palavra e retornamos 'N', caso contrario, o algoritmo seguirá verificando as letras da palavra até o fim da mesma, em seguida o algoritmo deve verificar se o estado atual está presente nos estados finais, caso sim o AFD reconhece a palavra e o algoritmo retorna 'S' para a palavra específica, caso não é retornado 'N'.
 
### Estruturas de dados utilizadas

Para a implementação do algoritmo foi utilizado as estruturas de dados: list e dict do python, list foi utilizado para armazenar as palavras e os estados finais, enquanto a estrutura dict foi utilizada para guardar os estados como 'chave' e um objeto contendo as possíveis transições como 'valor', sendo esse valor também um dicionário, onde a 'chave' representa uma letra e o 'valor' o próximo estado.

### Como possui complexidade O(|w|)

O algoritmo possui complexidade O(|w|) pois só existe uma iteração sobre a palavra, e o objetivo de utilizar o dicionario foi pelo fato de ele utilizar uma estrutura similiar a um hashmap que possue uma complexidade O(1) o que não aumenta o tamanho da complexidade do algoritmo.
