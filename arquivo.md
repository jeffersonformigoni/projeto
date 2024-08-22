Comandos Git - Cheat Sheet

O que é o Git?
A palavra Git vem de uma gíria usada por ingleses que remete à “cabeça dura”.

Imagina que você está trabalhando em um projeto com várias pessoas, onde todos estão mexendo nos mesmos arquivos ao mesmo tempo. Já deu pra entender a confusão que seria se todo mundo fizesse alterações aleatórias e não houvesse um jeito fácil de acompanhar isso, né?

Parece até um pesadelo... Mas não se preocupe: é aí que o Git entra em ação!

O Git é uma ferramenta de controle de versões que permite que várias pessoas trabalhem em um mesmo projeto ao mesmo tempo, integrando suas alterações de forma segura e organizada. Com o Git, é possível:

Acompanhar as modificações feitas em um arquivo ao longo do tempo.
Visualizar o histórico completo de alterações.
Identificar quem fez cada modificação.
Reverter para versões anteriores, caso algo não saia de acordo com o planejado.
É como uma espécie de superpoder para os desenvolvedores!

Criando ou clonando um repositório
Exibe o estado atual do repositório, mostrando os arquivos modificados, adicionados ou excluídos:



git status
Clona um repositório remoto para um diretório local:



git clone [url]
Exemplo:
git clone git@github.com:rocketseat-education/nlw12-spacetime-explorer.git

Cria um repositório Git em um diretório:



git init
Configurações gerais
Lista todo o conteúdo do arquivo de configurações:



git config --list
Configura o e-mail do usuário para o Git em um nível global:



git config --global user.email "e-mail"
Exemplo:
git config --global user.email ”oi@rocketseat.com.br”

Configura o nome do usuário para o Git em um nível global:



git config --global user.name "nome"
Exemplo:
git config --global user.name ”Rocketseat”

Trabalhando com commits
Desfaz (reseta) o último commit:



git reset --soft HEAD~1
Modifica o commit mais recente:



git commit --amend -m "Nova mensagem do commit"
Cria um novo commit contendo as alterações feitas:



git commit -m "Mensagem do commit"
Adicionando alterações para o próximo commit
Adiciona todos os arquivos modificados na área de preparação (stage):



git add .
Adiciona um diretório específico na área de preparação (stage):



git add [meu_diretorio]
Exemplo:
git add nlw-spacetime

Adiciona um arquivo específico na área de preparação (stage):



git add [meu_arquivo]
Exemplo:
git add index.html

Trabalhando com branches
Alterna para a branch especificada:



git checkout [nome-da-branch]
Exemplo:
git checkout main

Cria uma nova branch com o nome indicado:



git branch [nome-da-branch]
Exemplo:
git branch feature/user-section

Exibe a lista das branches existentes no repositório:



git branch
Combina e incorpora todas as alterações da branch especificada na branch atual:



git merge [nome-da-branch]
Exemplo:
git merge main

Atualizando e enviando alterações para o repositório remoto
Atualiza o seu repositório local com as alterações do repositório remoto:



git pull
Envia as alterações do seu repositório local para um repositório remoto:



git push
Trabalhando com stash
O stash permite que você armazene temporariamente as alterações que ainda não foram commitadas, proporcionando flexibilidade para realizar outras tarefas, como alternar entre branches ou atualizar o seu repositório.

Cria um stash e armazena todas as alterações que ainda não foram commitadas em uma área temporária:



git stash
Reaplica todas as alterações do stash mais recente no seu projeto:



git stash apply
Trabalhando com log
Exibe todo o histórico de commits do repositório:



git log
Exibe o histórico de commits de forma resumida:



git log --oneline
Exibe uma quantidade pré-definida de logs:



git log -n quantidade_log
Exemplo:
git log -n 3

Subindo um repositório para o GitHub
Agora que você já entendeu um pouco mais sobre os comandos Git, segue um passo a passo para você subir o seu código no GitHub:

Inicia o repositório Git:



git init
Adiciona todos os arquivos ao stage:



git add .
Cria o commit inicial:



git commit -m "Meu primeiro commit"
Cria a branch main:



git branch -M main
Adiciona o repositório remoto:



git remote add origin [url_do_seu_repositório]
Envia o código para o GitHub:



git push -u origin main
Ignorando arquivos com o .gitignore
Alguns arquivos precisam ser excluídos do controle de versão, por serem irrelevantes, temporários, ou por conterem informações sensíveis. Para isso, basta criar no diretório raiz do projeto, um arquivo chamado .gitignore e listar tudo o que você não quer que faça parte do controle de versão.

A pasta node_modules precisa estar aqui!
Subindo diretórios vazios com o .gitkeep
O Git normalmente ignora diretórios vazios, pois entende que não há nada para rastrear dentro deles. Para que o Git reconheça e inclua esses diretórios no controle de versão, é só adicionar um arquivo chamado .gitkeep dentro do diretório vazio.