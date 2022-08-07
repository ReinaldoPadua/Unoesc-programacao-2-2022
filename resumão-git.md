### Por que versionar código?
Para evitar perdas acidentais de arquivos ou trechos de códigos.
Para prover segurança e rastreabildiade.
Para facilitar o trabalho em equipe.

### O que é o Git e qual sua funcionalidade? 
É um sistema de versionamento de código distribuido. 

## Comandos Básicos

### git init
É o comando que inicializa um repositório git, ou em outras palavras, adiciona versionamento de código a um projeto feito em qualquer linguagem.
Por exemplo, você está desenvolvendo um site em php em seu computador. Vocês cria uma pasta onde serão adicionados os aquivos em php, html, js, css, etc.. e 
preferencialmente antes de começar a adicionar arquivos, ou codar, você executa o comando "git init", ele vai criar uma pasta chamada ".git/" dentro do seu projeto,
e apartir deste momento, você tem suporte a versionamento de código.

### git clone
o git clone serve para copiar um projeto de um endereço remoto para seu computador, você pode usar ele para copiar de algum servidor de sua rede 
ou plataformas de hospedagem de código como github ou outro. Você pode copiar utilizando o protocolo http ou ssh. 
Também pode especificar username e passowrd quando necessário ou gerar um chave .ssh em sua maquina e cadastrala no servidor git.
~~~
git clone https://github.com/ReinaldoPadua/Unoesc-programacao-2-2022.git
~~~
~~~
git clone git@github.com:ReinaldoPadua/Unoesc-programacao-2-2022.git (ssh)
~~~
~~~
git clone https://meuUsuariog:meuPassword@github.com/ReinaldoPadua/Unoesc-programacao-2-2022.git
~~~

### git add
Cada vez que você adicionar ou criar um arquivo dentro do seu projeto, você deve executar o comando "git add" + o nome do arquivo para colocar esse arquivo no "radar" do git, exemplo: 
~~~
git add controller.php
~~~
feito isso, o git passa a monitorar as alterações feitas nesse arquivo. Também é possivel executar o comando "git add *"
que adiciona versionamento para todos os arquivos existentes na pasta (com excessão dos arquivos definidos no arquivo .gitignore) 

### git commit
Após adicionar os primeiros arquivos ou as primeiras linhas de código, você deve "gravar" ou "salvar" o que você fez até agora, isso é feito através do 
comando "git commit", deve ser passado como parametro entre aspas uma mensagem descrevendo oque vocês, por exemplo:
~~~
git commit -m "criando arquivo de estilo da pagina home" 
~~~

### git branch
Branches são ramificações ou cópias do código contido no projeto. Todo projeto git normalmente tem uma branch principal(master, main, etc) onde fica
o código estavel do projeto. A partir dela são criadas novas branches onde é feito o desenvolvimento de novas funcionalidades ou correções de bugs.
o comando git branch sozinho, lista todas as branches disponveis no projeto e sinaliza dentro de qual branch você está localizado, 
já o comando git branch + nome  cria uma branch com o nome especificado (essa branch vai ser um copia da branch que você está posicionado). 
~~~
git branch desenvolvimento 
~~~
~~~
git branch 
~~~

### git checkout
Após listar as branches, voce deve entrar na branch desejada utilizando o comando git checkout + nome da branch. Você também tem a possibilidade de utilizar o
comando git checkout -b  + nome da branch, o -b vai criar uma branch nova a partir da branch que você está posiconado (igual o comando git branch nomedaBranch) e o
checkout vai fazer você entrar diretamente na nova branch.
~~~
git checkout desenvolvimento
~~~
~~~
git checkout -b  nova_funcionalidade 
~~~



### git push





### git pull

### git merge
