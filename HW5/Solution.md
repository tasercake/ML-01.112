# ML Homework 5

## Q1

If no other nodes' values are known, **X2** and **X6** are independent.

If the values of **X7** and **X11** are known, **X2** nd **X6** are no longer independent because there exists an open-gate path from **X2** to **X6**: `[X2, X3, X4, X5, X8, X9, X10, X11, X10, X9, X6]`.



## Q2

If all nodes can take take values from `{1, 2}`, then the number of free parameters for the network is **26**:

| Node | Free Parameters |
| ---- | --------------- |
| X1   | 1               |
| X2   | 1 * 2           |
| X3   | 1 * 2           |
| X4   | 1 * 2           |
| X5   | 1 * 2           |
| X6   | 1               |
| X7   | 1 * 2           |
| X8   | 1 * 2           |
| X9   | 1 * 2 * 2 * 2   |
| X10  | 1 * 2           |
| X11  | 1 * 2           |
If nodes **X3** and **X9** can take the values `{1, 2, 3}` and the rest can take the values `{1, 2, 3, 4, 5}`, then the number of free parameters is **392**

| Node | Free Parameters     |
| ---- | ------------------- |
| X1   | 4                   |
| X2   | 4 * 5 = 20          |
| X3   | 2 * 5 = 10          |
| X4   | 4 * 3 = 12          |
| X5   | 4 * 5 = 20          |
| X6   | 4                   |
| X7   | 4 * 5 = 20          |
| X8   | 4 * 5 = 20          |
| X9   | 2 * 5 * 5 * 5 = 250 |
| X10  | 4 * 3 = 12          |
| X11  | 4 * 5 = 20          |



## Q3

### 3a

P(X1=1) = 0.5

P(X3=1) = P(X1=1) * P(X2=1 | X1=1) * P(X3=1 | X2=1)

P(X3=1 | X4=1) = P(X3=1) * P(X4=1 | X3=1)

..................

### 3b

The probability table shows that the pairs (X3, X2) and (X10, X9) are independent.

Therefore:

```
P(X5=2 | X3=2, X11=2, X1=2)

	= (P(X5=2) * P(X3=2 | X5=2) * P(X11=2 | X5=2) * P(X1=2 | X5=2)) / (P(X1=2) * P(X3=2) * P(X11=2))

	= (P(X5=2) * P(X3=2 | X5=2)) / P(X3=2)
	= (0.5 * 0.5) + (0.4 * 0.4)
	= 0.45

```

