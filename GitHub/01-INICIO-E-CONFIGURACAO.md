# Início e Configuração

Comandos utilizados para **configurar o Git e iniciar ou obter um repositório**.

---

## `git config`

Utilizado para configurar informações do usuário que serão associadas aos commits.

### Quando usar?

Normalmente é configurado após instalar o Git em um computador pela primeira vez.

### Exemplos

<details>
<summary><b>Configurando o nome</b></summary>

```bash
git config --global user.name "Seu Nome"
```

</details>

<br>

<details>
<summary><b>Configurando o e-mail</b></summary>

```bash
git config --global user.email "seu@email.com"
```

</details>

> `--global` aplica a configuração para todos os repositórios do usuário naquele computador.

---

## `git init`

Transforma uma pasta comum em um **repositório Git**.

### Quando usar?

Quando um projeto está sendo iniciado localmente e ainda não possui controle de versão com Git.

### Exemplo

Dentro da pasta do projeto:

```bash
git init
```

O Git cria uma pasta oculta chamada `.git`, responsável por armazenar informações e o histórico do repositório.

---

## `git clone`

Cria uma cópia local de um **repositório já existente**.

### Quando usar?

Quando o projeto já está no GitHub e você deseja trabalhar nele no computador.

### Sintaxe

```bash
git clone URL_DO_REPOSITORIO
```

### Exemplo

```bash
git clone https://github.com/usuario/repositorio.git
```

> Ao utilizar `git clone`, normalmente não é necessário executar `git init` nem `git remote add origin`.

---

## `git remote add origin`

Conecta um repositório Git local a um **repositório remoto**, como um repositório hospedado no GitHub.

### Quando usar?

Quando o projeto foi iniciado localmente com `git init` e depois foi criado um repositório correspondente no GitHub.

### Sintaxe

```bash
git remote add origin URL_DO_REPOSITORIO
```

### Exemplo

```bash
git remote add origin https://github.com/usuario/repositorio.git
```

`origin` é o nome utilizado por convenção para representar o repositório remoto principal.