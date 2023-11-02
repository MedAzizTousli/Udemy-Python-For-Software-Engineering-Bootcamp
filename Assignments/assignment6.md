## Question 1
a.
```sql
SELECT * FROM ebayAuctions LIMIT 10;
SELECT * FROM ebayBids LIMIT 10;
SELECT * FROM sqlite_master LIMIT 10;
```
b.
```sql
SELECT bidtime, bid, bidder FROM ebayBids;
```
## Question 2

```sql
INSERT INTO userData VALUES (1, 5, 3, 'Login', 1234534.99);
INSERT INTO userData VALUES (4, 5, 6, 'Login', 1234553.99);
```