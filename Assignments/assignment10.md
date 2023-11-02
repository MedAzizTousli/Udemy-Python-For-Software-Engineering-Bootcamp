## Question 1
a.
```sql
SELECT
    DISTINCT ("BillingCountry"),
    SUM("Total") OVER (PARTITION BY "BillingCountry") as sum
FROM "Invoice"
```
b.
```sql
SELECT
    DISTINCT("TrackId"),
    MIN("InvoiceDate") OVER (PARTITION BY il."TrackId")
FROM "Invoice" i
JOIN "InvoiceLine" il
ON i."InvoiceId" = il."InvoiceId"
```
