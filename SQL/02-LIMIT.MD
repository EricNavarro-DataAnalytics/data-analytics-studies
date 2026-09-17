# LIMIT

O comando `LIMIT` é utilizado para **limitar a quantidade de registros exibidos** em uma consulta.

É útil para visualizar uma pequena parte da tabela ou quando não é necessário retornar todos os registros.

> **Exemplo:** *mostrar apenas os 5 primeiros doces cadastrados.*

---

## Sintaxe

```sql
SELECT coluna
FROM tabela
LIMIT quantidade;
```

## Exemplo

<details>
<summary><b>Limitando em 5 resultados</b></summary>

```sql
SELECT
    *
FROM doces
LIMIT 5;
```

</details>