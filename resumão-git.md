## Revisão Aula Git
#### Prof. Reinaldo M Padua, Unoesc.

### Por que versionar código?
* Para evitar perdas acidentais de arquivos ou trechos de códigos.
* Para prover segurança e rastreabilidade.
* Para facilitar o trabalho em equipe.

### O que é o Git e qual sua funcionalidade? 
É um sistema de versionamento de código distribuído. Em outras palavras, é um banco de dados que armazena e organiza todas as alterações feitas no código, facilitando o controle e organização do projeto. 

## Comandos Básicos

### git init
É o comando que inicializa um repositório git, em outras palavras, adiciona versionamento de código à um projeto feito em qualquer linguagem.
Por exemplo, você está desenvolvendo um site em php em seu computador. Vocês cria uma pasta onde serão adicionados arquivos em php, html, js, css, etc.. e 
preferencialmente antes de começar a adicionar arquivos ou codar, você executa o comando "git init", ele vai criar uma pasta chamada ".git" dentro do seu projeto,
e a partir deste momento, este projeto tem suporte a versionamento de código.

### git clone
o git clone serve para copiar um projeto de um endereço remoto para seu computador, você pode usar ele para copiar de algum servidor de sua rede 
ou de plataformas de hospedagem de código como github ou outros. Você pode copiar utilizando o protocolo http ou ssh. 
Também pode especificar username e password quando necessário ou gerar uma chave .ssh em sua máquina e cadastrá-la no servidor git.
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
feito isso, o git passa a monitorar as alterações feitas nesse arquivo. Também é possível executar o comando "git add *"
que adiciona versionamento para todos os arquivos existentes na pasta (com exceção dos arquivos definidos no arquivo .gitignore) 

### git commit
Após adicionar os primeiros arquivos ou as primeiras linhas de código, você deve "gravar" ou "salvar" o que você fez até agora, isso é feito através do 
comando "git commit", deve ser passado como parâmetro entre aspas uma mensagem descrevendo o que você fez, por exemplo:
~~~
git commit -m "criando arquivo de estilo para página home.html" 
~~~

### git branch
Branches são ramificações ou cópias do código contido no projeto. Todo projeto git normalmente tem uma branch principal(master, main, etc) onde fica
o código estável do projeto. A partir dela são criadas novas branches onde é feito o desenvolvimento de novas funcionalidades ou correções de bugs.
o comando git branch sozinho, lista todas as branches disponíveis no projeto e sinaliza dentro de qual branch você está localizado, 
Já o comando git branch + nome  cria uma branch com o nome especificado (essa branch vai ser uma cópia da branch que você está posicionado). 
~~~
git branch desenvolvimento 
~~~
~~~
git branch 
~~~

### git checkout
Após listar as branches, voce deve entrar na branch desejada utilizando o comando git checkout + nome da branch. Você também tem a possibilidade de utilizar o
comando git checkout -b  + nome da branch, o -b vai criar uma branch nova a partir da branch que você está posicionado (igual o comando git branch + nomedaBranch) e o
checkout vai fazer você entrar diretamente na nova branch.
~~~
git checkout desenvolvimento
~~~
~~~
git checkout -b  nova_funcionalidade 
~~~

### git push 
O git push serve para mandar o código de sua branch atual para um repositório remoto (no github, bitbucket ou servidor local). É interessante executar esse comando de tempos em tempo, ou a cada número de commits, pois se ocorrer algum problema em máquina, vai ter uma cópia atualizada salva no servidor. No primeiro push de uma branch
é necessário executar alguns comandos a mais:
~~~
git push --set-upstream origin desenvolvimento
~~~
~~~
git push 
~~~

### git pull
Supondo que você e um colega estão trabalhando no
mesmo projeto e branch, após seu colega commitar e fazer push, você deve executar um git pull para baixar as atualizações para sua branch. 
~~~
git pull 
~~~

### git merge
Após concluir o desenvolvimento em sua branch, você possivelmente vai precisar mesclar o que foi desenvolvido com outra branch. Isso pode ser feito direto na plataforma de hospedagem de código (Github, Bitbucket, outro) ou pode você executar localmente git merge + sua branch + branch destino. Se você fez o merge localmente, posteriormentevai ter que fazer push da branch que recebeu o merge (branch de destino). 
~~~
git merge desenvolvimento master 
~~~
