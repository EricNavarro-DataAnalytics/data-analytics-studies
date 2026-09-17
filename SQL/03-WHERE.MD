# WHERE

O comando `WHERE` é utilizado para **filtrar registros** de acordo com uma condição.

> **Exemplo:** *mostrar clientes que gastaram mais de R$ 500.*

---

## Sintaxe

```sql
SELECT coluna
FROM tabela
WHERE condição;
```

## Exemplos

<details>
<summary><b>Filtrando por número</b></summary>

```sql
SELECT
    *
FROM doces
WHERE preco > 10;
```

</details>

<br>

<details>
<summary><b>Filtrando por texto</b></summary>

```sql
SELECT
    *
FROM doces
WHERE marca = 'Nestlé';
```

</details>