# 🔄 Fluxo Git

Resumo do fluxo utilizado para salvar e enviar alterações para o GitHub.

---

## Alterar arquivos

Faça normalmente as alterações necessárias no projeto.

↓

## Verificar alterações

```bash
git status
```

↓

## Revisar alterações

```bash
git diff
```

↓

## Preparar alterações

```bash
git add .
```

↓

## Criar commit

```bash
git commit -m "Descrição da alteração"
```

↓

## Enviar para o GitHub

```bash
git push
```

---

## Fluxo resumido

```text
Alterar arquivos
      ↓
git status
      ↓
git diff
      ↓
git add .
      ↓
git commit
      ↓
git push
```

---

> Antes de começar a trabalhar novamente, utilize `git pull` quando houver possibilidade de alterações no repositório remoto.