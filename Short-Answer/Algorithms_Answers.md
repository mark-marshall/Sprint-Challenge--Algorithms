# Analysis of Algorithms

## Exercise I

```
a)  a = 0                                           O(1)
    while (a < n * n * n):                          O(n^3)
      a = a + n * n                                 O(1)
```

Calcs:
O(1) + O(n^3 * 1)
### O(n^3)

```
b)  sum = 0                                         O(1)   
    for i in range(n):                              O(n)
      i += 1                                        O(1)
      for j in range(i + 1, n):                     O(n)
        j += 1                                      O(1)
        for k in range(j + 1, n):                   O(n)
          k += 1                                    O(1)
          for l in range(k + 1, 10 + k):            O(n) -> k is dep on n 
            l += 1                                  O(1)
            sum += 1                                O(1)
```

Calcs:
O(1) + O(n * 1 * O(n * 1 * O(n * 1 * O(n * 1 + 1))))
### O(n^4)

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:                              O(1)
        return 0                                    O(1)
                                                    O(1) -> op on return line
      return 2 + bunnyEars(bunnies-1)               O(n) -> approach constant for large n, reach log(n) at n=2
```

Calcs:
O(1 + 1 + 1) + O(n)
### O(n)

