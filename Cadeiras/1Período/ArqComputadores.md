# Dado vs Informação
### Dado
* È a informação em seu estado bruto, ou seja, é a informação não contextualizada
    * Ex : A coleta de opções de *votos* em uma pesquisa eleitoral. São considerados dados
### Informação
* São os dados contextualizados, ou seja, é o resultado do processamento dos dados que podem ser usados na tomada de decisão
    * Ex : Os resultados da apuração dos votos coletado, indicando qual candidato tem a maior chance de ser escolhido
# Informática
* È a utilização de métodos no tratamento automático e racional da informação através da utilização de máquinas (computadores)
# Tecnologia da Informação
* Então a T.I é o conjunto de recursos não humanos dedicados ao : `armazenamento` dados, `processamento` de dados e `comunicação` da informação para executar uma ação 
# Computador
* Aquilo que computa, manipula dados e podem transforma-los em informações através de cálculos
### Computador Analógico
* São equipamentos mecânicos ou elétricos
    * Como a balança e termômetro
### Computador Digital
* São equipamentros eletrônicos
# Origem 
### Memória
* Aqui são armazenados os dados e instruções
### Entrada e Saída de Dados
* Permite ao computador receber e enviar dados
### Unidade de Controle
* Aqui a máquina controla o que está sendo feito
### Unidade Lógica e Aritmética
* Aqui são feitas as operações
# Natureza dos Computadores
### Características Primárias
* Velocidade
* Confiabilidade
* Capacidade de armazenamento
    * Alinhada as 3 caraterísticas primárias, surgem as características secundárias
### Características Secundárias
* Produtividade
* Tomada de decisão
* Redução de custo
# Sistema Informatizado
* Hardware - parte física do sistema informatizado
* Software - conjunto de instruções (algoritmos) a fim de resolver um problema
* Peopleware - pessoas envolvidas no desenvolvimento e utilização do sistema informatizado
## Como Funciona os Computadores
1. Entrada - recebe dados de entrada
2. Processa esses dados
3. Armazena e resgata esses dados
4. Devolve a informação para o usuário
* Em síntese ocorre a `entrada`, `processamento` e `saída de dados`
### Saída e Entrada de Dados
* Periféricos
### Processamento
* CPU (Central Process Unit), conhecido como processador
### Memória Principal
* RAM (volátil) - acessa os dados de forma não sequêncial, a tornando rápida; perde-se os dados ao faltar energia
* ROM (não-volátil) - não há perda de dados ao faltar energia; os dados são guardados apenas uma vez e não podem ser apagados
### Memória Secundária
* HD, SSD, DVD
## Como o Software se Comunica com o Hardware
* Na forma de sinais (pulsos) elétricos
* Cada pulso elétrico é chamado de bit (0 out 1)
* Um conjunto de 8bits = 1byte
    
        OBS : 1byte é o espaço necessário para armazenar 1 caracter
# Conversões
### Sistemas
* Decimal
* Binário 
* Octal
* Hexadecimal
# Lógica Digital
## Algebra Booleana 
* Métodos para simplificar circuitos lógicos
* Exitem apenas 3 operadores : `AND`, `OR` e `NOT`
* Variáveis apresentam apenas 0 ou 1 
* Operadores retornam apenas 0 ou 1
* Apresenta apenas 2 estados : Falso (0) ou Verdadeiro (1)
### Noções
x = jovens; y = faz Ciência da Computação
* (1 - x) representa todos que não são jovens
* (x . y) representa todos os jovens que fazem ciências da computação
* (x + y) representa que é jovem ou faz ciência da computação
* (1 - x)(x . y) representa todos os que não são jovens e faze ciências da computação
### Operações Booleanas Básicas
* Conjunção `^` = `AND` = `.`
    * X ^ Y = XY - Intercessão 
* Disjunção `v` = `OR` = `+`
    * X v Y = X + Y - XY  
* Negação `~` = `NOT`
    * ~X ~Y = (1 - X)(1 - Y)
### Tabela Verdade
* X = 0 ; Y = 0
    * X ^ Y = 0
    * X v Y = 0 
    * ~Y = 1; ~X = 1
* X = 0 ; Y = 1 
    * X ^ Y = 0
    * X v Y = 1 
    * ~Y = 0; ~X = 1
* X= 1 ; Y = 1
    * X ^ Y = 1
    * X v Y = 1 
    * ~Y = 0; ~X = 0
### Exercícios
* 2 + 5 > 4 ^ 3 != 3 -> Falso (0)
* ~(3 != 3) -> Verdadeiro (1)
### Leís da Algebra Booleana
* Comutativa
* Associativa
* Distributiva
### Operadores Lógicos
* `OR`, `AND` e `NOT`