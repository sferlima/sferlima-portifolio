## Git e GitHub

##### o que é git e github

Git é um sistema de controle de versões amplamente utilizado para gerenciamento de projetos de software. Ele permite rastrear alterações no código-fonte, facilitando a colaboração e o controle do histórico de desenvolvimento.

GitHub, por sua vez, é uma plataforma online para hospedagem de repositórios Git, funcionando também como uma rede social para desenvolvedores. Além de armazenar projetos remotamente, o GitHub oferece recursos para descoberta de projetos de outros usuários, colaboração e divulgação de portfólios como este.

Um elemento fundamental em todo repositório é o arquivo README.md, que serve como apresentação e documentação do projeto, facilitando o entendimento e possíveis contribuições. É possível incrementar o README com selos informativos utilizando o [shields.io](https://shields.io/), como status do projeto, tamanho do repositório, licença, entre outras coisas relevantes.

##### configurações iniciais no git bash

~~~bash 
git config --global user.name "seu_nome"
git config --global user.email "seu_email"
~~~

##### Principais Comandos Git

- git init – Inicializa um novo repositório local.
- git clone url_repositorio – Clona um repositório remoto.
- git add arquivo OU git add . – Adiciona arquivos para o próximo commit.
- git status – Exibe o status dos arquivos no diretório de trabalho.
- git commit -m 'texto do commit' – Registra as alterações feitas.
- git pull – Baixa as alterações do repositório remoto.
- git push – Envia commits para o repositório remoto.

##### Branches

Branches permitem criar diferentes linhas de desenvolvimento sem afetar o código principal.

- Como criar e trocar de branch: 
    1. Criando a branch:
    git branch nome_branch

    2. Trocando para a branch criada:
    git checkout nome_branch ou git switch nome_branch
    
    3. Criando e trocando:
    git switch -c nome_branch ou git checkout -b nome_branch 

- Como mesclar as branchs:
    1. Volte para a branch principal: 
    git checkout master ou git switch master
           
    2. Faça o merge:
    git merge nome_branch

- Deletar uma branch: git branch -d nome_branch

##### Commits
Podemos ter uma visão geral dos commits por meio do grafo de commits com os comandos:
~~~bash
git log
git log --online (versão simplificada dos commits)
git log graph (inclui um desenho da árvore de commits)
~~~

Estes comando disponibilzam um código (hash) que podemos utilizar para retornar a uma versão do projeto:
~~~bash
git checkout hash_versão -> volta para as mudanças deste commit.
git checkout master -> desfaz essa ultima mudança e retorna para o ultimo commit realizado do projeto.
~~~
Para desfazer um commit realizado também utilizamos o hash no comando: git reset --hard seu_hash

É possivel desfazer suas mudanças no projeto antes de realizar um commit utilizando o comando: git diff.

No entanto, se já tiver utilizado o 'git add' não é possível usar ele e sim usar o comando: git heset head.
