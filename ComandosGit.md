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
# 5.1 git branch -d nome-da-branch
## O que faz?
- apaga uma branch local depois de terminar seu proposito e fazer o merge.

# 6. git checkout/switch nome-da-branch
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
- conecta repositório local a um repositório Github ( conecta local com a nuvem ).
## Quando usar?
- uma única vez, após criar o repositório no GitHub.
## Exemplo
- após criar repositório no github git init, git remote add origin https://github.com/usuario/repositorio.git

# 10. git push
## O que faz?
- envia os commits locais para o github. salva na nuvem.
## Quando usar?
- depois de fazer commits. para atualizar a nuvem.
## Exemplo
- Primeiro push da main: git push -u origin main
- Depois disso: git push
- Primeiro push de uma nova branch: git push -u origin login

-u liga branch a branch do github.

# 11. git pull
## O que faz?
- baixa do GitHub as alterações mais recentes e atualiza o repositório local.
## Quando usar?
- antes de começar a trabalhar, principalmente se o projeto puder ter alterações feitas em outro computador ou diretamente pelo GitHub.
## Exemplo
- git push = computador > GitHub.
- git pull = GitHub > computador.

# 12. git clone
## O que faz?
- baixa um repositório existente do GitHub para o computador.
## Quando usar?
- quando o projeto já existe no GitHub e você quer começar a trabalhar nele localmente.
## Exemplo
- git clone https://github.com/usuario/repositorio.git
importante: se usou git clone, não precisa usar git init nem git remote add origin.

# 13. git log --oneline
## O que faz?
- mostra o histórico de commits de forma resumida.
## Quando usar?
- quando quiser visualizar os saves anteriores do projeto.
## Exemplo
- git log --oneline

# 13. git diff
## O que faz?
- mostra exatamente o que foi alterado nos arquivos.
## Quando usar?
- antes de dar git add, para conferir suas mudanças.
## Exemplo
- git diff