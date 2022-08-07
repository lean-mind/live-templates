## SQL

Tip: Use `WHERE 1 = 1` to did more easy comment the different filters, for example:

```sql
SELECT *
FROM ws_log
WHERE 1=1
    AND web_service = 'imprimir_factura'
--     AND fecha_fin =< '2022-08-07'
    AND resultado LIKE '%20220780%'
;
```

### SELECTS

- **selc_dist** (select the counts by groups)

```sql
SELECT DISTINCT web_service, count(web_service)
FROM ws_log
GROUP BY web_service;
```

- **selc_having** (select the field having more than "n" counts)

```sql
SELECT estado, count(estado)
FROM ws_log 
GROUP BY estado
HAVING count(estado) > 3
```
