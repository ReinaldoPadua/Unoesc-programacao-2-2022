# Resumo Abstração, Herança, Polimorfismo e Encapsulamento


### Abstração

“Abstração é o ato de abstrair, ou seja, isolar mentalmente para considerar à parte um elemento de representação que não é dado separadamente na realidade.”

Em programação orientada a objetos, é quando olhamos para um cenário ou contexto do mundo real e identificamos quais elementos são importante para representar
esse contexto em um software, por exemplo, em uma operação de comercialização de produtos, identificamos que vai existir um cliente, este vai ter nome, cpf, data de nascimento
entre outras informações, vai ter um produto com suas características, vai existir a loja, vai existir o pedido( que vai ter o produto, a quantidade, valores), vai ter o método de pagamento e o pagamento em si, etc. 


### Herança

É o mecanismo da orientação a objetos onde uma classe filho herda atributos e métodos de uma classe pai.  Exemplo, imagine uma classe Funcionário, que tem nome, matrícula, cpf e outros dados. Também imagine outras duas classes:  Vendedor, e estoquista, essas classes também têm os mesmos dados (nome, matrícula, cpf) e alguns métodos em comum, porém cada um também possui características específicas. Para não ter que implementar dados de forma repetida em todas as classes, faz mais sentido as classes Vendedor e Estoquista herdarem essas informações da classe Funcionário.

No Java isto acontece através do uso do "extends", exemplo:

    public class Vendedor extends Funcionario {.....

### Polimorfismo

É a característica da orientação a objetos, que permite o desenvolvedor usar o mesmo elemento de formas diferentes. Olhando para o mundo real, podemos afirmar que todo animal executa a ação de comer, mas olhando para os animais de forma distinta, enquanto um leão come carne, um boi se alimenta apenas de pasto... a mesma ação de comer, 
mas com comportamentos diferentes.

Para implementar o polimorfismo no Java, podemos utilizar classes abstratas e interfaces.

#### Classes Abstratas

Classes abstratas permitem definir uma classe genérica que fornecerá propriedades e métodos abstratos para as classes que herdam a classe abstrata. Nas classes que herdam, os métodos abstratos herdados devem ser sobrescritos para a implementação do comportamento específico. Obs: A classe abstrata não pode ser instanciada, ou seja,
não é possível gerar um objeto a partir dela, apenas a partir das classes que herdam. Exemplo, tenho uma classe abstrata "conta" e classes contaCorrente e contaInvestimento
que herda da classe abstrata e genérica "conta", neste contexto não faz sentido ter objetos gerados da conta abstrata, apenas das contas que herdaram.

    public abstract class Conta {
   
    public class ContaInvestimento extends Conta {

#### Interfaces

Interfaces são contratos que obrigam a classes que às implementam a ter determinados métodos,  por exemplo, pensando em uma Violao, ele pode ter uma interface "eletroacústico", na interface está descritos os métodos "aumentarVolume", "diminuirvolume", "regularGrave" entre outros. Logo se a classe Violao implementar esta interface, ela obrigatoriamente terá que implementar os métodos da interface.

      public interface eletroAcustico { 
  
      public class Violao implements eletroAcustico { 


### Encapsulamento

É a característica das linguagens orientadas a objeto que permitem proteger os atributos ou metodos de determinados objetos, permitindo seu acesso de forma indireta.
Por exemplo, pense em uma classe funcionária, ela tem um atributo salário, não é interessante que essa propriedade seja aumentada aleatoriamente, nem para mais, nem para menos. Exemplo:

        Funcionario joao = new Funcionario();
      
        joao.salario = 50.000;

Para evitar comportamentos inesperados, é recomendado deixar a propriedade salário com a visibilidade privada ( ela só pode ser vista e manipulada dentro da própria classe), e criar um método público chamado setSalario(), dentro desse método colocamos validações para por exemplo, não deixar diminuir o salário, ou não aumentar caso ele
tenha tido um aumento a menos de 6 meses, etc. Exemplo: 

     public void setSalario(Double novoSalario)  {
       if(novoSalario>this.salario)
           this.salario = novoSalario;
     }
       
     joao.setSalario(10.000)

#### Modificadores de acesso

Para prover encapsulamento, Java possui modificadores de acesso (private, public, protected), estes moficadores devem ser adicionados na frente de classes, metodos ou atributos.

  * public : Uma declaração com o modificador public pode ser acessada de qualquer lugar e por qualquer entidade que possa visualizar a classe a que ela pertence.
  
  * private : Os membros da classe definidos como não podem ser acessados ou usados por nenhuma outra classe. Esse modificador não se aplica às classes, somente para seus métodos e atributos. Esses atributos e métodos também não podem ser visualizados pelas classes herdadas.

  * protected : O modificador protected torna o membro acessível às classes do mesmo pacote ou através de herança, seus membros herdados não são acessíveis a outras classes fora do pacote em que foram declarados.  
  


