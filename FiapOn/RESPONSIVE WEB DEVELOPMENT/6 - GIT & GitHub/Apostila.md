# Apostila

## Git e GitHub
### Com o GIT instalado em sua máquina, chegou a hora de nos apresentarmos para ele, ou seja, configurar o sistema para ele identificar o desenvolvedor responsável pelas alterações. Para criarmos o nosso primeiro diretório, você deverá criar uma pasta (pode ser no desktop mesmo) e com o botão direito clicar na opção Git Bash Here.

### No exemplo “Criando uma pasta”, o nome da pasta criada é: Projeto Git. Após clicar em Git Bash Here o nosso terminal se abrirá, e você digitará o primeiro comando: 
```git
    git init
```

### Após o comando git init você notará uma pasta oculta chamada .git, isto quer dizer que iniciamos o nosso repositório, mas precisamos configurá-lo com o nome e o e-mail. Para isso, basta digitar no terminal os comandos:
```git
    git config --global user.name "Gustavo Torrente"
    git config --global user.email "email@fiap.com.br"
```

### Dica: realizamos esta configuração global para evitar que em todo projeto seja necessária uma nova configuração. Para verificar se o nome e e-mail foram setados corretamente, basta entrar com os comandos:
```git
    git config user.name
    git config user.email
```

### Dentro da sua pasta: Projeto Git, crie um arquivo **index.txt**. E agora em seu terminal, execute o comando: 
```git
    git status
```
### , este comando nos informa o estado de nosso arquivo.

### Neste caso, a mensagem retornada é: **untracked**, ou seja, um  arquivo desconhecido para o GIT. O GIT entende que existe um arquivo,mas não identifica nenhum estado. Precisamos informar para o GIT que este arquivo deve ser versionado e, para isso, vamos executar dois comandos. O primeiro comando é seguido do nome do arquivo:

```git
    git add index.txt
```
### E o segundo comando é responsável pela gravação no repositório.
```git
    git commit -m "Primeiro commit
```

### Pronto! Agora temos o primeiro versionamento do nosso arquivo. Agora que você já sabe como instalar, configurar e criar versionamentos do seu projeto, vamos aprender a navegar entre as versões. Para verificar todo histórico de mudanças em nosso repositório, utilizamos o seguinte comando:

```git
    git log
```
### O git log nos retorna um ID, o autor, data e a própria alteração realizada. Como não realizamos mudanças em nosso arquivo ainda não temos como navegar, então abra o seu arquivo em branco index.txt e salve uma alteração. Agora com nossa primeira alteração feita, vamos retornar ao terminal/prompt de comando para executar o comando 
```git
    git status
```

### Repare que ao executar este comando a mensagem em vermelho informa: **modified**. O GIT já sabe que aquele arquivo foi alterado e para visualizarmos esta mudança, um novo comando: 
```git
    git diff
```
### Repare que após executarmos este comando o GIT nos informa qual  foi a alteração (texto em verde) e quantas alterações foram realizadas (texto em azul). O próximo passo é versionar este arquivo e para isso utilize o comando que você já aprendeu: 
```git 
    git add index.html
```
### Durante o desenvolvimento de um projeto, erros podem acontecer e a necessidade de voltar para uma versão anterior do seu código se torna necessária.

### Para aumentarmos a produtividade em sistemas de controle de versão, temos a possibilidade de nomear as hashs, criando tags e versões paralelas do nosso código.

### Uma vez que trabalhamos com branches temos várias linhas de desenvolvimento. Quando trabalhamos em equipe cada um pode seguir a  sua branch, mas o que acontecena hora de integrar todas estas mudanças e alterações?

### Conflitos são inevitáveis, principalmente quando estamos trabalhando em equipe. Imagine a seguinte situação: Trabalho remoto com 2 programadores alterando partes diferentes do código. O GIT fica confuso e não sabe como proceder!

### E quando surgirem situações onde temos arquivos em nosso repositório, mas não queremos que eles sejam rastreados? Existem diversos motivos para isso acontecer e para que não atrapalhe a sua produtividade.

### O Github é a maior rede social de código aberto utilizando o sistema de controle de versão GIT. Em 2018 a Microsoft comprou o site Github por US$ 7,5 bilhões.

### Você já aprendeu a criar repositórios locais, mas através do Github você tem a possibilidade de criar repositórios remotos.

### Existem situações em que temos arquivos atualizados em nosso repositório remoto e arquivos que não estão atualizados no  repositório local. O **git pull** é responsável pela atualização de todas as versões, ideal para quando você está trabalhando off-line e seus arquivos locais ainda não estão sincronizados com o repositório remoto. Ficou curioso para conhecer este comando?

### O comando git push é o inverso do **git pull**, é através dele que você envia seus arquivos atualizados para o seu repositório remoto, no caso o Git hub.

### Já dizia um provérbio chinês: “Sábio é aquele que aprende com o erro dos outros”. Por isso, nada melhor que aprender com profissionais que já atuam na área e têm boas dicas para compartilhar.