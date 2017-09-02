# 8 - Trabalhando com métodos e encapsulamento

## 8.1 retorno

- O único modificador possível num parametro de método é o final, indicando que o parametro não pode ser modificado. Caso tente modificar, resulta em erro de compilação
- Para o caso de parametros de tipo primitivo, qualquer valor compatível mais restrito pode ser passado que a jvm converte no tipo esperado
- Early return é uma instrução de retorno num método void antes dele acabar
- Não se pode ter um código que jamais será executado, depois de uma instrução de return. Ocorre **erro de compilação**
- Em métodos que retornam algum valor, todo fluxo deve ter um return ou exception
- Em métodos void, não é permitido atribuir seu retorno a uma variável. **erro de compilação**

1) a 2) d xxx 3) b 4) a 


## 8.2 - static

- Um método ou atributo de instância dentro de um método estático: **erro de compilação**
- Como se fosse um script, se a variável estática não foi inicializada, ela retorna o valor padrão.
- Uma variável estática pode acessar outra estática
- Não é possível reescrever um método estático com um não estático, mesmo numa subclasse. Caso sobreescreva com outro método estático, a referencia do método é a mesma da classe, ou seja, se A extends B e sobreescreve um método estático, os retornos são diferentes se executar A.method() e B.method().

1) a 2) b 3) d 4) a 5) b


## 8.3 - métodos sobrecarregados

- Métodos sobrecarregados podem ter ou não tipo de retorno e visibilidade diferentes
- Compilador sempre invoca o método com o tipo menos genérico (mais específico). Entre Object e String, escolhe String. (A não ser que seja feito casting)
- É possivel inverter a ordem dos parametros e criar dois metodos totalmente distintos, mas em alguns casos pode ocorrer **compile error** ao passar dois ints para um método que recebe int e double

1) a 2) c 3) a 4) a 5) a xxx 6) b 7) b xxx 8) b


## 8.4 - construtor padrão

- se não for definido um construtor para a classe, o compilador adiciona um com a mesma visibilidade da classe e sem parâmetros, com um "super()" no corpo.
- Se for adicionado um construtor qualquer, o padrão deixa de existir se tentar criar a classe com new A(), resulta em **compile error**, "no default constructor"
- Cuidado ao tentar acessar variáveis sem estarem inicializadas, resultando em nullpointerexception
- Prestar atenção, se tiver tipo de retorno ou void, é um método e não o contrutor

1) d 


## 8.5 sobrecarga construtores

- Quando há mais de um construtor, qdo se está em um construtor é possível chamar outro com o "this(param, param2)"
- Se um contrutor chamar o outro e vice-versa, não compila
- Assim como nos métodos, havendo dois metodos um que recebe varargs e outro sem parametro, ao chamar o contrutor sem parametros, será executado o construtor sem parametros e não o varargs
- Se for usada, a instrução this() deve ser a primeira do construtor. Caso contrário, **compile error**
- Não é possível ter duas chamadas a this
- A instrução this() pode ter chamdas a metodos **estáticos** this(value())

1) a 2) f 3) f 4) f 5) e 

## 8.6 modificadores de acesso

- Quatro tipos: public, private, default e protected
- Classes e interfaces (cobrados na prova) só aceitam public ou default
- Membros (construtores, métodos e variáveis) aceitam os quatro modificadores
- variáveis locais (declaradas dentro do corpo de um método ou construtor) e parâmetros não podem receber nenhum modificador de acesso
- public: classes, interfaces e membros podem ser acessados por qualquer componente ou pacote
- protected: classes e interfaces podem ser acessadas de dentro do mesmo pacote; membros podem ser acessados no mesmo pacote ou se uma classe extender de outra, nesse caso a classe filha pode estar em outro pacote
- default: **não existe** em uma declaração de método ou classe! Com esse modificador a classe ou membro só é visível dentro do pacote. Mesmo se uma classe extender outra, ela só enxerga o atributo default se estiver no mesmo pacote. Se a classe for default, não importa o modificador dos membros da classe. 
- private: é o mais restritivo, ninguém consegue acessar o membro da classe, somente a própria classe
- Méotodos private e defalut não podem ser sobrescritos
- Uma classe é top-level se ela não foi definida dentro de outra classe
- Se o modificador do construtor for default, ele não é visivel por classes de outros pacotes
- Se um método sobrescrito não está visivel numa classe filha, a chamada passa para a classe pai
- final pode ser inicializado com variável static

1) d xxx 2) a xxx 3) b 4) a 5) a xxx 6) a 7) a xxx



