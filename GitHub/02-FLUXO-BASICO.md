# Fluxo Básico

Comandos utilizados para **acompanhar alterações e registrar versões do projeto**.

> **Fluxo comum:** `status` → `diff` → `add` → `commit`

---

## `git status`

Mostra o **estado atual do repositório**.

### Quando usar?

Pode ser utilizado a qualquer momento para verificar quais arquivos foram modificados, quais estão preparados para commit e o estado atual da branch.

### Exemplo

```bash
git status
```

---

## `git diff`

Mostra as alterações realizadas nos arquivos que ainda **não foram adicionadas à staging area**.

### Quando usar?

Antes de executar `git add`, para conferir exatamente o que foi alterado.

### Exemplo

```bash
git diff
```

Para visualizar alterações que já foram adicionadas à staging area:

```bash
git diff --staged
```

---

## `git add`

Adiciona alterações à **staging area**, preparando-as para o próximo commit.

### Quando usar?

Depois de revisar as alterações que deseja incluir no próximo commit.

### Exemplos

<details>
<summary><b>Adicionando um arquivo específico</b></summary>

```bash
git add comandos.md
```

</details>

<br>

<details>
<summary><b>Adicionando todas as alterações</b></summary>

```bash
git add .
```

</details>

---

## `git commit`

Registra as alterações preparadas na **história local do repositório**.

### Quando usar?

Depois de utilizar `git add` para preparar as alterações desejadas.

### Sintaxe

```bash
git commit -m "Mensagem do commit"
```

### Exemplo

```bash
git commit -m "Adiciona notas sobre comandos Git"
```

> Uma boa mensagem de commit deve indicar de forma clara o que foi alterado.

---

## `git log --oneline`

Exibe o histórico de commits de forma **resumida**.

### Quando usar?

Quando quiser consultar versões anteriores e visualizar os commits realizados.

### Exemplo

```bash
git log --oneline
```