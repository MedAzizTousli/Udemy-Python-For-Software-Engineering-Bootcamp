## Question 1
a.
```sql
SELECT eventId,
       eventName
FROM userData
WHERE userId = 3
```
b.
```sql
SELECT eventId,
       eventName
FROM userData
WHERE eventName LIKE '%l%';
```
c.
```sql
SELECT eventId,
       eventName
FROM userData
WHERE eventName = 'Login' OR eventName = 'Logout';
```
## Question 2
a.
```sql
SELECT eventId,
       eventName
FROM userData
WHERE eventName = 'Photo'
ORDER BY date DESC
```
b.
```sql
SELECT eventId,
       eventName,
       date
FROM userData
WHERE eventName = 'Photo' AND date >= 'T2019-01-01 00:03:51.718089'
ORDER BY date DESC
```