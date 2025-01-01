# JAVA

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