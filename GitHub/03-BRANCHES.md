# Branches

Comandos utilizados para **criar, acessar, unir e excluir branches**.

Uma branch permite desenvolver alterações separadamente sem modificar diretamente a branch principal.

---

## `git branch`

Permite visualizar as branches existentes ou criar uma nova branch.

### Visualizando branches

```bash
git branch
```

### Criando uma branch

```bash
git branch nome-da-branch
```

### Exemplo

```bash
git branch login
```

Esse comando cria a branch `login`, mas **não muda automaticamente para ela**.

---

## `git switch`

Muda para outra branch existente.

### Quando usar?

Quando deseja começar a trabalhar em outra branch.

### Sintaxe

```bash
git switch nome-da-branch
```

### Exemplo

```bash
git switch login
```

> O comando `git checkout` também pode trocar de branch, mas `git switch` possui uma função mais específica e uma sintaxe mais clara para esse objetivo.

---

## `git switch -c`

Cria uma nova branch e **já muda para ela**.

### Sintaxe

```bash
git switch -c nome-da-branch
```

### Exemplo

```bash
git switch -c login
```

Equivale aproximadamente a executar:

```bash
git branch login
git switch login
```

---

## `git merge`

Une as alterações de outra branch à **branch atual**.

### Quando usar?

Depois de finalizar uma funcionalidade ou alteração desenvolvida em uma branch separada.

### Exemplo

Supondo que o trabalho foi realizado na branch `login`:

```bash
git switch main
git merge login
```

Nesse caso, as alterações da branch `login` serão integradas à `main`.

> Antes de executar `git merge`, verifique em qual branch você está com `git status` ou `git branch`.

---

## `git branch -d`

Exclui uma branch local que já foi integrada.

### Sintaxe

```bash
git branch -d nome-da-branch
```

### Exemplo

```bash
git branch -d login
```

O `-d` evita a exclusão caso existam alterações da branch que ainda não tenham sido integradas.

Para forçar a exclusão:

```bash
git branch -D nome-da-branch
```

> Utilize `-D` com cuidado, pois ele força a exclusão da branch.