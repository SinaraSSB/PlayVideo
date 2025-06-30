<h1> --- Iniciando o Repositório Local ---- </h1>
<p>
git init 

git add . 

git commit -m "First commit play video"

git branch -M main

git remote add origin git@github.com:SinaraSSB/PlayVideo.git   <i>ou</i>

git remote add origin https://github.com/SinaraSSB/playvideo.git  

git push -u origin main </p>

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

git remote add apelido url
 
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

git remote -v


<h3> 3 - Remover um repositório remoto: </h3>

Caso você não precise mais de um repositório remoto específico, 
pode removê-lo com o comando git remote remove apelido. Substitua 'apelido' 
pelo nome do repositório remoto que deseja remover. Aqui está um exemplo:

git remote remove origin

Após a execução deste comando, o repositório remoto chamado "origin" 
será desvinculado do seu projeto local.


<h3> 4 - Alterar a URL de um repositório remoto: </h3>

Às vezes, é necessário atualizar a URL de um repositório remoto, 
como quando a URL do servidor do GitHub é modificada ou quando você copiou a URL incorreta ao adicionar
 o repositório remoto. Use o comando git remote set-url apelido nova_url para realizar essa atualização. 
 Substitua 'apelido' pelo nome do repositório remoto e 'nova_url' pela nova URL que você deseja associar a ele.
  Aqui está um exemplo:

git remote set-url origin https://github.com/seu-usuario/seu-repositorio.git

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

 git clone https://github.com/SinaraSSB/alurabook.git

 <hr>

 <h2>

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
