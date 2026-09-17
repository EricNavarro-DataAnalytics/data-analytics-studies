# GitHub e Repositório Remoto

Comandos utilizados para **sincronizar o repositório local com um repositório remoto**, como o GitHub.

---

## `git push`

Envia commits do repositório local para o **repositório remoto**.

### Quando usar?

Depois de realizar commits localmente e desejar enviar essas alterações para o GitHub.

### Primeiro push da `main`

```bash
git push -u origin main
```

Depois de configurar o upstream:

```bash
git push
```

### Primeiro push de uma nova branch

```bash
git push -u origin login
```

> A opção `-u` define a branch remota como **upstream** da branch local. Depois disso, comandos como `git push` e `git pull` podem ser utilizados sem informar novamente o remoto e a branch.

---

## `git pull`

Busca alterações do repositório remoto e atualiza a branch local.

### Quando usar?

Antes de começar a trabalhar, principalmente quando o projeto pode ter recebido alterações através de outro computador, colaborador ou diretamente pelo GitHub.

### Exemplo

```bash
git pull
```

Uma forma simples de lembrar:

```text
git push → computador → GitHub
git pull → GitHub → computador
```

---

## Fluxo comum

Depois de realizar alterações:

```bash
git status
git add .
git commit -m "Descrição da alteração"
git push
```

Antes de começar a trabalhar novamente:

```bash
git pull
```