# Dynamic Programming

Dynamic programming is a method for solving complex problems by breaking them down into simpler subproblems. It is applicable when the subproblems are overlapping, meaning that the same subproblems are solved multiple times.

## Key Concepts

1. **Optimal Substructure**: A problem exhibits optimal substructure if an optimal solution to the problem contains optimal solutions to its subproblems.

2. **Overlapping Subproblems**: A problem has overlapping subproblems if it can be broken down into subproblems which are reused several times.

## Example: Fibonacci Sequence

One of the classic examples of dynamic programming is the Fibonacci sequence. The naive recursive solution has an exponential time complexity, while the dynamic programming approach can reduce it to linear time.

### Recursive Solution

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)
```

### Dynamic Programming Solution

```python
def fibonacci(n):
    fib = [0] * (n + 1)
    fib[1] = 1
    for i in range(2, n + 1):
        fib[i] = fib[i - 1] + fib[i - 2]
    return fib[n]
```

## Applications

Dynamic programming is widely used in various fields, including:

- **Operations Research**: For optimization problems.
- **Computer Science**: In algorithms like shortest path, knapsack problem, etc.
- **Economics**: For decision-making processes.

## Conclusion

Dynamic programming is a powerful technique that can significantly reduce the time complexity of algorithms by storing the results of subproblems and reusing them. Understanding its principles is essential for tackling a wide range of computational problems.