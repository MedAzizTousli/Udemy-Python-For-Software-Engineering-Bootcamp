## Question 1
a.
```sql
SELECT "CustomerId",
    COUNT(1)
FROM "Invoice"
GROUP BY "CustomerId"
HAVING COUNT(1) != 7
```
b.
```sql
SELECT "CustomerId",
    COUNT(DISTINCT("TrackId"))
FROM "Invoice" i
JOIN "InvoiceLine" il
ON i."InvoiceId" = il."InvoiceId"
GROUP BY "CustomerId"
HAVING COUNT(DISTINCT("TrackId")) != 38
```
c.
```sql
SELECT "CustomerId",
       "TrackId",
    COUNT("TrackId")
FROM "Invoice" i
JOIN "InvoiceLine" il
ON i."InvoiceId" = il."InvoiceId"
GROUP BY "CustomerId", "TrackId"
HAVING COUNT("TrackId") != 1
```
