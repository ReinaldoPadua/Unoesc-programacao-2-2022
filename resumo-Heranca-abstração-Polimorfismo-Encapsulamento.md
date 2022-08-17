# Resumo Herança, abstração, Polimorfismo e Encapsulamento


### Abstração

“Abstração é o ato de abstrair, ou seja, isolar mentalmente para considerar à parte um elemento de representação que não é dado separadamente na realidade.”

Em programação orientada a objetos, é quando olhamos para um cenário ou contexto do mundo real e identificamos quais elementos são importante para representar
esse contexto em um software, por exemplo, em uma operação de comercialização de produtos, identificamos que vai existir um cliente, este vai ter nome, cpf, data de nascimento
entre outras informações, vai ter um produto com suas caracteristicas, vai existir a loja, vai exitir o pedido( que vai ter o produto, a quantidade, valores), vai ter o metodo de pagamento e o pagamento em si, etc. 


### Herança

É o mecanismo da orientação a objetos onde uma class filho herda atributos e métodos de uma classe pai.  Exemplo, imagine uma classe Funcionário, que tem nome, matrícula, cpf e outros dados. Também imagine outras duas classes:  Vendedor, e estoquista, essas classes também tem os mesmos dados (nome, matrícula, cpf) e alguns métodos em comum, porém cada um também possui características específicas. Para não ter que implementar dados de forma repetida em todas as classes, faz mais sentido as classes Vendedor e Estoquista herdarem essas informações da classe Funcionário.

No Java isto acontece através do uso do "extends", exemplo:

* public class Vendedor extends Funcionario {.....





### Polimorfismo

### Encapsulamento
