**Comandos para o git**

`git init` // inicia a linha do tempo / Iniciar um repositório
na pasta que será o novo repositório Git.
`git add + nome_do_arquivo` // adiciona ou atualiza mudanças para irem para a linha do tempo.
`git add .` // adicionar tudo de uma vez.
`git commit -m "#"`// adiciona um ponto na linha do tempo // Quando adicionamos com o git add ainda não estamos persistindo os dados no histórico do Git, mas adicionando a uma área temporária onde podemos ficar levando e trazendo alterações até garantirmos que algo realmente deve ser salvo, então rodamos o git commit.
Para fazer um commit, precisamos adicionar uma mensagem ao pacote, então rodamos com o parâmetro -m "mensagem".
Depois de ter adicionado as alterações com git add
`git log` // visualiza os pontos na linha do tempo / commit / Para ver todo o histórico.
`git status` // informa o estado das alterações do nosso projeto
`git show` // apresenta determinado ponto na história
`git branch` // gerências novas linhas do tempo
`git branch nome` // Criando uma nova branch. Podemos rodar o comando git branch ou git checkout.
`git checkout -b + nome_da_nova_branch` // Criando uma nova branch e já trocando para ela.
`git branch -d + nome` // Deletando uma branch. 
`git push origin nome_da_branch` // Enviando uma branch para o servidor. Caso tenhamos criado uma branch em nossa máquina, precisamos enviar ela para o servidor com o comando push, explicado mais abaixo neste texto, e passar alguns parâmetros que são o origin e nome da branch.
`git push origin :nome_da_branch` // Deletando uma branch remota.
`git checkout master` e `git merge nome_branch` //  Juntando branches. Quando trabalhamos com branches, mais cedo ou mais tarde, vamos precisar juntar as nossas alterações com a branch master.
Para isso usamos o comando merge.
Exemplo: Imagina que vamos fazer um merge da branch nome_branch na master.
`git push origin master` // Enviando as alterações para o servidor. Depois que finalizamos nossas alterações, fechamos nossos commits, então devemos enviar os commits para o servidor. 

`git rm nome_do_arquivo_ou_pasta` // Apagando, movendo ou renomeando arquivos ou pastas sem estragar nosso histórico Git
Quando deletamos algum arquivo, movemos de pastas, o Git fica com um histórico de deleção de arquivo e adição de outro.

Para que isso não aconteça, existem comandos do Git que salvam nossas vidas, o git rm, para deletar, e git mv, para movermos coisas.
`git rm -r pasta` // Lembrando que, para remover pastas, é sempre necessário que ela esteja vazia ou que executemos o comando rm com o parâmetro -r para que a deleção seja recursiva.

`git mv nome_do_arquivo_ou_pasta destino` // Movendo ou renomeando arquivo ou pasta com Git.
`git reset nome_do_arquivo` // Revertendo alterações. Existem diversas maneiras de desfazer coisas com o Git. Desfazendo do stage.
`git reset HEAD .` // Para desfazer tudo.
`git checkout nome_do_arquivo` // Desfazendo alterações em um arquivo para o último commit.
`git checkout .` // Desfazendo tudo para o último commit.
`git reset --soft HEAD~1` // Desfazendo uma alteração, mas colocando ela em stage.
`git reset --hard HEAD~1` // Onde HEAD~1 é relacionado ao último commit. Desfazendo para o último commit sem colocar as alterações em stage.

`git push --all origin` // Mandar todas as novas branches locais para o servidor.
`git checkout nome_da_branch_existente` // Trocando de branch.
`git checkout` // manipula as linhas do tempo
`git merge` // unir linhas do tempo
`git reset nome_do_arquivo` // Removendo arquivos do index, Para remover um arquivo do stage rodamos o comando reset.
`git reset HEAD` // Para remover tudo
`git diff` // Será retornado uma lista de itens que foram alterados
`git remote -v` // Listando o caminho do servidor / Para sabermos para onde estão sendo enviadas nossas alterações ou de onde estamos baixando as coisas.
`git clone` // clonar um projeto / repositório / Para baixar um repositório do GitHub, Bitbucket, GitLab ou qualquer que seja o servidor do nosso projeto, devemos rodar o comando git clone com o link do repositório.

`git pull` // puxa do repositório remoto / Baixar as últimas alterações do servidor
Quando algo estiver diferente no nosso repositório remoto (no servidor), podemos baixar para a nossa máquina com o comando pull.

`git remote set-url origin + link` // Adicionando o caminho do servidor,
Caso tenhamos criado o repositório localmente antes de criar no servidor, podemos adicionar o caminho com o comando set-url.
`git remote set-url origin + link` // Para alterar o servidor onde hospedamos nosso repositório, usamos o mesmo comando set-url.

`git remote add origin + repositório do github` // Adicionar repositório do "github"
`git push -u origin master` // envia alterações locais pela primeira vez
`git push` // envia alterações locais para o repositório remoto

`git config --list` // Para verificar as configurações locais
`git config --global user.name` // Para encontrar o nome de usuário
`git config --global user.email` // Para encontrar o email
`git config --global user.name "nome do usuário"` // Alterar o nome de usuário
`git config --global user.email "email do usuário"` // Alterar o email
`git config --global core.editor vim` // Alterando o editor de textos usados no commit e diffs



Fonte: https://woliveiras.com.br/posts/comandos-mais-utilizados-no-git/#Verificandoasconfiguraeslocais