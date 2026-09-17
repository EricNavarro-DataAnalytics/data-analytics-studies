git switch -c login

FAÇO A FUNCIONALIDADE

git add .
git commit -m "Adiciona sistema de login"

git switch main
git merge login

git branch -d login

git push