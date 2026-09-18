# 📝 Lista 01 - SELECT, LIMIT e WHERE

Exercícios para praticar os comandos `SELECT`, `FROM`, `LIMIT` e `WHERE`.

---

<details>
<summary><b>🟢 Nível Fácil</b></summary>

<br>

### 1. Primeiros clientes

Mostre as **5 primeiras linhas** da tabela `tb_customers`, exibindo todas as colunas.

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    *
FROM tb_customers
LIMIT 5;
```

</details>

---

### 2. Primeiros produtos

Mostre os **10 primeiros produtos**, exibindo:

- `product_id`
- `product_category_name`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    product_id,
    product_category_name
FROM tb_products
LIMIT 10;
```

</details>

---

### 3. Clientes de São Paulo

Mostre os **10 primeiros clientes do estado de São Paulo (SP)**, exibindo:

- `customer_id`
- `customer_city`
- `customer_state`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    customer_id,
    customer_city,
    customer_state
FROM tb_customers
WHERE customer_state = 'SP'
LIMIT 10;
```

</details>

---

### 4. Pedidos entregues

Mostre os **8 primeiros pedidos que foram entregues (`delivered`)**, exibindo:

- `order_id`
- `order_status`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    order_status
FROM tb_orders
WHERE order_status = 'delivered'
LIMIT 8;
```

</details>

---

### 5. Pagamentos com cartão de crédito

Mostre os **10 primeiros pagamentos realizados com cartão de crédito (`credit_card`)**, exibindo:

- `order_id`
- `payment_type`
- `payment_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    payment_type,
    payment_value
FROM tb_order_payments
WHERE payment_type = 'credit_card'
LIMIT 10;
```

</details>

---

### 6. Avaliações com nota 5

Mostre as **10 primeiras avaliações que receberam nota 5**, exibindo:

- `review_id`
- `order_id`
- `review_score`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    review_id,
    order_id,
    review_score
FROM tb_order_reviews
WHERE review_score = 5
LIMIT 10;
```

</details>

---

### 7. Vendedores de São Paulo

Mostre os **7 primeiros vendedores do estado de São Paulo (SP)**, exibindo:

- `seller_id`
- `seller_city`
- `seller_state`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    seller_id,
    seller_city,
    seller_state
FROM tb_sellers
WHERE seller_state = 'SP'
LIMIT 7;
```

</details>

---

### 8. Produtos com preço maior que R$ 100

Mostre os **10 primeiros itens de pedidos com preço maior que R$ 100**, exibindo:

- `order_id`
- `product_id`
- `price`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    product_id,
    price
FROM tb_order_items
WHERE price > 100
LIMIT 10;
```

</details>

---

### 9. Produtos com mais de 5000 gramas

Mostre os **10 primeiros produtos que pesam mais de 5000 gramas**, exibindo:

- `product_id`
- `product_category_name`
- `product_weight_g`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    product_id,
    product_category_name,
    product_weight_g
FROM tb_products
WHERE product_weight_g > 5000
LIMIT 10;
```

</details>

---

### 10. Geolocalizações do Rio de Janeiro

Mostre os **5 primeiros registros de geolocalização do estado do Rio de Janeiro (RJ)**, exibindo:

- `geolocation_zip_code_prefix`
- `geolocation_city`
- `geolocation_state`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    geolocation_zip_code_prefix,
    geolocation_city,
    geolocation_state
FROM tb_geolocation
WHERE geolocation_state = 'RJ'
LIMIT 5;
```

</details>

<br>

</details>

---

<details>
<summary><b>🟡 Nível Médio</b></summary>

<br>

Exercícios de nível médio, com uso de múltiplas condições, operadores lógicos e comparações no `WHERE`.

---

### 1. Clientes de Campinas

Mostre os **10 primeiros clientes que moram em Campinas, SP**, exibindo:

- `customer_id`
- `customer_city`
- `customer_state`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    customer_id,
    customer_city,
    customer_state
FROM tb_customers
WHERE customer_city = 'campinas'
    AND customer_state = 'SP'
LIMIT 10;
```

</details>

---

### 2. Itens com preço alto e frete baixo

Mostre os **10 primeiros itens** que possuem:

- preço maior que R$ 100;
- frete menor que R$ 20.

Exiba:

- `order_id`
- `product_id`
- `price`
- `freight_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    product_id,
    price,
    freight_value
FROM tb_order_items
WHERE price > 100
    AND freight_value < 20
LIMIT 10;
```

</details>

---

### 3. Pagamentos parcelados no cartão de crédito

Mostre os **10 primeiros pagamentos com cartão de crédito parcelados em mais de 5 vezes**, exibindo:

- `order_id`
- `payment_type`
- `payment_installments`
- `payment_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    payment_type,
    payment_installments,
    payment_value
FROM tb_order_payments
WHERE payment_type = 'credit_card'
    AND payment_installments > 5
LIMIT 10;
```

</details>

---

### 4. Avaliações com nota baixa

Mostre as **15 primeiras avaliações com nota menor ou igual a 2**, exibindo:

- `review_id`
- `order_id`
- `review_score`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    review_id,
    order_id,
    review_score
FROM tb_order_reviews
WHERE review_score <= 2
LIMIT 15;
```

</details>

---

### 5. Produtos de esporte e lazer com mais de 1000 gramas

Mostre os **10 primeiros produtos da categoria `esporte_lazer` que pesam mais de 1000 gramas**, exibindo:

- `product_id`
- `product_category_name`
- `product_weight_g`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    product_id,
    product_category_name,
    product_weight_g
FROM tb_products
WHERE product_category_name = 'esporte_lazer'
    AND product_weight_g > 1000
LIMIT 10;
```

</details>

---

### 6. Vendedores do Paraná ou Santa Catarina

Mostre os **15 primeiros vendedores que sejam do Paraná (PR) ou Santa Catarina (SC)**, exibindo:

- `seller_id`
- `seller_city`
- `seller_state`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    seller_id,
    seller_city,
    seller_state
FROM tb_sellers
WHERE seller_state = 'PR'
    OR seller_state = 'SC'
LIMIT 15;
```

</details>

---

### 7. Pedidos enviados

Mostre os **10 primeiros pedidos com status `shipped`**, exibindo:

- `order_id`
- `order_status`
- `order_purchase_timestamp`
- `order_estimated_delivery_date`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    order_status,
    order_purchase_timestamp,
    order_estimated_delivery_date
FROM tb_orders
WHERE order_status = 'shipped'
LIMIT 10;
```

</details>

---

### 8. Clientes de Belo Horizonte

Mostre os **10 primeiros clientes que moram em Belo Horizonte, MG**, exibindo:

- `customer_id`
- `customer_city`
- `customer_state`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    customer_id,
    customer_city,
    customer_state
FROM tb_customers
WHERE customer_city = 'belo horizonte'
    AND customer_state = 'MG'
LIMIT 10;
```

</details>

---

### 9. Produtos por altura e largura

Mostre os **10 primeiros produtos que tenham altura maior ou igual a 20 cm e largura menor ou igual a 30 cm**, exibindo:

- `product_id`
- `product_height_cm`
- `product_width_cm`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    product_id,
    product_height_cm,
    product_width_cm
FROM tb_products
WHERE product_height_cm >= 20
    AND product_width_cm <= 30
LIMIT 10;
```

</details>

---

### 10. Pagamentos por boleto acima de R$ 200

Mostre os **10 primeiros pagamentos feitos por boleto com valor maior que R$ 200**, exibindo:

- `order_id`
- `payment_type`
- `payment_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    payment_type,
    payment_value
FROM tb_order_payments
WHERE payment_type = 'boleto'
    AND payment_value > 200
LIMIT 10;
```

</details>

<br>

</details>

<details>
<summary><b>🔴 Nível Difícil</b></summary>

<br>

Continua sendo utilizado somente `SELECT`, `WHERE` e `LIMIT`.

A dificuldade agora está em **interpretar e combinar várias regras ao mesmo tempo**, utilizando operadores lógicos e parênteses.

---

### 1. Pagamentos de alto valor parcelados no cartão

Mostre os **10 primeiros pagamentos** que atendam a todas estas condições:

- pagamento com cartão de crédito;
- valor maior que R$ 500;
- parcelado em 6 vezes ou mais.

Exiba:

- `order_id`
- `payment_type`
- `payment_installments`
- `payment_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    payment_type,
    payment_installments,
    payment_value
FROM tb_order_payments
WHERE payment_type = 'credit_card'
    AND payment_value > 500
    AND payment_installments >= 6
LIMIT 10;
```

</details>

---

### 2. Itens com faixa de preço e limite de frete

Mostre os **10 primeiros itens de pedidos** cujo:

- preço seja maior ou igual a R$ 100;
- preço seja menor ou igual a R$ 300;
- frete seja menor ou igual a R$ 25.

Exiba:

- `order_id`
- `product_id`
- `price`
- `freight_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    product_id,
    price,
    freight_value
FROM tb_order_items
WHERE price >= 100
    AND price <= 300
    AND freight_value <= 25
LIMIT 10;
```

</details>

---

### 3. Produtos de categorias específicas e peso elevado

Mostre os **10 primeiros produtos** que:

- sejam da categoria `informatica_acessorios` ou `moveis_decoracao`;
- e, independentemente da categoria, pesem mais de 2000 gramas.

Exiba:

- `product_id`
- `product_category_name`
- `product_weight_g`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    product_id,
    product_category_name,
    product_weight_g
FROM tb_products
WHERE (
        product_category_name = 'informatica_acessorios'
        OR product_category_name = 'moveis_decoracao'
    )
    AND product_weight_g > 2000
LIMIT 10;
```

</details>

---

### 4. Clientes de Campinas ou São Paulo

Mostre os **15 primeiros clientes do estado de São Paulo (SP)** que morem em:

- Campinas;
- ou São Paulo.

Exiba:

- `customer_id`
- `customer_city`
- `customer_state`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    customer_id,
    customer_city,
    customer_state
FROM tb_customers
WHERE customer_state = 'SP'
    AND (
        customer_city = 'campinas'
        OR customer_city = 'sao paulo'
    )
LIMIT 15;
```

</details>

---

### 5. Avaliações entre notas 3 e 4

Mostre as **10 primeiras avaliações** cuja nota seja:

- diferente de 5;
- e maior ou igual a 3.

Exiba:

- `review_id`
- `order_id`
- `review_score`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    review_id,
    order_id,
    review_score
FROM tb_order_reviews
WHERE review_score != 5
    AND review_score >= 3
LIMIT 10;
```

</details>

---

### 6. Pedidos cancelados ou indisponíveis

Mostre os **15 primeiros pedidos** cujo status seja:

- `canceled`;
- ou `unavailable`.

Exiba:

- `order_id`
- `order_status`
- `order_purchase_timestamp`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    order_status,
    order_purchase_timestamp
FROM tb_orders
WHERE order_status = 'canceled'
    OR order_status = 'unavailable'
LIMIT 15;
```

</details>

---

### 7. Vendedores de SP ou RJ por CEP

Mostre os **10 primeiros vendedores** que:

- estejam em SP ou RJ;
- e possuam `seller_zip_code_prefix` menor que 20000.

Exiba:

- `seller_id`
- `seller_city`
- `seller_state`
- `seller_zip_code_prefix`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    seller_id,
    seller_city,
    seller_state,
    seller_zip_code_prefix
FROM tb_sellers
WHERE (
        seller_state = 'SP'
        OR seller_state = 'RJ'
    )
    AND seller_zip_code_prefix < 20000
LIMIT 10;
```

</details>

---

### 8. Produtos pesados e altos

Mostre os **10 primeiros produtos** que:

- pesem mais de 3000 gramas;
- e tenham altura maior que 30 cm.

Exiba:

- `product_id`
- `product_category_name`
- `product_weight_g`
- `product_height_cm`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    product_id,
    product_category_name,
    product_weight_g,
    product_height_cm
FROM tb_products
WHERE product_weight_g > 3000
    AND product_height_cm > 30
LIMIT 10;
```

</details>

---

### 9. Pagamentos por boleto ou cartão de débito

Mostre os **10 primeiros pagamentos** que:

- tenham sido realizados com `boleto` ou `debit_card`;
- e tenham valor superior a R$ 150.

Exiba:

- `order_id`
- `payment_type`
- `payment_installments`
- `payment_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    payment_type,
    payment_installments,
    payment_value
FROM tb_order_payments
WHERE (
        payment_type = 'boleto'
        OR payment_type = 'debit_card'
    )
    AND payment_value > 150
LIMIT 10;
```

</details>

---

### 10. Itens caros com frete alto

Você quer encontrar itens relativamente caros que também tiveram um frete alto.

Mostre os **10 primeiros itens** em que:

- `price` seja maior que R$ 500;
- `freight_value` seja maior que R$ 30.

Exiba:

- `order_id`
- `product_id`
- `price`
- `freight_value`

<details>
<summary><b>Ver solução</b></summary>

```sql
SELECT
    order_id,
    product_id,
    price,
    freight_value
FROM tb_order_items
WHERE price > 500
    AND freight_value > 30
LIMIT 10;
```

</details>

<br>

</details>
