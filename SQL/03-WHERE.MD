# WHERE
O comando `WHERE` é utilizado para **filtrar registros** de acordo com uma condição.
> exemplo: mostrar clientes que gastaram mais de 500 reais.
## Sintaxe
<details>
<summary><b>Filtrando por número</b></summary>

```sql
SELECT 
    *
FROM doces

where preco > 10;
```

</details>

<details>
<summary><b>Filtrando por texto</b></summary>

```sql
SELECT 
    *
FROM doces

where marca = 'Nestlé';
```

</details>
