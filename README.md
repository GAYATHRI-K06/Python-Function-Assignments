# Python-Function-Assignments
# NAME: GAYATHRI K
# REG NO: 212223230061

# Python Function Assignments

## 1. Calculator Using Function

**Question:**
Write a function `calculate(a, b, operation)` that performs addition, subtraction, multiplication, or division based on the supplied operation.

**Example Input:**

```text
10
5
+
```

**Code:**

```python
def calculate(a, b, operation):
    if operation == "+":
        return a + b

    elif operation == "-":
        return a - b

    elif operation == "*":
        return a * b

    elif operation == "/":
        return a / b

    else:
        return "Invalid operation"


a = int(input())
b = int(input())
operation = input()

print(calculate(a, b, operation))
```

**Output:**

```text
15
```

---

## 2. Sum of Numbers Using `*args`

**Question:**
Write a function `sum_numbers(*args)` that accepts any number of arguments and returns their sum.

**Example Input:**

```text
10 20 30 40
```

**Code:**

```python
def sum_numbers(*args):
    total = 0

    for n in args:
        total += n

    return total


numbers = list(map(int, input().split()))

print(sum_numbers(*numbers))
```

**Output:**

```text
100
```

---

## 3. Employee Information Using `**kwargs`

**Question:**
Write a function `employee(**args)` that accepts employee information such as name, ID, department and salary, then displays the information.

**Code:**

```python
def employee(**args):
    for key, value in args.items():
        print(key, ":", value)


employee(
    name="Gayathri",
    ID=101,
    department="Testing",
    salary=50000
)
```

**Output:**

```text
name : Gayathri
ID : 101
department : Testing
salary : 50000
```

---

## 4. Remove Duplicates While Preserving Order

**Question:**
Write a function `remove_duplicates(lst)` that returns a list containing only unique elements while preserving their original order.

**Example Input:**

```text
1 2 2 3 4 3 5 1
```

**Code:**

```python
def remove_duplicates(lst):
    result = []

    for item in lst:
        if item not in result:
            result.append(item)

    return result


numbers = list(map(int, input().split()))

print(remove_duplicates(numbers))
```

**Output:**

```text
[1, 2, 3, 4, 5]
```

---

## 5. Sort List of Tuples Using Lambda

**Question:**
Using a lambda function, sort a list of tuples based on the second element.

**Example Input:**

```text
[(1, 5), (2, 3), (4, 1)]
```

**Code:**

```python
numbers = [(1, 5), (2, 3), (4, 1)]

result = sorted(numbers, key=lambda x: x[1])

print(result)
```

**Output:**

```text
[(4, 1), (2, 3), (1, 5)]
```
