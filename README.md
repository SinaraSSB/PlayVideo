<h1> --- Iniciando o Repositório Local ---- </h1>
<p>
> git init 

> git add . 

> git commit -m "First commit play video"

> git branch -M main

> git remote add origin git@github.com:SinaraSSB/PlayVideo.git   <i>ou</i>

> git remote add origin https://github.com/SinaraSSB/playvideo.git  

> git push -u origin main </p>

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

 -----------------------------------------------------------------------------------//---------------

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

<h2> git log </h2>

<p> comando em que conseguimos identificar quais commits foram realizados no projeto e quem fez.

Ao executá-lo é exibido o histórico dos commits que foram feitos ao longo do projeto.

Se analisarmos o retorno, retonhamos o primeiro commit que o Rodrigo fez para subir o projeto inicial.
 Identificamos o nome do autor, data seguido da mensagem. Logo acima temos o commit mais atual
 que é o que acabamos de fazer.  </p>
 
 --- 

<h3> VS -  Alertas ao lado do Nome do arquivo </h3>

 <p>  Quando estamos trabalhando em um projeto utilizando o versionamento Git e a IDE VSCode, 
 ao adicionar ou alterar algum arquivo aparece uma sinalização ao lado do nome desses arquivos. 

<strong> M: A letra M  </strong>representa o estado Modified, do português modificado. Isso significa que o arquivo 
 já existia no repositório, mas que recebeu alguma modificação que ainda não foi registrada no Git.

<strong> U: A letra U </strong>representa o estado Untracked, do português não rastreado. Isso significa que o arquivo 
ainda não existia no repositório e que ainda não teve seu registro (commit) feito no Git. </P>

<hr>

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

<h2> Adicionando colaboradores ao projeto</h2>
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