# 1. git init
## O que faz?
- transforma uma pasta comum em um repositório.
## Quando usar?
- quando se começa um projeto do zero, o primeiro comando a ser usado.
## Exemplo
- no caminho da pasta \MeuProjeto, usar git init, cria a pasta .git que guarda o histórico do projeto.

# 2. git status
## O que faz?
- mostra o estado atual do repositório.
## Quando usar?
- a todo momento. Com ele é possível visualizar o que mudou, o que ainda não foi salvo, e o que está pronto para commit.
## Exemplo
- ao usar git status, mostra modified: "comandos.md" significa que foi criado/alterado o arquivo, mas ainda não salvou no git.

# 3. git add
## O que faz?
- coloca arquivos na área de preparação ( staging area ).
## Quando usar?
- ao querer incluir uma alteração no próximo commit.
## Exemplo
- adiciona um arquivo: git add  comandos.md ( nome arquivo ).
- adiciona tudo: git add .

# 4. git commit
## O que faz?
- cria um ponto de save no histórico do projeto. salva localmente.
## Quando usar?
- depois de fazer alterações, e usar o git add.
## Exemplo
git commit -m "Adicionado nota de comandos".

# 5. git branch nome-da-branch
## O que faz?
- cria uma nova branch.
## Quando usar?
- ao desenvolver funcionalidades separadas da main e só juntar quando estiver funcionando. para evitar erros na main.
## Exemplo
- programar o login, ao invés de fazer na main e correr riscos de código bugado, cria-se uma nova branch, para implementar a funcionalidade. git branch login.

# 6. git checkout nome-da-branch
## O que faz?
- troca para outra branch.
## Quando usar?
- quando quer usar outra branch existente.
## Exemplo
- apos criar a branch login, a  atual ainda é a main, para trabalhar na branch criada, usa-se git checkout login

# 7. git switch -c nome-da-branch
## O que faz?
- cria uma nova branch e já entra nela.
## Quando usar?
- é o jeito mais moderno e prático do checkout.
## Exemplo
- git switch -c login.
- equivale a: git branch login > git checkout login

# 8. git merge nome-da-branch
## O que faz?
- junta as alterações de uma branch em outra.
## Quando usar?
- depois de terminar todas as funcionalidades em uma branch.
## Exemplo
- ao terminar a funcionalidade da branch login, ao mudar pra main, git switch main, basta utilizar git merge login para trazer tudo da branch login para a main.

# 9. git remote add origin
## O que faz?
- conecta repositório local a um no github ( conecta local com a nuvem ).
## Quando usar?
- antes de dar o push, uma única vez, quando cria o repositório remoto.
## Exemplo
- após criar repositório no github, git remote add origin email-do-projeto.

# 10. git push
## O que faz?
- envia os commits locais para o github. salva na nuvem.
## Quando usar?
- depois de fazer commits. para atualizar a nuvem.
## Exemplo
- após commitar as mudanças na main, basta dar o push, git push main, para salvar no github.
- git push -u origin nome-da-branch ( primeira vez que for dar push em uma branch )