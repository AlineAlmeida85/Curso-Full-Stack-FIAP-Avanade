# Sistema de Controle de Versão

#### Ele vai permitir controlar alterações que ocorreram no decorrer de um tempo em um arquivo ou no projeto inteiro e isso vai facilitar quando precisarmos voltar trechos, ou saber quem fez aquela alteração, quando, porque e como fez, vai nos permitir também trabalhar em um grupo de desenvolvedores. Muitas vezes podemos ter na equipe até umas 10 pessoas trabalhando no mesmo projeto e, consequentemente no mesmo arquivo. E o sistema de controle de versão vai ter a inteligencia de saber juntar as alterações de cada desenvolvedor daquele arquivo. E quando todo mundo está colocando a mão no mesmo arquivo a chance de acontecer uma bobagem é gigantesca.

#### Agora que ja sabemos o que é o controlador de versões e pra que serve, vamos então utilizá-lo.

#### Iniciando pela configuração do GIT:
```git
    git config --global user.name "seu nome"
    git config --global user.email "seu email"
```
#### Este comando acima configura o usuario que vai utilizar o Git, e no caso utilizamos o comando global para que seja configurado apenas uma vez, sem ter a necessidade de configurar a cada novo projeto.
#### Para verificar a configuração feita acima use o comando:
```git
    git config user.name
```
#### E aparecerá o nome que está configurado, assim:

<p align="center">
  <img alt="foto" title="foto" src="./img/foto01.png"/>
</p>

#### Para ver o email é:
```git
    git config user.email
```
#### E...
<p align="center">
  <img alt="foto" title="foto" src="./img/foto02.png"/>
</p>

## ESTADOS DOS ARQUIVOS E COMMITS

#### Para iniciar um projeto usamos o comando:
```git
    git init
```

#### Voce pode criar um arquivo manualmente ou usando o comando:
```git
    touch nome do arquivo.formato
```
#### E se for uma pasta, podemos criar usando o comando:
```git
    mkdir nome da pasta
```
#### Assim:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto03.png"/>
</p>

#### Usei om comando:
```git
    ls 
```
#### Para listar os itens da pasta em que estou e la está, a pasta **Curso** que criei.

#### Agora vamos começar a versionar os arquivos. Vamos criar um arquivo txt dentro do nosso repositório.
```git
    touch index.txt
```
#### E:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto04.png"/>
</p>

#### O arquivo foi criado porém ainda não foi versionado. Vamos usar o comando:
```git
    git status
```

#### Para ver como está o arquivo criado:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto05.png"/>
</p>

#### Esta dizendo que temos um arquivo do tipo **untracked** na master. O que significa que esse arquivo ainda não é conhecido no nosso repositório, é um arquivo novo e ainda não foi versionado. \ou seja, o comando **git status** sempre vai retornar o status em que se encontra o arquivo ou o projeto.
#### Para apontar para o git o aquivo ou o projeto a ser versionado, usamos o comando:
```git
    git add nome do arquivo.extensão
```
#### Para versionar o arquivo, Ou
```git
    git add .
```
#### Para versionar todo o conteúdo ou projeto, vamos ver:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto06.png"/>
</p>

#### **DICA: Para versionar vários arquivos ao mesmo tempo, basta adicionar um a um com a estensão seguido de espaço.**

#### Após ter adicionado, perceba que o git não nos retornou nada, ou seja, ele ja adicionou. Se usarmos o comando:
```git
    git status
```

#### Vamos notar:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto08.png"/>
</p>

#### Então agora o Git está reconhecendo o novo arquivo e poderá versioná-lo. Quando usamos o comando **git add** estamos informando ao Git que existe um arquivo que deve ser monitorado pois está aguardando numa área temporária para ser versionado. Agora vamos usar o comando:
```git
    git commit -m "mensagem"
```
#### Na mensagem procure ser o mais simples e direto possível especificando sempre o que foi feito naquele versionamento para que fique documentado de uma forma correta e clara.
#### E
<p align="center">
  <img alt="foto" title="foto" src="./img/foto09.png"/>
</p>

#### Assim, então, nosso arquivo foi versionado.

## NAVEGAÇÃO ENTRE AS VERSÕES

#### Agora que ja sabemos criar as versões através dos comandos: 
```git
    git add
    git status
    git commit
```
#### Vamos fazer uma simulação da evolução do código fonte e como podemos voltar e avançar entre as versões. Vamos então criar mais umas duas versões e navegar entre elas. No nosso projeto criamos um arquivo chamado **index.txt** que está vazio, ou seja, a versão 1 é a versão em branco do arquivo criado. Pra ver o histórico que ja possuimos, quais foram as alterações que ja aconteceram, ou o que ja foi criado, usamos o comando:
```git
    git log
```
#### Podemos navegar por esse histórico, mesmo se for grande:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto11.png"/>
</p>

#### Mas, no nosso exemplo tem somente uma. Analisando a foto acima, notamos que:
- existe o ID do commit e onde foi feito
- o autor do commit (nome e email)
- a data do commit
- e a mensagem que foi passada no commit

#### Vamos fazer algumas alterações nesse arquivo. Abra ele e digite algo e salve depois:

<p align="center">
  <img alt="foto" title="foto" src="./img/foto12.png"/>
</p>

#### Agora no terminal digirte o comando:
```git
    git status
```
#### Perceba que o status do arquivo foi alterado:

<p align="center">
  <img alt="foto" title="foto" src="./img/foto13.png"/>
</p>

#### E para ver a alteração que foi feita usamos o comando:
```git
    git diff
```
#### E
<p align="center">
  <img alt="foto" title="foto" src="./img/foto14.png"/>
</p>

#### Analisando a foto acima, o comando usado retorna:
- o nome do arquivo que foi alterado
- o ID da alteração
- que foi adicionada +1 linha no arquivo
- no caso, a mensagem que foi adicionada ao arquivo
#### Então, concluimos até aqui que, realmente foi feita essa alteração incluindo a mensagem no arquivo, e tendo a ceteza então que está tudo correto, vamos adicionar esse arquivo para ser versionado usando o comando:
```git
    git add .
```
#### E vamos usar agora o:
```git
    git status
```
#### Para verificar o status da alteração:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto15.png"/>
</p>

#### Ele retorna com o status modified, ou seja, o arquivo ja está separado para ser versionado através do commit:
```git
    git commit -m "Criamos uma linha de modificação para exemplo"
```
#### Assim ele mostra:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto16.png"/>
</p>

#### Que foi feita uma alteração no arquivo com apenas uma inserção. Então se digitarmos o comando:
```git
    git log
```
#### Vamos notar que:
<p align="center">
  <img alt="foto" title="foto" src="./img/foto17.png"/>
</p>

**Ctrl L**: limpa a tela

#### Agora temos dois commits mostrados em ordem decrescente, pode ocorrer de aparecem os dois pontos na tela do git **":"**, o que significa que o git está em modo de navegação para que possa navegar entre os logs usando as teclas seta para cima ou para baixo, para sair do modo de navegação use a tecla Q.
#### E vamos usar agora o:
```git
    git status
```
#### Veremos que não te mais nada para commitar. Agora vamos criar mais uma versão.