# SELECT

O comando `SELECT` é utilizado para **selecionar uma ou mais colunas** de uma tabela.

O comando `FROM` indica **de qual tabela os dados serão selecionados**.

> **Exemplo:** *mostrar o preço, tipo e marca dos doces cadastrados.*

---

## Sintaxe

```sql
SELECT coluna
FROM tabela;
```

## Exemplos

<details>
<summary><b>Selecionando todas as colunas</b></summary>

```sql
SELECT
    *
FROM doces;
```

</details>

<br>

<details>
<summary><b>Selecionando colunas específicas</b></summary>

```sql
SELECT
    preco,
    tipo,
    marca
FROM doces;
```

</details>