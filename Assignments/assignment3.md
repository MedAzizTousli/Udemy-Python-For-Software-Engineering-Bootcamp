## Question 1
```python
for i in range(1, 6):
    print("x"*i)
```
## Question 2

```python
for i in range(5):
    ch = []
    ch += " " * (4-i)
    ch += "x" * (2*i+1)
    ch += " " * (4-i)
    print(ch)
```
## Question 3
```python
for i in range(5):
    ch = []
    ch += " " * (4-i)
    ch += "x" * (2*i+1)
    ch += " " * (4-i)
    print(ch)
for i in range(3, -1, -1):
    ch = []
    ch += " " * (4-i)
    ch += "x" * (2*i+1)
    ch += " " * (4-i)
    print(ch)
```