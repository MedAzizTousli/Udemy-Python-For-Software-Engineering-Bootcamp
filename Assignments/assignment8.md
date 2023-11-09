## Question 1
a.
```sql
SELECT "InvoiceId",
    "InvoiceDate"::TIMESTAMP - '2009-01-01 00:00:00'::TIMESTAMP AS timedif
FROM "Invoice"
```
## Question 2
a.
```sql
SELECT "InvoiceId",
    date_part('YEAR', "InvoiceDate"::TIMESTAMP) AS year,
    date_part('MONTH',"InvoiceDate"::TIMESTAMP) AS month,
    date_part('DAY',"InvoiceDate"::TIMESTAMP) AS day,
    date_part('HOUR',"InvoiceDate"::TIMESTAMP) AS hour,
    date_part('MINUTE',"InvoiceDate"::TIMESTAMP) AS minute,
    date_part('SECOND',"InvoiceDate"::TIMESTAMP) AS second
FROM "Invoice"
```
b.
```sql
SELECT "InvoiceId",
    "InvoiceDate"
FROM "Invoice"
WHERE date_part('DAY',"InvoiceDate"::TIMESTAMP) <=5
```
