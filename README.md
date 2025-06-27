git init 

git add . 

git commit -m "First commit play video"

git branch -M main

git remote add origin git@github.com:SinaraSSB/PlayVideo.git

git remote add origin https://github.com/SinaraSSB/playvideo.git  

git push -u origin main

https://cursos.alura.com.br/course/git-github-compartilhando-colaborando-projetos/task/139310

https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

---------------------------------------------------------------------------

1 - Adicionar um repositório remoto:

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

2 - Listar os repositórios remotos:

Para listar os repositórios remotos associados ao seu projeto local, você pode utilizar o 
comando git remote -v. Isso exibirá uma lista de todos os repositórios remotos vinculados ao seu projeto, 
juntamente com suas URLs. Veja um exemplo:

git remote -v


3 - Remover um repositório remoto:

Caso você não precise mais de um repositório remoto específico, 
pode removê-lo com o comando git remote remove apelido. Substitua 'apelido' 
pelo nome do repositório remoto que deseja remover. Aqui está um exemplo:

git remote remove origin

Após a execução deste comando, o repositório remoto chamado "origin" 
será desvinculado do seu projeto local.


4 - Alterar a URL de um repositório remoto:

Às vezes, é necessário atualizar a URL de um repositório remoto, 
como quando a URL do servidor do GitHub é modificada ou quando você copiou a URL incorreta ao adicionar
 o repositório remoto. Use o comando git remote set-url apelido nova_url para realizar essa atualização. 
 Substitua 'apelido' pelo nome do repositório remoto e 'nova_url' pela nova URL que você deseja associar a ele.
  Aqui está um exemplo:

git remote set-url origin https://github.com/seu-usuario/seu-repositorio.git

Isso atualizará a URL do repositório remoto "origin" para a nova URL especificada.


5 - Alterar o apelido de um repositório remoto:

Se você deseja renomear um repositório remoto, use o comando 
git remote rename apelido novo_apelido. Substitua 'apelido' pelo nome atual do repositório remoto e
 'novo_apelido' pelo novo nome que você deseja atribuir a ele. Aqui está um exemplo:

git remote rename origin novo-origin

Isso renomeará o repositório remoto de "origin" para "novo-origin".

-----------------------------
-------------
O comando git push deve ser executado para sincronizar as mudanças do repositório local com o repositório remoto, 
ou seja, quando desejamos enviar os novos commits que realizamos em nosso repositório local para o repositório remoto. 
No entanto, para garantir uma conexão segura, é essencial configurar uma chave SSH no computador antes de
 executar esse comando.

Chave SSH
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

 O Git é uma ferramenta excelente para acompanhar a mudança entre versões de um mesmo projeto e, 
 dentre vários benefícios, nos ajuda a observar de perto o desenvolvimento do seu aprendizado.
  Tudo isso de uma forma organizada através dos commits.

Além disso, algo que é essencial no universo da tecnologia é apresentar o seu progresso 
para a comunidade e montar um portfólio dos seus projetos para demonstrar suas habilidades. 
Dessa forma, o GitHub é essencial para compartilhar e colaborar em projetos de programação de todo o mundo.
