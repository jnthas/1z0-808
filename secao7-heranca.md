# Trabalhando com herança

## 9.1 Implementando herança

- Para que a classe filha herde da classe mãe, é preciso que a classe mãe seja visível e também pelo menos um de seus construtores. Ocorre erro de compilação se por exemplo, a classe mãe possui somente o construtor Mae(int i) e a classe filha não implementar esse construtor
- A classe mãe não pode ser final, já a filha pode
- Dependendo da visibilidade, a classe filha não consegue enxergar o método ou atributo. Ex: this.x = 5, send que x é private da classe mãe
- Se houver um ciclo na herança **não compila**. Ex.: A extends B e B extends A

### Métodos estáticos 

- Não existe herança de membros estáticos, mas é possivel acessar um método ou atributo estático pelo nome da classe filha
- Não é possivel acessar um membro estático através da instrução super, pois ela referencia o objeto (erro de compilação)
- É possivel reescrever um método estático na classe filha, mas isso não é sobreescrita (overwrite)
- Não existe herança de construtores, a filha chama o construtor da mãe
- Não existe herança de atributos, se a filha tiver um atributo com mesmo nome da mãe, ele será acessivel com this.x e super.x, para filha e mãe respectivamente


### Object

- Quando usamos um objeto qualquer no contexto de string, na verdade é chamado o toString() do objeto. Ex. sout("Carro: " + carro)

1) Sim 2) Nao 3) a 4) a 5) c 6) c 7) a 8) b

## 9.2 Uso poliformismo

- Mesmo que a referência seja da classe pai, o método executado é do classe filha, o que importa é o objeto e nesse caso é da classe filha.
- O método que será executado (binding) será descoberto em **tempo de execução**
- A assinatura é decidida em **compile-time**
- Para reescrever um método é preciso que ele tenha o mesmo nome, tipo e ordem dos parametros iguais, retorno igual ou mais específico, visibilidade igual ou maior, exceptions iguais; mais específicas ou menos, não pode ser final na mãe. Pode haver um erro de compilação ou o método pode não ser considerado reescrita (overwrite)
    - Sobre a visibilidade de um método reescrito, uma classe mãe com método public não pode ter seu método reescrito com protected, dessa forma a visibilidade diminuiu
    - Numa interface o padrão é public, e não precisa colocar a instrução. Mas ao implementar, a classe **DEVE** colocar public ou ocorrerá erro de compilação
    - Uma classe abstrata que extende uma classe comum pode tornar abstrato um método que antes era comum, passando a implementação desse método para quem for extender a classe abstrata. É uma pegadinha tbm.
    - Sobre o retorno ser mais específico, na verdade ele deve ser **covariante**. O melhor exemplo é quando um método retorna um List<> mas seu overwrite retorna um ArrayList<>. Detalhe: **Não funciona com tipos primitivos, somente referência!!!**
    - Sobre as exceptions: um metodo da classe filha pode subir somente exceptions mais epecíficas que a superclasse, ou então subir menos exceptions da que foi definida na classe mãe. RuntimeException funciona mesmo que não declare com throws ou seja mais genérico na classe filha.

### super e this

- Se a classe mãe e filha possuem o mesmo método (overwrite) e a classe mãe chama esse método, ele é chamado na classe filha, dependendo da questão pode gerar um loop infinito

1) a 2) b 3) c 4) a 5) a 6) d 7) g 8) b 9) a





