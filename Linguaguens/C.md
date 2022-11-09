### Sumário
* [C++](#c)
* [C](#c-1)


# Paradigmas da Programação
* Imperativo - máquina de turing
     * Davam comandos de passo a passo do que a máquina teria que fazer
     * Geravam códigos muito grandes, logo, era um código de difícil manuntenção
* Procedural - aqui surge as funções/métodos, o que diminui o tamanho do código
* Estrutural - surgue condicionais, loops, diminuindo mais ainda o tamanho do código
* Orientado a objetos - trazer o mundo real para a programação, aqui surge as classes e os conceitos de objeto (polimorfismo, herança, encapsulamento)
# Paradigmas Declarativos
* Se preocupam em como fazer, e não como foi feito
* Programação Funcional - surgiu para ser mais rápida que a p.o.o
* Programação Lógica
* Linguagens de marcação
     * HTML, XML, SQL
# C++
* Linguagem multiparadigma
     * Paradigma da programação procedural
          * Tudo que está dentro da função main vai ser executada de forma sequêncial
     * Paradigma da programação orientada a objetos
## Variáveis
### Tipagem
* Estática - é preciso atribuir o tipo primitivo de dado à variável
### Tipos Primitivos
* Também conhecidos como tipos de dados
* Armazenam só 1 valor por variável, por isso são chamados de tipos de dados simples
* `string` nome = "Pedro";
     * è necessário incluir biblioteca
     ```bash
     #include <string>
     ```
* `int` numeroInteiro = 10;
* `float` numeroFlutuante1 = 1.6235; 
     * precisão de +- 6 casas decimais;
* `double` numeroFlutuante2 = 1.6235; 
     * precisão de +- 10 casas decimais;
* `char` sexo = 'M';
* `bool` escolha = true;
### Boas Práticas
* Recomenda-se que a declaração de variáveis sejam as primeiras intruções da função 
## Entrada e Saída de Dados
* Incluir biblioteca :
```bash
#include <iostream>
using namespace std;
```
### Saída
* Função : `cout` <<;
```bash
#include <iostream>
using namespace std;

int main() {
     cout << "Olá mundo !";
}
```
### Entrada
* Função : `cin` >>;
```bash
#include <iostream>
#include <string>
using namespace std;

int main() {
     string nome;

     cout << "Escreva seu nome : ";
     cin >> nome;

     cout << "Seu nome é : " << nome;
}
```
## Condicionais
* if...else if...else
* switch() {case : ;}
## Laços de Repetição
* for
* while
* do...while
# C
## Entrada e Saída de Dados
* Incluir biblioteca :
```bash
#include <stdio.h>
```
### Saída de Dados
* Função : `printf();`
* Sintaxe : `prinft("string de controle", arg1,arg2,...);`
* Na string de controle do prinft() pode conter :
     * texto
     * códigos especiais
          * \n - pular linha
          * \t - tab
     * formatos - relacionados aos argumentos
```bash
#include <stdio.h>

int main() {
     printf("Olá mundo !");
}
```
### Entrada de Dados
* Função : `scanf();`
* Sintaxe : scanf(`"string de controle"`, `&variável`);
* Na string de controle do scanf() pode conter : 
     * formatos
```bash
#include <stdio.h>

int main() {
     char nome[15];

     printf("Digite seu nome : ");
     scanf("%s", nome);

     printf("Seu nome é : %s", nome);
}
```
* Não se deve utilizar o `&` com `vetores` - os colchetes indicam vetores
     ```bash
     char nome[15];
     
     scanf("%s", nome);
     ```
## Variáveis
* Variável Global
* Variável de Parâmetro
* Variável Local
### Tipagem
* Estática
### Tipos Primitivos
* Também conhecidos como tipos de dados
* Armazenam só 1 valor por variável, por isso são chamados de tipos de dados simples
* `char` - formato `%c`
     ```bash
     char letra = 'P';
     ```
     * string - formato `%s`
          ```bash
          char nome[] = "Pedro";
          ```
          * È possível específicar o número de caracteres no [ ] da variável `nome`
          * Em C, uma string é uma array de caracteres concatenado
* `int` - formato `%d`
     ```bash
     int numeroInteiro = 10;
     ```
* `float \ double` - formato `%f`
     ```bash
     float numeroFlutuante1 = 10.222;
     double numeroFlutuante2 = 10.2222222;
     ```
* void - não possui valor
     * utilizado para indicar que uma função não possui valor
### Onde Declarar
```bash
#include <stdio.h>

int resultado; // variável global

int multiplicacao (int n1, int n2) { # variáveis de parâmetro
     int produto; # variável local
     
     produto = n1 * n2;
     return produto; # funções de tipo primitivo requerem um retorno
} 

int main() {
     resultado = multiplicacao(10, 500);
     printf("%d", resultado);
}
```
### Qualificadores
* Na declaração, precedem o tipo primitivo
     * `short`
     * `long`
     * `unsigned`
     * `signed` - default
```bash
unsigned int valor;
```
* C permite que o programa defina se uma variável de tipo numérico deva ou não reservar o bit de sinal (números negativos)
```bash
unsigned int; # não reserva o bit de sinal
signed int; # reserva o bit de sinal
```
* Se nenhum modificador for indicado, por default, o compilador C reservará o bit de sinal
## Constantes
* È semelhante a uma variável, exceto que seu valor armazenado é imutável(constante)
```bash
#include <stdio.h>

int main() {
     const int i = 10;
     prinft("%d", i);
}
```
```bash
#include <stdio.h>

int main() {
     const int i = 10;
     i = 20;
     printf("%d", i);
}
$ERROR
```
## Arrays - Vetores
* Permite armazenar dados de uma mesmo tipos primitivo a uma variável, que, neste caso, será chamada de array
     * A quantidade de dados são conhecidas como `length`(tamanho) ou posições
     * E cada dado pode ser acessado por um índice
     * A contagem de índices começa do 0...(tamanho - 1)
### Sintaxe
```bash
<tipo-prmitivo> <nome-vetor>[tamanho] = {dado1, dado2,...};
```
* Caso não se especificar o tamanho máximo do array, ao atribuir, o compilador irá alocar o espaço suficiente para armazenar todos os valores
```bash
int numeros[5] {40, 60, 50, 30, 40}
```
```bash
int numeros {4, 7, 12, 52}
```
```bash
#include <iostream>
#define qtdAlunos 20

int main() {
     float nota[qtdAlunos], soma;

     for (int i = 0; i < qtdAlunos; i++) {
          printf("");
          scanf("f", &nota[i]);
          soma = soma + nota[i];
     }
     printf("Média da disciplina = %f", soma);
}
```
## Matrizes
* Estrutura de dados homogênea, a qual cada elemento pode ser acessada por dois índices
     * Dividida em `colunas`(eixo y) e `linhas`(eixo x)
     * A contagem dos índices vai de 0...(tamanhoColunas - 1)
### Sintaxe - como declarar
```bash
<tipo-primitivo> <nome-matriz>[tamanhoColunas][tamanhoLinhas];
```
```bash
int numeros[3][5] {1,2,3,4,5} {1,2,3,4,5} {1,2,3,4,5};
```
* Foram alocadas 3 colunas, as quais acoplam 5 linhas

## Funções
### Sintaxe - como declarar
* <'retorno> <nome-função> (parâmetros) {}
### Prática
* Função que calcula as raizes da equação do segundo grau
```bash
#include <stdio.h>
#include <math.h>

int main() {
    int a, b, c;

    printf("Digite o valor de a: ");
    scanf("%d", &a);
    
    printf("Digite o valor de b: ");
    scanf("%d", &b);
    
    printf("Digite o valor de c: ");
    scanf("%d", &c);
    
    void calcularEquacao(int a, int b, int c) {
        int x1, x2, delta;
        delta = b * b - 4 * a * c;
        x1 = (-b + sqrt(delta)) / 2;
        x2 = (-b - sqrt(delta)) / 2;
        printf("As soluções dessa equação é: %d e %d", x1, x2);
    }
    
    calcularEquacao(a, b, c);
}
```
* `sqrt` é uma função da biblioteca <math.io> que permite calcular a raiz quadrada
### `fgets`
* Específica para leitura de string ao invés do scanf()
* Sintaxe : fgets(variável, número-max-de-caracteres, stdin);
```bash
#include <stdio.h>

int main() {
char nome[15];

printf("Escreva seu nome : ");
fgets(nome, 15, stdin);

printf("Seu nome é : %s", nome);
}

```
### `sizeof`
* Função que imprimi a quantidade de bytes armazenáveis

## Diretiva de Pré-Processamento
* No pré-processamento ocorre a substituição
```bash
#include <stdio.h>
#define pi 3.1416   // diretiva

int main() {
     float raio; 
     printf("Para que possa ser calculado a área e o comprimento do círculo, informe o raio : ");
     scanf("%f", &raio);
    
     float area = pi * raio * raio, comp = 2 * pi * raio;
     printf("O círculo possui área e comprimento de, respectivamente, %.2f e %.2f", area, comp);
}
```

## Struct
* Permite armazenar dados de diferentes tipos primitivos a uma variável, que, neste caso, será chamada de struct
### Sintaxe - como declarar uma struct
* Modo 1
     * <'struct> <'nome-struct> {}(aqui ficam as declarações e atribuições);
* Modo 2
     * <'typedef> <'struct> {}<'nome-struct>;  
### Prática
* Modo 1
```bash
struct pessoa {
char nome[20];
int idade;
float altura;
} p1 = {"Pedro", 19, 1.67},
p2 = {"Alice", 23, 1.60};

printf("Nome: %s\nIdade: %dz\nAltura: %f", p1.nome, p1.idade, p1.altura);
```
* Trocar o valor da variável do tipo string de uma struct: `strcpy`
     * strcpy(struct.variável, "nova string");
```bash
strcpy(p2.nome, "Joana");
```
* Troca-se qualquer outra variável que não seja do tipo string normalmente
```bash
p2.idade = 26;
```
* Para imprimir todos as variáveis de uma struct, recomenda-se criar uma função
```bash
void imprimir() {
     printf("Nome: %s\nIdade: %d\nAltura: %f", p1.nome, p1.idade, p1.altura);
}
```
### Typedef
* Usado para redefinir o nome do tipo primitivo
```bash
typedef int inteiro
inteiro x = 10;

printf("O valor de x é: %d", x);
```
* Modo 2
```bash
typedef struct {
     char nome[20];
     int idade;
     float altura;
}pessoa;

// declaração
pessoa p1, p2;

// atribuição
p1.nome = "Pedro";
p1.idade = 19;
p1.altura = 1.67;
```
* Array do tipo struct
```bash
typedef struct {
float nota
char nome[15];
char disciplina [20];
}aluno;

// declaração
aluno a1;

for(int i = 0; i < 5; i++) {
     srtcpy(cleitinho[i].nome,"CLEITINHO A MÍDIA");
     srtcpy(cleitinho[i].disciplina,"ESTRUTURA DE DADOS EM C");
     cleitinho[i].nota = 10;
}

// impressão
for(int i = 0; i < 5; i++) {
     printf("\nO Nome do aluno é: %s", cleitinho[i].nome);
     printf("\nA disciplina do curso é: %s", cleitinho[i].disciplina);
     printf("A nota do aluno é: %.2f", cleitinho[i].nota);
}
```
* Struct dentro da struct
```bash
typedef struct {
 int hora, minutos, segundos
}horario;

typedef struct {
     int dia, mes, ano;
}data;

typedef struct {
horario hrs, # hrs erda tudo de horario
data date, # date herda tudo de data
char descricao[30];
}compromisso;

// declaração
compromisso reuniao;

//atribuição dos valores da struct
reuniao.hrs.hora = 8;
reuniao.hrs.minutos = 16;
reuniao hrs.segundos = 20;
reuniao.date.dia = 20;
reuniao.date.mes = 03;
reuniao.date.ano = 2022;
reuniao.descricao = "reunião de marketing";

// impressão
printf("O horário da reunião é %d:%d:%d\n e o assunto abordado será %s", reuniao.hrs.hora, reuniao.hrs.minutos, reuniao.hrs.segundos, reuniao.descricao);
```
* Função `strcpm`
```bash

```