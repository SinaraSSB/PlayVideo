<h1> --- Iniciando o Repositório Local ---- </h1>
<h3>Curso de Git e GitHub: compartilhando e colaborando em projetos </h3>


---

> `git init `

> `git add . `

> `git commit -m "First commit play video"`

> `git branch -M main `

> `git remote add origin git@github.com:SinaraSSB/PlayVideo.git   <i>ou</i>`

> `git remote add origin https://github.com/SinaraSSB/playvideo.git  `

> `git push -u origin main `

<hr>

https://www.devmedia.com.br/comandos-e-tags-html5/23618

https://cursos.alura.com.br/course/git-github-compartilhando-colaborando-projetos/task/139310

https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


---- 
O Git é uma ferramenta excelente para acompanhar a mudança entre versões de um mesmo projeto e, 
 dentre vários benefícios, nos ajuda a observar de perto o desenvolvimento do seu aprendizado.
  Tudo isso de uma forma organizada através dos commits.

Além disso, algo que é essencial no universo da tecnologia é apresentar o seu progresso 
para a comunidade e montar um portfólio dos seus projetos para demonstrar suas habilidades. 
Dessa forma, o GitHub é essencial para compartilhar e colaborar em projetos de programação de todo o mundo.

---------------------------------------------------------------------------

<h3> 1 - Adicionar um repositório remoto: </h3>

Quando você deseja estabelecer uma conexão entre seu repositório local e um repositório remoto, 
como aquele hospedado no GitHub, o comando git remote add é a ferramenta essencial. 
Essa etapa é crucial para possibilitar a colaboração e o compartilhamento de código com outras pessoas,
 bem como para fazer backup de seu trabalho em um servidor remoto.

A sintaxe básica do comando é a seguinte:

> git remote add apelido url
 
'apelido': Este é um nome que você atribui ao repositório remoto. Geralmente, se utiliza nomes descritivos,
 como "origin" para o repositório principal no GitHub, 
 mas você pode escolher nomes que façam sentido para o seu projeto.

'url': Aqui, você insere a URL do repositório remoto. Esta URL é única para cada repositório remoto e 
serve como o endereço para acessar e interagir com ele pela internet. Certifique-se de copiar a URL 
correta do repositório que deseja adicionar.

<h3> 2 - Listar os repositórios remotos:  </h3>

Para listar os repositórios remotos associados ao seu projeto local, você pode utilizar o 
comando git remote -v. Isso exibirá uma lista de todos os repositórios remotos vinculados ao seu projeto, 
juntamente com suas URLs. Veja um exemplo:

> git remote -v


<h3> 3 - Remover um repositório remoto: </h3>

Caso você não precise mais de um repositório remoto específico, 
pode removê-lo com o comando git remote remove apelido. Substitua 'apelido' 
pelo nome do repositório remoto que deseja remover. Aqui está um exemplo:

> git remote remove origin

Após a execução deste comando, o repositório remoto chamado "origin" 
será desvinculado do seu projeto local.


<h3> 4 - Alterar a URL de um repositório remoto: </h3>

Às vezes, é necessário atualizar a URL de um repositório remoto, 
como quando a URL do servidor do GitHub é modificada ou quando você copiou a URL incorreta ao adicionar
 o repositório remoto. Use o comando git remote set-url apelido nova_url para realizar essa atualização. 
 Substitua 'apelido' pelo nome do repositório remoto e 'nova_url' pela nova URL que você deseja associar a ele.
  Aqui está um exemplo:

> git remote set-url origin https://github.com/seu-usuario/seu-repositorio.git

Isso atualizará a URL do repositório remoto "origin" para a nova URL especificada.


<h3> 5 - Alterar o apelido de um repositório remoto: </h3>

Se você deseja renomear um repositório remoto, use o comando 
git remote rename apelido novo_apelido. Substitua 'apelido' pelo nome atual do repositório remoto e
 'novo_apelido' pelo novo nome que você deseja atribuir a ele. Aqui está um exemplo:

git remote rename origin novo-origin

Isso renomeará o repositório remoto de "origin" para "novo-origin".

----

O comando git push deve ser executado para sincronizar as mudanças do repositório local com o repositório remoto, 
ou seja, quando desejamos enviar os novos commits que realizamos em nosso repositório local para o repositório remoto. 
No entanto, para garantir uma conexão segura, é essencial configurar uma chave SSH no computador antes de
 executar esse comando.

---

<h2> Chave SSH </h2>

Ao vincular um repositório remoto ao nosso repositório local, via comando git remote add,
 precisamos utilizar algum protocolo seguro, como HTTPS ou SSH. No caso de se utilizar o protocolo SSH,
  escolha realizada neste curso, devemos gerar uma chave SSH em nosso computador, além de cadastrá-la em 
  nossa conta do GitHub. Isso é necessário para garantir a autenticação, pois o GitHub checa se quem está realizando 
  o push dos commits tem permissão para realizar tal ação.

Geração de uma chave SSH
Antes de executar o comando git push, precisamos gerar uma chave SSH. 
A geração da chave é feita via terminal, 
com o comando ssh-keygen -t ed25519 -C "SEU EMAIL AQUI":

Na primeira linha da mensagem você consegue identificar o diretório no seu computador no qual a chave foi salva. 
Agora, basta acessar tal diretório para ter acesso à chave SSH.

Observação: Nesse diretório serão gerados dois arquivos que representam a chave SSH,
 sendo um para a chave privada (arquivo id_ed25519) e o outro para a chave pública (id_ed25519.pub).

---

---

<h2>Clonando um repositório </h2>

Na opção de clonar, o GitHub fornece a URL do repositório. Sendo assim,
 a copiamos e abrimos o explorador de arquivos do computador e acessamos a área de trabalho.

Em seguida, clicamos com o botão direito do mouse e selecionamos "Abrir no terminal".
 Em seguida, para clonar o repositório, vamos passar o comando git clone seguido da URL 
 que copiamos e apertamos "Enter".

 > git clone https://github.com/SinaraSSB/alurabook.git

 <hr>

 <h4> O comando clone já realiza automaticamente a conexão entre o repositório remoto e o repositório local. </h4>
 <p>   não precisa git remote add origin git@github.com:SinaraSSB/PlayVideo.git 
 
 > git remote

 Feito isso é exibido o origin.
 O origin é o nome que o GitHub atribui quando fazemos o clone, é como se referisse a origem do repositório.

 Passamos git push e em sequência precisamos informar para onde enviaremos o commit. 
 Escrevemos origin que é o apelido do repositório remoto, seguido de main que é a branch e apertamos "Enter".

 > git push origin main

</p>

---

## Explorando outros comandos / git Status / git diff

`git status`

> Este comando nos indica em qual ramificação (branch) estamos e se há algo para adicionar e realizar um commit. 


`git diff`

`git diff > difs.txt`

> o objetivo é visualizar todas as alterações antes de prosseguir com o commit. Ao executar git diff, são exibidas as diferenças entre dois estados. 
**Por padrão, os estados comparados são as modificações que foram realizadas e ainda não foram adicionadas ao commit, e o último commit realizado, também conhecido como head. Esse comando exibe a diferença entre o último commit e o que temos modificado no arquivo.**

Para analisar a diferença entre esses dois commits específicos, precisamos incluir os três commits em nossa análise. Podemos fazer isso utilizando o comando git diff.

Primeiro, copiamos o hash do commit mais antigo que desejamos comparar, e colamos esse hash seguido de "..": git diff 5880fc1... Em seguida, copiamos o hash do commit mais recente que queremos comparar, e o colamos após "..".

`git diff 5880fc1..5bc160e`

O comando completo fica git diff, o commit mais antigo, "..", o commit mais novo. Ao teclarmos "Enter", ele mostra todas as alterações.

>O comando git diff, por padrão, compara as modificações que foram feitas mas ainda não foram adicionadas para serem commitadas, mostrando a diferença entre o estado atual do projeto e o último commit. Quando utilizamos git add em um arquivo, e em seguida executamos git diff, percebemos que não é mais exibido nenhum resultado. Por quê? 
>ele está em um estado que chamamos de stage (palco), ou seja, ele foi colocado em um local onde os commits são realizados. Portanto, o arquivo não está mais no estado anterior, fora do stage, onde o diff normalmente aponta. Assim, o comando git diff não mostrará mais diferenças para esse arquivo. Se rodarmos o git diff, não obtivemos nenhum retorno.

o comando git diff revela a diferença entre dois estados. Por padrão, ele compara o último commit com as alterações presentes no momento atual, mas também podemos especificar a diferença entre dois commits, ou entre um commit e o estado atual do projeto, ou seja, nosso head.


---
---

<h2> git log </h2>

`git log ` 

comando em que conseguimos identificar quais commits foram realizados no projeto e quem fez.

Ao executá-lo é exibido o histórico dos commits que foram feitos ao longo do projeto.
Se analisarmos o retorno,  Identificamos o nome do autor, data seguido da mensagem. 
Logo acima temos o commit mais atual,  que é o que acabamos de fazer. 

Com esse comando, visualizamos nossa lista de commits, o registro de versionamento. 
Para sair dessa visualização do git log, simplesmente pressionamos a tecla "Q". 


--- 

### Criar um Arquivo .txt com os Logs de Commits 

Execute o Comando git log para ver os registros de commits
No terminal, execute: 

`git log > logs.txt `

para criar um arquivo chamado logs.txt contendo os logs de commits

---
<h3>Alterando a visualização do log</h3>

para visualizar apenas as mensagens dos commits, de forma simplificada. Não estamos interessados em quem foi o autor do commit, em qual branch ele está, ou outros detalhes. Não desejamos verificar o hash completo do commit, apenas uma lista das mensagens, de forma mais compacta, linha por linha.
digitaremos git log, mas com a flag --oneline.

  `git log --oneline`

Isso nos permitirá visualizar o log de commits de forma muito mais resumida.

Com git log --oneline, teremos nosso histórico de commits exibido com os hashes reduzidos, mostrando apenas os primeiros caracteres do hash. Isso já é suficiente para identificarmos algum commit.

Isso é bastante semelhante ao que vemos no GitHub

</p>
--- 

<h3>Visualizando a alteração do commit</h3>
se for preciso examinar o commit e suas alterações, não apenas sua mensagem, 
mas também seu conteúdo. digitamos o comando: 

`git log -p`

Essa opção -p vai nos fornecer, além das informações padrão, o hash completo, o autor ou autora, a data e a mensagem do commit. Além disso, ele mostrará um diff, que é essencialmente um formato que o git utiliza para exibir as alterações de um commit específico.
Ele diz que as linhas que começam com "-" (---- a/index.html), significa que foram linhas que foram removidas. E as linhas que começam com "+" (+++ b/index.html), são as linhas adicionadas.

---

>Em suma, temos o git log --online para visualizar o log de forma compacta. Temos também o git log -p para ver  isso de forma expandida, com as alterações.

---

### Outras formas de exibição do log

E várias outras opções também, como o git log --graph, que exibirá uma linha do nosso log, e isso será ainda mais útil quando falarmos um pouco sobre branches.

Mas, essencialmente, se percorro isso até a parte em que temos um merge, que foi feito no curso anterior, percebemos que ele representa graficamente uma linha do tempo se desviando para outro ponto e depois retornando à nossa linha principal.

Note que à esquerda há uma linha vertical, e a partir do ponto de merge, outra linha se ramifica dessa vertical, estendendo-se até o commit do Rodrigo. Isso ficará um pouco mais claro, mas com o uso de --graph, conseguimos visualizar o log de uma forma mais visual.

Há ainda uma opção interessante, que é o --pretty ou --format. Ambos são sinônimos.
`git log --pretty 
git log --format`
Com --format ou --pretty, podemos exibir o commit da maneira que desejar. 
Por exemplo, utilizarmos --format="" e dentro das aspas digitar %H %an.

`git log --format="%H %an"`

### Vendo as alterações - 

git log --oneline

#### Analisando um commit especifico

para ver as alterações realizadas em um commit específico, independentemente de quem o tenha feito. 

Para isso, copiaremos o hash correspondente e digitaremos git show, seguido do respectivo hash.
para que nos apresente o conteúdo e os detalhes desse commit.

`git show 2ad48c0`

O comando git show nos proporcionará uma exibição semelhante ao git log -p, 
porém focado apenas no commit em questão, não em todo o registro.

são apresentados o hash do commit, o nome do autor, a data, a mensagem de commit e o diff correspondente, que detalha as alterações realizadas. Dessa forma, podemos navegar pelo conteúdo, descendo para visualizar as mudanças específicas. 

Observe como o comando git show é bastante simples, ele exibe o diff para nós. Novamente, basta pressionar "Q" para sair. Um detalhe interessante é que, ao digitarmos git show --help, podemos entender melhor como o comando funciona.

`git show --help`

O Git segue o padrão de nome do comando seguido de --help, com isso,
 podemos solicitar ajuda em caso de dúvidas em um determinado comando.

`NAME
    git-show - Show various types of objects
    
SYNOPSIS
    git show [<options>] [<object>…]`
    
Isso nos mostra que o git show espera algumas opções e objetos, como um commit, por exemplo.

Outra possibilidade é que o objeto seja algo diferente, mas para nossos propósitos, vamos focar no commit. 
Porém, antes de prosseguir, deixe-me explicar brevemente o formato de sinopse apresentado pelo help.

`git show [<options>] [<object>…]`

Sempre que algo está entre colchetes, isso indica que é opcional.

Você percebeu que apenas digitamos git show seguido pelo nome do nosso hash do commit, certo? Não especificamos nenhum opcional. Isso significa que, além das opções que já discutimos, esse objeto, o commit, também é opcional.
Se esse objeto não for informado, o help indica que ele "defaults to head" (assume o padrão como sendo o "head"). Portanto, ao pressionar "Q" para sair e digitar git log novamente, podemos destacar um detalhe interessante, 
O nosso último commit, do lado do hash do commit, temos (HEAD -> main, origin/main, origin/HEAD)

Primeiro, main é o nome de um branch e vamos falar sobre branch mais adiante. E esse origin, já sabemos que é o nosso repositório remoto, é lá no GitHub. Portanto, esse origin/main significa que esse commit também é onde está o nosso branch main no repositório remoto.

Basicamente, o que isso significa é que este commit representa o estado atual da nossa branch main, ou seja, é o estado atual da "main" no nosso repositório remoto.

Agora, o "HEAD" e o "origin/HEAD", que significam a mesma coisa que "HEAD" no repositório remoto, referem-se ao estado atual no repositório remoto. O que isso implica? "HEAD" representa simplesmente o último commit, ou seja, o commit atual do qual estamos trabalhando.

**HEAD: commit mais recente da branch atual**

Assim, como "mudanças no título e gitignore" é o último commit, ou seja, o mais recente, ele é o nosso HEAD. **Portanto, HEAD é essencialmente um sinônimo, um ponteiro, um apelido para o nosso último commit, o mais recente estado do nosso projeto no momento.**

Então, por que toda essa explicação sobre "HEAD"? 
Porque ao digitar apenas git show, sem mais nada, o Git mostrará os detalhes do último "commit".

`git show`


Assim, mais uma vez, o comando git show exibe os detalhes de um ou mais registros de alterações (commits),
 e se nenhum registro for especificado, ele por padrão seleciona o cabeçalho (HEAD), que é o último registro
 de alterações.

Portanto, sempre que encontrarem referências ao HEAD em documentação, artigos, textos ou similares, é bastante simples. Ele é apenas um alias para o registro de alterações mais recente da sua posição atual. Então, entendemos o funcionamento do git show. Ele exibe os detalhes do último registro de alterações ou de um registro específico.

---

<h3> Mensagens dos Commits </h3>

<p> Apesar de não existir uma regra universal para a escrita das mensagens de commit, algumas boas práticas podem ser seguidas para garantir que outras pessoas, e até mesmo você no futuro, entendam que alterações foram feitas e por quê.

As mensagens dos commits devem ser simples e objetivas. A seguir, listamos algumas orientações para isso:

Mantenha a mensagem curta e concisa: A primeira linha da mensagem deve conter, no máximo, 72 caracteres. Caso seja necessário uma descrição adicional, você deve pular uma linha e adicionar os detalhes, como o contexto, da mudança realizada.
<ul>
<li>Uso de verbo no infinitivo: É comum que a mensagem do commit inicie com um verbo no infinitivo que descreva a alteração feita, como “adicionar”, “corrigir” ou “atualizar”. Em sequência, são adicionados detalhes concisos da mudança. Por exemplo: “Atualizar texto do título da página”. </li>

<li>Evite detalhes técnicos: Não inclua detalhes técnicos complexos na mensagem de commit. Esses detalhes podem ser adicionados nos comentários de código ou na documentação. </li>

<li>É importante ter em mente que a mensagem do commit é uma forma de documentação do histórico das mudanças que ocorreram ao longo do código. A pessoa que ler essa mensagem pode não ter conhecimento do contexto original. Assim, garanta que suas mensagens de commit tenham clareza e sejam suficientemente descritivas. </li>
<ul>

Um commit deve ser realizado sempre que você finalizar uma tarefa específica ou resolver algum bug. Isso mantém o histórico de commits claro e rastreável, de modo que seja possível entender o que foi feito em cada commit.

Assim, é importante realizar commits frequentemente. Porém, evite realizar commits muito pequenos ou muito grandes, 
pois isso pode tornar difícil o seu entendimento.

Lembre-se de nunca realizar um commit de um código que você sabe que contém bugs. O ideal é que o commit 
contenha somente código funcional.

O controle de mudanças do Git é feito através dos commits. Cada commit armazena o estado completo do projeto em um determinado momento por meio de um snapshot. Ou seja, cada commit é um registro completo do repositório no momento 
em que esse commit foi criado.

Como cada commit é uma representação completa e consistente do estado do projeto em um determinado ponto no tempo,
 isso facilita a rastreabilidade e o entendimento de como se deu a evolução do código ao longo do tempo.

Todo commit conta com um id único e traz uma referência aos commits anteriores. Assim, 
através dessa cadeia de commits, o Git registra um histórico completo de todos os commits realizados no repositório.

Caso queira conhecer melhor sobre esse processo, acesse a documentação oficial do Git.
 https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-O-B%C3%A1sico-do-Git 
</p>
---

<h3> Adicionando colaboradores ao projeto</h3>
Se quisermos que outras pessoas colaborem nesse projeto, 
é preciso adicioná-las manualmente no projeto. 
Logamos no GitHub e acessamos o repositório.
Na barra de menu superior, clicamos no botão "Settings", que se refere a configuração
No menu lateral esquerdo, clicamos em "Collaborators". Feito isso, notamos que não há nenhum colaborador.
Para adicionarmos, no fim da tela, clicamos no botão verde chamado "Add people".
Na nova janela, há um campo referente ao username da pessoa que adicionaremos como colaboradora.
Ao fazer isso, a ferramenta indica que o pedido de acesso está pendente, 
pois o novo Colaborador precisa aceitá-lo. Sendo assim, esse processo não é automático.
Cada commit possui por padrão um autor, que é a pessoa que realizou aquelas alterações no código.

Entretanto, quando trabalhamos em equipe pode ser que algum trecho de código seja escrito em dupla ou trio. 
Assim, como definir a autoria dessas outras pessoas no commit?

O Git oferece a possibilidade de adicionar mais de um autor a um commit.
 Para isso, após escrever a mensagem do commit, pulamos duas linhas e usamos 
 a palavra-chave Co-authored-by:, seguido do nome e e-mail associado ao GitHub (entre < >)
  de cada pessoa colaboradora.

Cada coautor deve estar em uma linha diferente, como é mostrado no exemplo a seguir:

git commit -m "Adicionar nova funcionalidade.
>
>
Co-authored-by: NOME <nome@email.com>
Co-authored-by: OUTRO-NOME <outro@email.com>"

https://docs.github.com/pt/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors

---
---
<h2> VSCode -  Alertas ao lado do Nome do arquivo </h2>

 <p>  Quando estamos trabalhando em um projeto utilizando o versionamento Git e a IDE VSCode, 
 ao adicionar ou alterar algum arquivo aparece uma sinalização ao lado do nome desses arquivos. 

<strong> M: A letra M  </strong>representa o estado Modified, do português modificado. Isso significa que o arquivo 
 já existia no repositório, mas que recebeu alguma modificação que ainda não foi registrada no Git.

<strong> U: A letra U </strong>representa o estado Untracked, do português não rastreado. Isso significa que o arquivo 
ainda não existia no repositório e que ainda não teve seu registro (commit) feito no Git. </P>

<hr>

---

<h2> Baixando novos commits -- git pull</h2>

o repositório local não atualiza automaticamente, 
Para isso, existe o comando git pull especificamente para isso. 
Ele funciona como o oposto do push, já que puxa os commits do remoto para o local.
além de git pull, na mesma linha de código indicamos qual é o repositório remoto do qual baixaremos esses commits,
nesse caso será o origin. Em seguida, passamos a branch main, onde ele trará esses commits para o repositório local.

> git pull origin main

Portanto, o comando git pull tem esse objetivo, baixar os novos commits
 que outras pessoas colaboradoras do seu repositório enviaram para o GitHub. 
 Com isso, temos um fluxo de trabalho.

--- 

<h3> Fluxo de trabalho Git </h3>

Quando estivermos trabalhando em um projeto e precisarmos realizar mudanças, 
usaremos o git status para verificar os arquivos modificados.
Adicionaremos essas mudanças com o comando git add, depois, 
realizaremos um commit com o git commit. 
Subiremos essas mudanças para o repositório com o git push e eventualmente, 
conforme outras pessoas forem colaborando com o projeto, traremos essas mudanças 
novamente para o computador com o git pull.
Cada pessoa faz o clone do repositório local e centralizam no repositório remoto do GitHub, 
permitindo a colaboração de todos.

---

<h2> Resolvendo Conflitos </h2>
Quando trabalhamos em grupos outras pessoas enviam atualizações, 
Para baixar esses commits, precisamos acessar a aba de Controle de Origem, ou seja, 
a integração com o Git. Em seguida, clicamos no terceiro ícone da barra lateral esquerda. 
Nessa aba, clicaremos no botão "Views and More Actions" (Views e Mais Ações),
 que tem o ícone de reticências (…) e fica no canto superior direito da aba.
Com isso, abrimos um menu suspenso onde a terceira opção é "Pull" (Puxar). 
Ao clicarmos nele, baixamos os commits dos outros colaboradores do projeto.

Quando o Git for tentar baixar o commit que ambos estão alterando o mesmo arquivo, na mesma linha.   haverá um conflito com o meu commit, porque ambos estão alterando o mesmo arquivo, na mesma linha. 

Ao clicarmos no Pull, ele tenta sincronizar e mostra uma mensagem de erro. Inclusive, apareceu um pop-up, no canto inferior direito do Visual Studio Code, informando que houve um conflito ao tentar fazer o merge (fusão), desses commits.
se houver um conflito no mesmo arquivo e na mesma linha, 
ele não consegue distinguir qual versão manter.
O Git não escolhe uma versão, ele nos deixa decidir qual versão deve ser mantida

O Git detecta que houve um conflito e até mostra um botão azul, no canto inferior direito da tela, escrito "Resolve in Merge Editor". Se clicarmos nesse botão, poderemos resolver o conflito em uma ferramenta de edição de conflitos.

depois de resolver o conflito precisamos fazer o Commit novamente e
depois o botão de sincronização, para enviar 

no github 
Ao clicarmos no link dos commits, no canto superior direito, acessamos o histórico e notamos que ele mostra o commit de alteração também mostra o  commit do outro colaborador, e o commit que resolveu esse conflito dos dois commits anteriores.
é assim que funciona quando há um conflito: o Git marca no código, nós resolvemos o conflito fazendo um novo commit, e então tudo fica em ordem no repositório,

<h1> Git Revert - Desfazendo um commit</h1>

<p>
    Cada commit representa uma versão do código, que fica registrada no histórico.
    Conhecemos o git-log e conseguimos conferir todo o histórico de versões.
    E, eventualmente, vamos querer voltar no tempo, pois alguém pode pedir para desfazer uma alteração.

    poderíamos entrar no site do GitHub, clicar na lista do log para ver os commits e encontrar qual foi 
    o commit que fez essa alteração.  Lembre-se de que é possível detalhar o que aquele 
    commit fez no código e quais arquivos foram modificados

    Vamos abrir o VS Code e, naquela ferramenta do GitHub que estávamos utilizando no próprio VS Code, 
    para abrir o log, aquele histórico dos nossos commits. 
    A ferramenta é a "Source Control", no terceiro botão do menu lateral esquerdo.

Clicando nessa ferramenta, temos o menu de três pontos 
(botão "Views and More Actions"). Vamos clicar nele e verificar se temos a opção de log.
 Procurando nas opções, não vemos nenhuma que mostre nosso histórico de commits.

Começamos a usar essa integração do Visual Studio Code com o Git,
 mas nem todos os comandos estão disponíveis via menu. Os mais comuns, como ver o status, 
 qual arquivo foi modificado, fazer um commit, ADD, push, pull, são exibidos.
 Mas, se quisermos executar um log ou outros comandos mais avançados,
 e que não são tão comuns,  o VS Code não mostra. 
 <strong> Sendo assim, teremos que usar o terminal novamente. </strong>

 vamos rodar o comando git log, que já conhecemos. 
 > git log
 Como vimos anteriormente,  esse comando traz algumas informações dos nossos commits. 
 Cada commit possui um ID, o qual identifica esse commit de maneira única.
 O ID único é a maneira pela qual o Git diferencia cada commit. 
 É como se fosse um ID de registro no banco de dados.  
 Precisamos saber qual é o commit que queremos desfazer e, para isso, usaremos esse ID.
 então vamos copiar o ID dele (o código de letras e números ao lado de "commit").
 ex. commit 2ad48c068dc9677fb57efec70620700410f976b0
 Em seguida, pressionamos a tecla "Q" para retornar ao nosso terminal. 
 O comando para reverter um commit é o git revert, passando ao lado o ID do commit a ser desfeito.
 > git revert 2ad48c068dc9677fb57efec70620700410f976b0

Executando o comando git revert, é aberta uma pequena janela no topo da tela. Isso acontece porque o git revert
é o comando responsável  por realizar o processo de identificar o commit pelo ID passado como parâmetro, 
analisar cada alteração feita por ele e desfazer essas alterações sozinho.
Entretanto, o revert não desfaz as alterações modificando apenas os arquivos. 
Ele cria um novo commit para registrar esse revert.
 o revert já nos fornece uma mensagem para esse novo commit,
 dizendo que realizou um revert e traz a mensagem do commit original,
  por exemplo, além do ID desse commit.

Revert "removendo foto"
This reverts commit 2ad48c068dc9677fb57efec70620700410f976b0.

Fechando esta janela, essa mensagem já ficará salva para o novo commit.

Agora, vamos executar o comando git log no terminal para verificar o que aconteceu.

Na lista de commits, foi retornado esse novo commit no topo da lista,
 indicando que ocorreu um revert do commit. 

na verdade, o revert não apaga o commit original. O que ele faz é criar um novo commit que efetua uma 
espécie de "Ctrl + Z" no commit original. Todos os arquivos modificados pelo commit original 
têm suas alterações desfeitas, mas o revert fica registrado no histórico.

No entanto, como é um novo commit, ele está apenas no nosso repositório local. 
Portanto, quisermos enviá-lo para o GitHub, será necessário sincronizar, 
rodando novamente o seguinte comando no terminal:

    git push origin main

Com isso,sincronizamos e enviamos esse commit de 
revert para o repositório remoto, permitindo que outras pessoas possam baixá-lo.

Nós fizemos o revert, desfizemos a alteração de um determinado commit. O próprio git se encarregou de olhar cada arquivo, 
desfazer as respectivas alterações e registrar isso no histórico, revertendo o código para a versão anterior.

</p>

<h2> git reset - Resetando um commit </h2>

<p> 
aprendemos como desfazer um commit utilizando o comando git revert.
 Esse comando gera um novo commit com essa mudança, desfazendo todo o código
 que foi alterado naquele determinado commit.

existem situações em que não queremos, de fato, desfazer um commit. 
Na verdade, queremos apagar o commit do histórico.
Por exemplo, nós podemos estar trabalhando em uma funcionalidade que no meio do caminho é cancelada, 
sendo que nós já tínhamos alterado os arquivos e feito um ou mais commits. 
Então, aqueles commits não fazem mais sentido no histórico e queremos apagá-los.

podemos rodar um log para visualizar esse commit no histórico, mas terá que ser pelo terminal.
Da mesma forma que o revert, se queremos apagar um commit,
 vamos precisar do ID do commit em questão para identificá-lo.

O comando para apagar um commit é o git reset --hard junto do ID do commit.
> git reset --hard a3322db2eb6f82162977169f5461fc93b81bfac1
Um detalhe importante: o parâmetro --hard foi colocado porque o comando reset possui
 algumas opções, alguns modos de realizar esse reset.
  O parâmetro --hard serve para apagar o commit e também apagar a mudança no código.

Na verdade, com o comando reset utilizando a opção --hard, 
temos que passar o ID do commit, mas não é o ID do commit que queremos resetar,
 mas sim o ID do comando anterior. o qual queremos voltar pra ele
  temos que passar o ID da versão a que queremos retornar. 
  Ou seja, esse comando retorna ao estado do commit indicado pelo ID.
Ao dar "Enter", uma mensagem aparece indicando que nosso HEAD agora está no início do ID,
que identifica nosso commit.

> Além do comando revert, que nos permite reverter uma mudança mantendo o commit e criando um novo,
> temos o comando reset para quando queremos apagar um determinado commit, excluí-lo do histórico 
> porque ele não faz mais sentido.
> Nós apresentamos essas duas situações: em uma delas estamos revertendo um commit, 
> na outra estamos apagando um commit. Mas há uma terceira situação possível.
</p>



<h2> Arquivos que queremos que o Git Ignore</h2>

No caso do nosso projeto, criamos um repositóroi, que é a pasta principal do projeto. 
Todos os arquivos contidos nela, como style.css, index.html, app.js, até mesmo os diretórios,
como a pasta .img e todos os arquivos internos dela, serão rastreados pelo Git quando
 usamos o comando git add..

No entanto, pode haver uma pasta ou arquivo específico que desejamos que o Git ignore. Talvez seja um arquivo ou diretório necessário para a execução do projeto localmente, mas que não faz sentido compartilharmos com outras pessoas. Cada uma terá seu arquivo ou diretório específico, portanto, não queremos enviar para o GitHub.

Porém, se adotarmos essa estratégia, teríamos que ter cuidado ao realizar um commit para não usar git add., 
caso contrário, o Git incluiria automaticamente o diretório que gostaríamos de ignorar.
 E então, teríamos que ficar adicionando individualmente cada arquivo, o que não seria nada produtivo.

Existe um recurso que nos permite criar um arquivo para informar ao Git quais diretórios
 e arquivos do projeto ele deverá ignorar. Esse arquivo é chamado de .gitignore. 
 Podemos criar um arquivo com esse nome no nosso projeto.

 No Visual Studio Code, criaremos um novo arquivo. O nome desse arquivo deve ser .gitignore, 
 com um ponto no início, pois será um arquivo oculto. Após criar o arquivo .gitignore, 
 incluiremos nele quais arquivos e diretórios do projeto queremos ignorar.

 Por exemplo, vamos supor que temos uma pasta chamada temp/ no projeto, que é uma pasta temporária, com arquivos temporários. Estamos adicionando essa pasta no arquivo .gitgnore para que o Git ignore esse arquivo. Se tivermos outros arquivos e diretórios, cada um deles estaria separado por linhas.

Portanto, na linha abaixo, poderíamos colocar arquivo.txt passando um nome específico ou padrão,
 por exemplo, *.css. Nós usaremos apenas o temp/. Com isso, estamos dizendo, basicamente, 
 para o Git: "Ignore a pasta temp do projeto".
> .gitignore

> *.doc 

> temp/

> PastaTXT/  

Ao invés de criarmos o .gitignore manualmente, precisando lembrar quais são os arquivos e diretórios daquela linguagem, daquela tecnologia, existem sites que nos auxiliam nessa tarefa.
Existem sites geradores de .gitignore para cada tecnologia.

Um desses auxiliadores é o site gitignore.io, que é um site utilitário.
 Nele, indicamos a tecnologia ou a linguagem de programação, por exemplo, Java, 
 e apertamos o botão "criar". Com isso, ele retorna como seria um .gitignore para um projeto com Java.

---
##  Compartilhar trechos no código

 GitHub oferece um recurso para quando desejamos compartilhar trechos de códigos com outras pessoas, sem a necessidade de criar um repositório e realizar todo o processo de commits que realizamos.

Abrindo o site do GitHub, no ícone de "+ (mais)", no canto superior direito, além da opção de criar um novo repositório, encontramos outras opções. Dentre elas, temos uma chamada "New Gist".

Ao selecioná-la, seremos direcionados para um formulário. A ferramenta GitHub Gist foi desenvolvida pelo próprio GitHub para compartilhamento de códigos. A descrição inclusive menciona "compartilhe códigos de maneira instantânea, comentários ou trechos de códigos pontualmente".

Nós podemos criar um "Gist" e, assim que a criação for realizada, será gerada uma URL que copiaremos e compartilharemos com outras pessoas.

Ao final da página, existe um botão verde, "Create secret gist", que serve para criarmos o Gist. E ele também tem a opção de ser um Gist público ou secreto. 
Funciona da mesma forma que o repositório. Se for público, pessoas podem acessar os Gists que criamos. Se for privado, somente a pessoa responsável pelo arquivo pode compartilhá-lo com outras pessoas. O Gist privado não aparece na página do usuário no GitHub.
O endereço que está na barra de endereços do navegador é o que compartilharemos com outras pessoas

--- 
--- 

# Branches

## Ramificando o trabalho


# Branches

## Ramificando o trabalho

    Temos nosso projeto desenvolvido e queremos começar a trabalhar em outra funcionalidade. 
    Para isso, podemos criar uma ramificação, um galho na nossa árvore. Isso é o que chamamos de branch.
    Se digitarmos o comando git branch ele vai mostrar quais são as branches, isto é, 
    quais são as ramificações existentes no nosso trabalho.

 `   git branch `

    Por padrão, só temos a branch main, que o Visualizing Git chama de master. Antigamente, 
    a branch principal se chamava master, mas essa nomenclatura padrão foi alterada para main. 
    Sendo assim, hoje em dia, a branch padrão se chama main.Se quisermos renomear a master para main, 
    usamos o comando abaixo:

`  git branch -m master main  `
    
    Se quisermos remover alguma branch, caso tenhamos uma lista de várias branches, podemos usar o 
    comando git branch -d seguido do nome da branch que queremos remover. Por exemplo: 
    git branch -d master 
 
## Criando uma nova ramificação

git branch

Poderíamos usar o comando git branch seguido de uma nova branch que quisermos, referente a qualquer nova funcionalidade. Porém, se quisermos criar uma branch e já mover para ela, podemos usar dois comandos. 
O primeiro é o git checkout -b seguido do nome da nova branch nova-funcionalidade.

git checkout -b nova-funcionalidade

Além desse comando mais antigo, podemos utilizar o git switch, também seguido do nome da branch desejada. "Switch" significa trocar, ou seja, esse comando basicamente alterna entre branches.

Porém, se digitarmos simplesmente git switch nova-funcionalidade, será informado que essa branch não existe. Então, vamos executar git switch -c nova-funcionalidade (-c referente a "create").

git switch -c nova-funcionalidade

Agora temos uma nova ramificação do nosso trabalho.
 Podemos fechar o terminal e adicionar alguma modificação no código.

git status

com isso, ele mostra que estamos na branch nova-funcionalidade. 
Vamos adicionar o arquivo index.html com o comando git add, 
e depois adicionar um commit com a mensagem "estamos no branch nova-func".

` git add index.html
git commit -m "estamos no branch nova-func" `

Se fizermos um git log agora, temos um retorno um pouco diferente.

` git log`

Temos o commit anterior, do merge na branch main; temos o origin/main;
 agora o último commit é onde está o HEAD atual; e temos a branch nova-funcionalidade.
  Repare que a branch nova-funcionalidade ainda não foi para o origin, pois não enviamos.
  Porém, antes de enviar, vamos fazer um switch e voltar para branch main:

`git switch main`

A funcionalidade que estamos desenvolvendo está nessa branch, isto é, o commit existe nela, 
não descartamos ele. Porém, voltamos a trabalhar na linha de trabalho principal main.

Se voltarmos para o terminal e executarmos git log, o head terá voltado para main. 
Então, o HEAD é onde estamos no momento, é o commit atual onde o nosso projeto está.

Dito isso, vamos fazer um git switch para nova-funcionalidade:

`git switch nova-funcionalidade`

Mais uma vez, o código aparecerá atualizado com o que adicionamos.
 Assim, podemos fazer o git push para o repositório remoto, ou seja, 
 origin da branch nova-funcionalidade.

`git push origin nova-funcionalidade`

**Após teclar "Enter", a nova ramificação será criada e teremos uma nova linha de trabalho.**

[https://git-school.github.io/visualizing-git/](https://git-school.github.io/visualizing-git/)

> *obs.: git checkout é um comando “antigo” e que há alternativas mais modernas. É importante ressaltar que o comando checkout continua funcionando e não há nenhum indício de que ele será removido do git, mas devido à sua grande complexidade, ele foi separado em dois comandos diferentes: o git switch, que também vimos nessa aula,
 e o git restore,*

>Note que fizemos o push de nova-funcionalidade, e no GitHub, ele exibe uma mensagem que indica que podemos criar uma pull request a partir da nossa nova branch.

>O GitHub já identificou que existe uma nova branch e que, em algum momento, vamos querer unir a branch nova-funcionalidade com a main, que é a branch principal.

## Unindo a nova Branch na Main

Criando a nova branch

use: 
  ```markdown
  git branch newbranch  
  git checkout newbranch
  ```
ou

  `git checkout -b newbranch`         -- cria e move para ela 

faz as alterações necessárias na nova branch

```markdown
  git add .
  git commit -m 'msg newbranc'
```

essas alterações ficam só na newbranch, 
quando desejar juntar essas alterações a main

`git checkout main
git merge newbranch ` 

resolve os conflitos e faz o commit da nova branch

## Fazendo um merge commit
Estamos no cenário onde as duas branches evoluíram de forma independente. Este é o cenário mais comum: trabalhamos na branch de alguma funcionalidade, e outras funcionalidades foram adicionadas à main, outras coisas foram feitas e já estão na linha de trabalho principal.

Sendo assim, quando fizermos um git switch para main e tentarmos fazer um git merge de nova-funcionalidade, o Git vai entender que esses dois trabalhos estão independentes e não evoluíram de forma igual. Dessa forma, ele irá unir criando um novo commit automaticamente. Ele criará um novo commit de merge, ou merge commit, como normalmente é chamado nas documentações.

```markdown
git switch main
git merge nova-func
```


Com esses comandos, será aberto um editor que permite a alteração da mensagem de commit de merge. 
No nosso caso, vamos deixar o commit como está.

Como o editor é o VI, basta executar :x para salvar e sair. Ao final, teremos um novo commit criado. Se executarmos o comando git log --graph, podemos observar o que acontece na main.
por último mostra o merge commit, isto é, o commit de mescla.

Reparem que bifurcamos o nosso trabalho e depois unimos. Lembrando que tudo isso é feito automaticamente pelo Git, mas é importante entender que existem essas duas estratégias: de fast forward e de criação do merge commit.

Dessa forma, conseguimos unir trabalho de duas branches diferentes para ter tudo na linha principal;
 unimos à linha principal, então agora podemos fazer deploy da nossa aplicação.

Para finalizar, vamos executar o comando git push origin main para atualizar a main com todo o trabalho novo.
 Em seguida, removeremos a branch nova-funcionalidade com git branch -d,
  para manter o projeto limpo e sem excesso de branches.

```markdown
git push origin main

git branch -d nova-funcionalidade

```
---
--- 
## Para saber mais: pull requests

>O GitHub possui uma funcionalidade chamada Pull requests, que é uma sugestão de alteração em determinado repositório. Outras ferramentas, como o GitLab, podem chamar essa mesma ferramenta de Merge requests.
Essa sugestão de alteração é, de forma resumida, a abordagem que adotamos ao colaborar com equipes para adicionar novas funcionalidades ou corrigir alterações. Ao invés de manualmente mesclarmos o código de nossa branch com a main, nós criamos um pull request (ou merge request), pois dessa forma a alteração fica mais visível para toda a equipe e permite que outras pessoas possam revisar esse trabalho.

## comando mágico chamado git rebase

[git rebase](https://cursos.alura.com.br/course/git-github-dominando-controle-versao-codigo/task/150397)

criamos uma nova branch chamada nova-funcionalidade e estamos trabalhando nela. Enquanto trabalho nessa branch, outras pessoas podem ter criado outros branches e já se uniram à linha principal, à main. Normalmente, essa main é o projeto final que pode ser enviado à produção. É o projeto com todas as funcionalidades que estejam completas.

Estamos criando uma nova funcionalidade, porém queremos testá-la na versão mais recente do projeto. Repare que, a partir do momento em que criamos a nova-funcionalidade, dois outros commits também foram criados, ou seja, duas funcionalidades foram adicionadas no projeto principal.

Queremos garantir que o que estamos desenvolvendo funcione, mesmo com as funcionalidades que as outras pessoas criaram. Queremos garantir que tudo se integre da forma correta.

Sendo assim, queremos fazer com que a branch nova-funcionalidade não seja criada a partir da versão antiga da branch maine sim da versão mais nova.

Portanto, queremos reescrever a história, fazendo com que o primeiro commit da nova funcionalidade venha logo após do momento atual da main atualizada. Queremos fazer com que a branch nova-funcionalidade, seja reescrito para ter todas as funcionalidades da main antes dela.

Isso pode ser feito com um comando mágico chamado git rebase, que faz muita coisa, como reescrever a história dos commits. Então, se estivermos em nova-funcionalidade e executarmos o comando git rebase main, ele pegará todos os commits da main que não estão na branch nova-funcionalidade, e tentar adicionar um a um antes da branch nova-funcionalidade.

`git rebase main`

Ele pegará o primeiro commit e tentar adicionar antes do commit nova-funcionalidade. Pegará o próximo commit, que é o último da main, e tentar adicionar antes do commit nova-funcionalidade. Após isso, pega todos os commits da nova-funcionalidade e aplica depois do último da main.

Pode parecer bastante complexo, mas se visualizarmos o que está acontecendo, talvez fique um pouco mais fácil. Ele primeiro traz o head para a main e depois aplica tudo da nova-funcionalidade, cada um dos commits, depois. Vai aplicando commit a commit depois da última coisa que estiver na main.


> Recapitulando novamente. Temos duas branches independentes, uma main e uma nova-funcionalidade. Se queremos garantir que essa nova-funcionalidade agora tenha tudo o que tem na main também, podemos fazer o rebase.
>  
> O rebase fará o quê? Se estamos na nova-funcionalidade e tentamos fazer o rebase com a main, ele vai alterar o branch para ir para a main. Depois da main, ele vai aplicando cada um dos commits da nova-funcionalidade. Isso é feito commit por commit, porque se tiver algum conflito em algum dos commits, vamos resolvendo um a um. Dessa forma, conseguimos reescrever a história.
a.> 
> 
> Reparem que agora o nova-funcionalidade possui dois commits com hashes diferentes, porque vieram de outro lugar a partir de uma nova história. 

* O merge junta os trabalhos de duas branches, podendo gerar um merge commit. Já o rebase aplica os commits de outra branch na branch atual. O trabalho do rebase é equivalente ao que vimos na prática como fast forward do merge. Ao realizar o rebase, todos os commits da outra branch são adicionados antes do primeiro commit da nossa branch atual, reescrevendo a história. Isso faz com que novas alterações possam ser integradas à nossa branch e permite que quando formos realizar o merge, não seja necessário um merge commit, garantindo o fast forward.

* **Lembre-se:** sempre criamos commits quando o nosso projeto está em um estado funcional.

--- Guardando as alterações feitas - git stash 

https://cursos.alura.com.br/course/git-github-dominando-controle-versao-codigo/task/150398gi


--- 
## Guardando para depois - git stash
---
`git stash`
Agora, imagine o seguinte cenário: Estamos desenvolvendo uma funcionalidade grande. Estamos no meio da implementação dela, ela ainda não está pronta. No entanto, precisamos interromper o trabalho nela para resolver um bug urgente ou mudar nosso foco para alguma correção pequena que seja urgente. Ou seja, queremos interromper nosso trabalho. Como estamos no meio de uma funcionalidade, nosso código pode não estar compilando ou não 
estar em um estado que possamos criar um commit.
> Lembre-se: sempre criamos commits quando o nosso projeto está em um estado funcional.

Se o código está compilando, se está, pelo menos, executando da forma esperada. Portanto, não vamos criar um commit com nosso código em um estado incompleto. O que fazemos se nos deparamos com um cenário onde estamos no meio da implementação de uma funcionalidade, mas precisamos interromper aquele processo? 

--- 

--- 
## Guardando para depois - git stash
---
`git stash`

Agora, imagine o seguinte cenário: Estamos desenvolvendo uma funcionalidade grande. Estamos no meio da implementação dela, ela ainda não está pronta. No entanto, precisamos interromper o trabalho nela para 
resolver um bug urgente ou mudar nosso foco para alguma correção pequena que seja urgente. Ou seja, 
queremos interromper nosso trabalho. Como estamos no meio de uma funcionalidade, nosso código pode não 
estar compilando ou não estar em um estado que possamos criar um commit.

> Lembre-se: sempre criamos commits quando o nosso projeto está em um estado funcional.

Se o código está compilando, se está, pelo menos, executando da forma esperada. Portanto, não vamos criar um commit com nosso código em um estado incompleto. O que fazemos se nos deparamos com um cenário onde estamos no meio da implementação de uma funcionalidade, mas precisamos interromper aquele processo? 

### Criando uma nova funcionalidade

Primeiro, se estamos criando uma nova funcionalidade, vamos criar um novo branch. 
Portanto, escreveremos no terminal `git switch -c movendo-detalhes`.

Estamos em uma nova branch, podemos criar nossa nova funcionalidade. 

fomo interrompidos: Um bug muito urgente surgiu, 
então precisamos trabalhar em outra coisa. O que acontece?

Não podemos criar um commit agora. Nosso projeto está em um estado inválido, removemos a chamada de função.
 Além disso, se executarmos um git status, temos modificações. Portanto, não podemos começar a trabalhar em outra coisa e ir para outro branch, porque o arquivo app.js está modificado. Precisamos desfazer essa alteração, mas guardar o que já alteramos.

 ## Guardando as alterações feitas
 O que queremos fazer é engavetar a alteração que fizemos até agora, mas sem criar um commit. Queremos guardar ela para depois, queremos estocar ela para depois poder recuperar e continuar trabalhando. E é exatamente isso que o comando git stash faz. Ele guarda uma alteração para continuarmos trabalhando nela depois.

Se executarmos o comando `git stash`, ele vai pegar tudo o que está no nosso estado atual e estocar. Ele vai guardar para que possamos recuperá-lo depois.

O git stash nos diz que salvou o nosso estado na nossa gaveta, no nosso estoque ("Saved working directory and index state WIP on movendo-detalhes: linha do script"). Portanto, se voltarmos para o nosso arquivo, ele estara no seu estado válido, ele voltou lá com a nossa alteração.

depois que cuidamos do bug e podemos voltar para esse branch de nova funcionalidade e retomar o trabalho,
recuperar o que está no nosso stash.

### Recuperando as alterações

Podemos executar o comando git stash pop. Esse pop, ele aplica o que tiver na nossa gaveta, no nosso estoque.

`git stash pop`

Após executarmos o `git stash pop`, o que estava guardado é aplicado novamente ao código.

> Portanto, o git stash guarda uma alteração para que ela possa ser retomada depois.

> Ele guarda um estado para que possamos retomá-lo depois. E normalmente é utilizado quando estamos no meio de uma alteração, queremos guardar algo rapidamente para corrigir um bug e trabalhar em outra coisa rapidamente e depois voltar a trabalhar nisso. Portanto, não podemos criar um commit.

 Se executarmos o comando `git stash list`, ele lista tudo o que está nesse nosso estoque.

$ git stash list
stash@{0}: WIP on movendo-detalhes: c53eb16 Quebrando linha do script
stash@{1}: WIP on main: c53eb16 Quebrando linha do script
$

> Mas repare que os nomes que esse nosso git stash list nos mostra não são muito descritivos. 
> Ele coloca um work in progress (WIP) na branch que estávamos e o último commit antes de adicionarmos esse stash. Portanto, isso não é muito útil.

### Limpando as alterações guardadas

`git stash clear`

podemos limpar a nossa stash, apagar tudo? 
Podemos fazer um git stash clear, limpamos a nossa stash.
Portanto, se fizermos o git stash list, não tem mais nada lá.

### Acrescentando uma descrição à stash

Agora, se quisermos adicionar algo a nossa stash, mas com um nome mais descritivo,
 **podemos fazer, ao invés de só git stash,** vamos escrever git stash push -m. 
 E aí, podemos adicionar uma mensagem qualquer, será "Movendo chamada de função".

` git stash push -m "Movendo chamada de função"`

E se fizermos um git stash list, temos um nome bem mais descritivo. 

### Entendendo a pilha de modificações

Se fizermos um git stash pop, ele sempre vai aplicar a última alteração que adicionamos.
 Portanto, ele sempre pega esse de índice zero. Ele sempre vai empilhando modificações.

O que isso quer dizer? Imagina que essa nossa stash é uma gaveta e nessa gaveta estamos guardando pratos. Portanto, abrimos a gaveta, colocamos um prato. Na gaveta, adicionamos outro prato em cima. 
Se vamos pegar um prato, pegamos o prato que está em cima, certo?
 Portanto, é o último que adicionamos. Isso é o conceito de pilha.

> Temos aqui na stash uma pilha de modificações. Portanto, quando fazemos pop, sempre aplicamos a última que adicionamos. 



ENTENDENDO O CONCEITO PILHA
---

Se fizermos um git stash pop, ele sempre vai aplicar a última alteração que adicionamos.
 Portanto, ele sempre pega esse de índice zero. **Ele sempre vai empilhando modificações.**

O que isso quer dizer? Imagina que essa nossa stash é uma gaveta e nessa gaveta estamos guardando pratos. Portanto, abrimos a gaveta, colocamos um prato. Na gaveta, adicionamos outro prato em cima. Se vamos pegar um prato, pegamos o prato que está em cima, certo? 
Portanto, é o último que adicionamos. **Isso é o conceito de pilha.**
Temos aqui na stash uma pilha de modificações. Portanto, quando fazemos pop, sempre aplicamos a última que adicionamos. 

---

### Retomando alterações anteriores à versão mais recente

`git stash apply`

quando queremos aplicar algo que está na stash anterior à versão mais recente, podemos fazer o git stash apply e o índice. Podemos aplicar várias stashes se elas não estiverem no mesmo arquivo, se elas não forem conflitar com o que temos.

> git stash:
> se temos alguma alteração que precisamos adicionar ou salvar para depois, chamamos o comando `git stash.` 
> O comando git stash vai adicionando mensagens no formato de pilha. 
> 
> Se queremos pegar algo e aplicar uma alteração à última stash que adicionamos, usamos `git stash pop`;
> 
> Se queremos aplicar alguma específica, usamos `git stash apply`;
> 
> Se queremos adicionar algo na nossa stash com mensagem, usamos `git stash push`;
> sem msg seria `git stash`;
> 
> Se queremos limpar a nossa stash, usamos `git stash clear`.
> O comando git stash clear limpa a stash, ou seja, apaga tudo que foi salvo com o comando git stash. 
> Caso você queira remover apenas um único item da stash, você pode utilizar git stash drop.
> 
> se queremos ver a nossa lista,  usamos ` git stash list`

### Para saber mais: pop, drop e apply

Os comandos pop, drop e apply do git stash possuem semelhanças e diferenças bem importantes, então vamos fazer um pequeno resumo de suas funcionalidades aqui:

#### Apply
O comando git stash apply espera um índice de um item na stash e o aplica ao repositório, porém, esse comando não remove o item da stash, ou seja, se após executar o comando git stash apply 1 você executar git stash list, o item referente ao índice 1 continuará na stash.

#### Pop
O git stash pop faz exatamente a mesma coisa que o git stash apply, porém, além de aplicar o item da stash, ele também o remove de lá. Esse comando, sem nenhum parâmetro extra, vai aplicar o último item adicionado à stash, mas nós também podemos informar um índice para ele, como git stash pop 1.

#### Drop
O git stash drop funciona exatamente como o pop, mas com uma simples diferença: ele apenas remove o item da stash, sem aplicá-lo em nosso repositório. Dessa forma, git stash drop remove o último item adicionado à stash, enquanto o git stash drop 1 remove da stash o item com índice 1.

--- 

### git restore  - Descartando várias alterações

Imaginem que nós estamos criando alguma modificação. Temos vários arquivos modificados e alterados. 
Porém, nós percebemos que a implementação está incorreta ou a funcionalidade não será mais implementada. Basicamente, queremos descartar o que foi feito.
> Se temos apenas um arquivo, para descartar essa modificação, podemos fazer um Ctrl + Z.
Mas, se temos vários arquivos, sair fazendo Ctrl + Z em muitos lugares pode ser bastante cansativo.
Para isso, podemos utilizar o git.

Então, nosso git status tem modificações. E o que queremos fazer é desfazer essas modificações.
Nós não fizemos git add e não commitamos isso. 
> Como não foi commitado, não é um revert, nem um reset. 

O que queremos fazer é restaurar o nosso local de trabalho para um estado válido, sem essas modificações.
Então, queremos fazer um git restore.

> Podemos fazer o restore para algum estado específico, mas se não informarmos o estado, isso significa que a restauração será feita sem o que foi modificado. Ou seja, o último commit do nosso branch atual.

Então, queremos fazer o restore de quê? Podemos fazer de app.js e de index.html um de cada vez. Ou fazer do ponto (git restore .). Assim como já aprendemos que o git add . adiciona o projeto todo, o git restore . restaura todo o projeto também. E esse ponto não é um significado especial do git.

> Na linha de comando, o ponto significa o diretório atual. Então, estamos fazendo o restore de tudo na pasta atual.

Então, esse git restore vai fazer um **Ctrl + Z no nosso projeto**. Assim, as linhas que adicionamos serão apagadas, de todos os arquivos que alteramos e não commitamos ainda. Então, com isso, se fazemos um git status, temos o nosso projeto limpo novamente.

E o `git restore` é um dos comandos que veio para substituir o `git checkout`. Então, o git checkout, como dissemos, faz muitas coisas. Uma das coisas que ele fazia é o restore. Com o `git checkout -- .`, temos o mesmo resultado.

> O git restore restaura o projeto ou restaura arquivos específicos para algum ponto específico. Por padrão, ele faz o restore para head, ou seja, para o nosso último commit, que no nosso caso aqui é quebrando a linha do script.

--- 

#### git restore --staged 

Vamos supor que fizemos alterações em um arquivo; e adicionamos com o git add arquivo.html 
para fazer o commit. então, ele está no "stage", pronto para ser comitado. 
Isso é o que chamamos de "stage" ou "staging area". Mas, o que acontece se quisermos desfazer isso? 
Não estamos prontos para comitar. Queremos fazer mais alterações ou simplesmente desistir dessa modificação.

Note que o próprio git já nos mostra que podemos fazer um restore do que está em nossa "staging area". Se fizermos git restore --staged, significa que estamos modificando algo que está dentro dessa "staging area", dentro de algo que fizemos com o git add.

Assim, com `git restore --staged arquivo.html`, 
não desfazemos a alteração, mas retornamos ao estado anterior. Agora, é como se não tivéssemos feito o git add. 

Agora, se quisermos desfazer as alterações, fazemos o `git restore arquivo.html`.
Sendo assim, desfizemos as alterações. Repare a diferença entre o --staged e o staged.

Um outro parâmetro que podemos passar para o restore é, suponha que queremos mover nosso arquivo.html para o estado que estava quando fizemos o Merge branch 'nova-func' into main.

O que podemos fazer? Podemos copiar o hash do commit, fazer o git restore --source = e colá-lo em seguida. Queremos restaurar para esse estado nosso arquivo.html. O comando inteiro ficará parecido com o seguinte:

`git restore --source = 5081a55bc92af2917c8519f16a7412b86ba3b1c2 arquivo.html`

Quando fazemos isso, ele pega o arquivo e o coloca no estado que estava nesse commit.

Mas, se quisermos apenas visualizar o arquivo e entender como ele estava naquele estado, podemos desfazer esse trabalho, ou seja, restaurar para o estado normal dele com o git restore arqiuvo.html, que é equivalente a fazer --source = head.

> Fazer o restore sem esse --source é equivalente a fazer --source = head, que corresponde ao último commit que temos no branch atual.

--- 

> Working Tree (Árvore de Trabalho): É o espaço onde você está trabalhando nos arquivos do seu projeto. Aqui, você pode fazer alterações, adicionar novos arquivos ou modificar os existentes. Basicamente, é o que você vê e edita diretamente no seu computador.

Staging Area (Área de Preparação): É como uma "pré-seleção" dos arquivos que você deseja incluir no próximo commit. Quando você faz alterações nos arquivos e usa o comando git add, está colocando esses arquivos na staging area. Isso significa que eles estão prontos para serem salvos na próxima versão do seu projeto, mas ainda não foram efetivamente salvos.

--- 