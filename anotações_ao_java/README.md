# JAVA Variáveis

- **int** = É usado para representar números inteiros. Ele ocupa 4 bytes (32 bits) na memória e pode armazenar valores no intervalo de -2.147.483.648 a 2.147.483.647

  - #### Características do **`int`** em Java:

    - **Tipo primitivo:** Não é um objeto, mas um tipo simples usado para eficiência.
    - **Padrão de inicialização**: Dentro de classes, a variável `int` é inicializada como **0** por padrão (se for um campo de instância).
    - **Boxing e Unboxing**: Pode ser convertido automaticamente para um objeto da classe **`Integer`** (autoboxing) e vice-versa (unboxing).

    #### Exemplo com autoboxing:

    public class Main {
        public static void main(String[] args) {
            int numero = 10;
            Integer numeroBoxed = numero; // Autoboxing
            int numeroUnboxed = numeroBoxed; // Unboxing

            System.out.println("Número autoboxed: " + numeroBoxed);
            System.out.println("Número unboxed: " + numeroUnboxed);
        }
    }



- **byte** = É usado para representar números inteiros de 8 bits com sinal. É o menor tipo inteiro disponível e é útil quando se quer economizar memória em situações que envolvem grandes quantidades de dados pequenos.

  - ### Características do byte:

    - Tamanho: 1 byte (8 bits).
    - Intervalo de valores: de -128 a 127
    - Tipo primitivo: Não é um objeto; oferece maior desempenho e ocupa menos memória.
    - Valor padrão: 0 (se não for explicitamente inicializado, em contextos como campos de classe).

    #### Exemplo de uso:

    public class Main {
        public static void main(String[] args) {
            byte idade = 25; // Declarando e inicializando um byte
            System.out.println("Idade: " + idade);

            // Operações com byte
            byte soma = (byte) (idade + 5); // É necessário fazer o casting em operações
            System.out.println("Idade daqui a 5 anos: " + soma);
        }
    }

    

 - **short** = É usado para representar números inteiros de 16 bits com sinal. É útil quando é necessário um intervalo maior que **`byte`**, mas menor que **`int`**, economizando memória em situações específicas.

   - #### Características do **`short`**:

     - **Tamanho**: 2 bytes (16 bits).
     - **Intervalo de valores**: de **-32.768** a **32.767** (ou seja, de −215-2^{15}−215 a 215−12^{15} - 1215−1).
     - **Tipo primitivo**: Não é um objeto; oferece melhor desempenho.
     - **Valor padrão**: `0` (quando não explicitamente inicializado em campos de classe).

     #### Exemplo de uso:

     public class Main {
         public static void main(String[] args) {
             short anoAtual = 2025; // Declarando e inicializando um short
             System.out.println("Ano atual: " + anoAtual);

             // Operações com short
             short proximoAno = (short) (anoAtual + 1); // Necessário casting em operações
             System.out.println("Próximo ano: " + proximoAno);
         }
     }

     

- **long** = É usado para representar números inteiros de 64 bits com sinal. Ele é ideal para armazenar valores inteiros muito grandes que ultrapassam o limite do tipo **`int`**.

  - #### Características do **`long`**:

    - **Tamanho**: 8 bytes (64 bits).

    - **Intervalo de valores**: de **-9.223.372.036.854.775.808** a **9.223.372.036.854.775.807** (ou seja, de −263-2^{63}−263 a 263−12^{63}-1263−1).

    - **Tipo primitivo**: Oferece desempenho otimizado em comparação com objetos.

    - **Valor padrão**: `0L` (quando não explicitamente inicializado em campos de classe).

      #### Exemplo de uso:

      public class Main {
          public static void main(String[] args) {
              long populacaoMundial = 8000000000L; // Declaração e inicialização de um long
              System.out.println("População mundial: " + populacaoMundial);

              // Operações com long
              long populacaoFutura = populacaoMundial + 100000000L;
              System.out.println("População mundial em 10 anos: " + populacaoFutura);
          }
      }

      

- **float** = É usado para representar números de ponto flutuante com precisão simples, ou seja, números com casas decimais que requerem menos memória do que o tipo **`double`**.

  - #### Características do **`float`**:

    - **Tamanho**: 4 bytes (32 bits).
    - **Intervalo de valores**: Valores aproximados: **±3.40282347E+38** (máximo) a **±1.40239846E-45** (mínimo).
    - **Precisão**: Aproximadamente 7 casas decimais significativas.
    - **Sufixo `f` ou `F`**: Literais do tipo **`float`** devem ter o sufixo `f` ou `F` para diferenciá-los de **`double`**, que é o padrão para números com ponto decimal.
    - **Valor padrão**: `0.0f` (em campos de classe não inicializados explicitamente).

    #### Exemplo de uso:

    public class Main {
        public static void main(String[] args) {
            float preco = 19.99f; // Declarando e inicializando um float
            System.out.println("Preço do produto: " + preco);

            // Operações com float
            float desconto = 5.5f;
            float precoFinal = preco - desconto;
        
            System.out.println("Preço com desconto: " + precoFinal);
        }
    }

    

- **double** = É usado para representar números de ponto flutuante com precisão dupla. Ele é o tipo padrão para valores decimais e é amplamente utilizado quando é necessária maior precisão em cálculos.

  - #### Características do **`double`**:

    - **Tamanho**: 8 bytes (64 bits).
    - **Intervalo de valores**: Máximo: **±1.79769313486231570E+308**. / Mínimo: **±4.94065645841246544E-324**.
    - **Precisão**: Aproximadamente **15-16 dígitos significativos**.
    - **Tipo padrão**: Literais numéricos com ponto decimal são tratados como **`double`** por padrão.
    - **Valor padrão**: `0.0` (para campos de classe não inicializados explicitamente).

    #### Exemplo de uso:

    public class Main {
        public static void main(String[] args) {
            double preco = 199.99; // Declarando e inicializando um double
            System.out.println("Preço do produto: " + preco);

            // Operações com double
            double desconto = 20.55;
            double precoFinal = preco - desconto;
        
            System.out.println("Preço com desconto: " + precoFinal);
        }
    }

    

- **boolean** = É usado para representar valores lógicos que podem ser **`true`** (verdadeiro) ou **`false`** (falso). É amplamente utilizado em controle de fluxo, como em instruções condicionais e loops.

  - #### Características do **`boolean`**:

    - **Tamanho**: Não é definido em termos de bytes, pois depende da implementação da JVM (mas geralmente é tratado como um bit).
    - **Valores permitidos**: Apenas **`true`** ou **`false`**.
    - **Tipo primitivo**: Não pode ser tratado como um número (ao contrário de algumas linguagens que permitem 0 e 1 como valores lógicos).
    - **Valor padrão**: **`false`** (quando não inicializado explicitamente, como em campos de classe).

    #### Exemplo de uso:

    public class Main {
        public static void main(String[] args) {
            boolean estaChovendo = true; // Declaração e inicialização de um boolean
            System.out.println("Está chovendo? " + estaChovendo);

            // Controle de fluxo com boolean
            if (estaChovendo) {
                System.out.println("Pegue um guarda-chuva!");
            } else {
                System.out.println("Aproveite o dia ao ar livre!");
            }
        }
    }

    

- **char** = É usado para representar um único caractere Unicode. Ele pode armazenar letras, dígitos, símbolos ou qualquer outro caractere Unicode, como emojis.

  - #### Características do **`char`**:

    - **Tamanho**: 2 bytes (16 bits).
    - **Valor**: Representa um único caractere Unicode no intervalo de **`\u0000`** (0) a **`\uFFFF`** (65.535).
    - **Valor padrão**: **`\u0000`** (caractere nulo) para campos de classe não inicializados.
    - **Representação**: Literais de **`char`** são definidos entre aspas simples (`'`), como `'A'` ou `'7'`.

    #### Exemplos de uso:

    public class Main {
        public static void main(String[] args) {
            char letra = 'A'; // Declarando e inicializando um char
            char digito = '7';
            char simbolo = '@';
            char unicode = '\u2764'; // Código Unicode para um coração

            System.out.println("Letra: " + letra);
            System.out.println("Dígito: " + digito);
            System.out.println("Símbolo: " + simbolo);
            System.out.println("Unicode: " + unicode);
        }
    }





# JAVA OPERADORES 



## Classificação do operadores

### Atribuição
Representado pelo símbolo de igualdade =.

O operador de atribuição é utilizado para definir o valor inicial ou sobrescrever o valor de uma variável. em Java definimos um tipo, nome e opcionalmente atribuímos um valor à variável através do operador de atribuição. Exemplos abaixo:

#### Exemplo em código

//classe Operadores.java
String nome = "GLEYSON";
int idade = 22;
double peso = 68.5;
char sexo = 'M';
boolean doadorOrgao = false;
Date dataNascimento = new Date();



# Aritméticos

O operador aritmético é utilizado para realizar operações matemáticas entre valores numéricos, podendo se tornar ou não uma expressão mais complexa.

Os operadores aritméticos são: + (adição), - (subtração), * (multiplicação) e / (divisão).

#### Exemplo em código

//classe Operadores.java
double soma = 10.5 + 15.7;
int subtração = 113 - 25;
int multiplicacao = 20 * 7;
int divisao = 15 / 3;
int modulo = 18 % 3;
double resultado = (10 * 7) + (20/4);

**ATENÇÃO! O operador de adição (+), quando utilizado em variáveis do tipo texto, realizará a “concatenação de textos”.**

//classe Operadores.java
String nomeCompleto = "LINGUAGEM" + "JAVA";
		
//qual o resultado das expressoes abaixo?
String concatenacao ="?"; 

concatenacao = 1+1+1+"1";

concatenacao = 1+"1"+1+1;

concatenacao = 1+"1"+1+"1";

concatenacao = "1"+1+1+1;

concatenacao = "1"+(1+1+1);



# Unários

Esses operadores são aplicados juntamente com um outro operador aritmético. Eles realizam alguns trabalhos básicos como incrementar, decrementar, inverter valores numéricos e booleanos.

(+) Operador unário de valor positivo – números são positivos sem esse operador explicitamente;

(-) Operador unário de valor negativo – nega um número ou expressão aritmética;

(++) Operador unário de incremento de valor – incrementa o valor em 1 unidade;

(--) Operador unário de decremento de valor – decrementa o valor em 1 unidade;

(!) Operador unário lógico de negação – nega o valor de uma expressão booleana;

#### Exemplos abaixo:

//classe Operadores.java
int numero = 5;
		
//Imprimindo o numero negativo
System.out.println(- numero);

//incrementando numero em mais 1 numero, imprime 6
numero ++;
System.out.println(numero);

//incrementando numero em mais 1 numero, imprime 7
System.out.println(numero ++);// ops algo de errado não está certo

System.out.println(numero);// agora sim, numero virou 7

//ordem de precedencia conta aqui
System.out.println(++ numero);

boolean verdadeiro = true;

System.out.println("Inverteu " + !verdadeiro);

**Muito cuidado com ordem de precedência dos operadores unários!**



# Ternário

O Operador de Condição Ternária é uma forma resumida para definir uma condição e escolher por um dentre dois valores. Você deve pensar numa condição ternária como se fosse uma condição IF normal, porém, de uma forma em que toda a sua estrutura estará escrita numa única linha.

O operador ternário é representado pelos símbolos ?: utilizados na seguinte estrutura de sintaxe:

<Expressão Condicional>`` 
?
``<Caso condição seja true>``
:
 ``<Caso condição seja false>

#### Exemplos abaixo:

// classe Operadores.java
int a, b;

a = 5;
b = 6;

/* EXEMPLO DE CONDICIONAL UTILIZANDO UMA ESTRUTURA IF/ELSE
if(a==b)
   resultado = "verdadeiro";
else
   resultado = "falso";
*/

//MESMA CONDICIONAL, MAS DESSA VEZ, UTILIZANDO O OPERADOR CONDICIONAL TERNÁRIO
String resultado = (a==b) ? "verdadeiro" : "false";

System.out.println(valor);

**O operador ternário é aplicado para qualquer tipo de valor.**



# Relacionais

Os operadores relacionais avaliam a relação entre duas variáveis ou expressões. Neste caso, mais precisamente, definem se o operando à esquerda é igual, diferente, menor, menor ou igual, maior ou maior ou igual ao da direita, retornando um valor booleano como resultado.

- == Quando desejamos verificar se uma variável é IGUAL A outra.

- != Quando desejamos verificar se uma variável é DIFERENTE da outra.

- > Quando desejamos verificar se uma variável é MAIOR QUE a outra.

- >= Quando desejamos verificar se uma variável é MAIOR OU IGUAL a outra.

- < Quando desejamos verificar se uma variável é MENOR QUE outra.

- <= Quando desejamos verificar se uma variável é MENOR OU IGUAL a outra.

#### Exemplo em código

//classe Operadores.java
int numero1 = 1;
int numero2 = 2;

if(numero1 > numero2)
	System.out.print("Numero 1 maior que numero 2");

if(numero1 < numero2)
	System.out.print("Numero 1 menor que numero 2");

if(numero1 >= numero2)
	System.out.print("Numero 1 maior ou igual que numero 2");

if(numero1 <= numero2)
	System.out.print("Numero 1 menor ou igual que numero 2");

if(numero1 != numero2)
	System.out.print("Numero 1 é diferente de numero 2");jav

### Comparações avançadas

Quando se refere a comparação de conteúdos na linguagem, devemos ter um certo domínio de como o Java trata o armazenamento deste valores na memória.

**Quando estiver mais familiarizado com linguagem, recomendamos se aprofundar no conceito de espaço em memória Stack versus Heap.**

Vamos a alguns exemplos para ilustrar:

**Valor e referência:** Precisamos entender que em Java tudo é objeto, logo objetos diferentes podem ter as mesmas características, mas lembrando, **são objetos diferentes.**

#### Exemplo em código

// ComparacaoAvancada.java
public static void main(String[] args) {

        String nome1 = "JAVA";
        String nome2 = "JAVA";
        
        System.out.println(nome1 == nome2); //true
    
        String nome3 = new String("JAVA");
        
        System.out.println(nome1 == nome3); //false
    
        String nome4 = nome3;
    
        System.out.println(nome3 == nome4); //true
        
        //equals na parada
        System.out.println(nome1.equals(nome2)); //??
        System.out.println(nome2.equals(nome3)); //??
        System.out.println(nome3.equals(nome4)); //??
    
    }

== versus equals: Existe uma relevância forte em realizar comparações com == e equals na qual precisamos ter uma compreensão de quais as regras seguidas pela linguagem **** , exemplo:

#### Exemplo em código

// ComparacaoAvancada.java
 public static void main(String[] args) {
        
        int numero1 = 130;
        int numero2 = 130;
        System.out.println(numero1 == numero2); //true
        
        Integer numero1 = 130;
        Integer numero2 = 130;
    
        System.out.println(numero1 == numero2); //false
        
        // A razão pela qual o resultado é false, é devido o Java tratar os valores
        // Como objetos a partir de agora.
        // Qual a solução ?
        // Quando queremos comparar objetos, usamos o método equals
        
         System.out.println(numero1.equals(numero2)); 
 }



# Lógicos

Os operadores lógicos representam o recurso que nos permite criar expressões lógicas maiores a partir da junção de duas ou mais expressões.

- && Operador Lógico "E"

- || Operador Lógico "OU"

#### Exemplo em Código

// Operadores.java
boolean condicao1=true;

boolean condicao2=false;

/* Aqui estamos utilizando o operador lógico E para fazer a união de duas 
expressões. 
É como se estivesse escrito:
 "Se Condicao1 e Condicao2 forem verdadeiras, executar código"
*/

if(condicao1 && condicao2)
	System.out.print("Os dois valores precisam ser verdadeiros");;

//Se condicao1 OU condicao2 for verdadeira, executar código.
if(condicao1 || condicao2)
	System.out.print("Um dos valores precisa ser verdadeiro");
Expressões lógicas avançadas
Nós acabamos de aprender que existem os operadores lógicos 
&
 (E) e || (OU), mas por quê no exemplo acima, foram ilustradas as condições:

if (condicao1 && condicao2) e if(condicao1 || condicao2) ?

**A duplicidade nos operadores lógicos é um recurso conhecido como Operador Abreviado, isso quer que se a condição1 atender aos critérios não será necessário validar a condição2.**

#### Exemplo em Código

// ComparacaoAvancada.java
int numero1 = 1;
int numero2 = 1;

if(numero1== 2 & numero2 ++ == 2 )
    System.out.println("As 2 condições são verdadeiras");

System.out.println("O numero 1 agora é " + numero1);
System.out.println("O numero 2 agora é " + numero2);

// Vamos mudar a linha 5 do código acima para: if(numero1== 2 && numero2 ++ == 2 )

**O mesmo acontece com o operador | e || considerando que operador agora representa que, se uma das alternativas for verdadeira, a outra nem precisa ser avaliada.**

