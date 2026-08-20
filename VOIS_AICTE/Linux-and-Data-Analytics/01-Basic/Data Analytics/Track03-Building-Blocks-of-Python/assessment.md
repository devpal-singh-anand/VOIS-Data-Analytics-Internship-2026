# VOIS Assessment — Building Blocks of Python

## Questions and Answers

### 1. Which of the following is not used as a loop in Python?

* `for` loop
* `while` loop
* `do-while` loop
* None of the above

**Answer:** `do-while` loop

---

### 2. What signifies the end of a statement block or suite in Python?

* `}`
* `end`
* A line that is indented less than the previous line
* A comment

**Answer:** A line that is indented less than the previous line

---

### 3. `x = 'pqrs'` — Which of the following is the correct output of this program?

```python
x = 'pqrs'
for i in range(len(x)):
    x[i].upper()
print(x)
```

* `PQRS`
* `pqrs`
* `qrs`
* None of these

**Answer:** `pqrs`

**Reason:** `.upper()` returns a new string; it does not modify the original string `x`.

---

### 4. What keyword would you use to add an alternative condition to an `if` statement?

* `else if`
* `elseif`
* `elif`
* None of the above

**Answer:** `elif`

---

### 5. What will be the output of this statement?

```python
i = 0
while i < 3:
    print(i)
    i += 1
else:
```

* `01`
* `012`
* `0120`
* `0123`

**Answer:** `012`

