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

## Exercise II

Initialize a "low" value as 0                       O(1)
Initialize a "high" value as the total floors       O(1)

While tested floor is not equal to the target       O(log(n)) -> at worst, runs for half n
    Initialize "middle" as ("high" + "low") // 2    O(1)
    If it breaks, set "high" as "middle"            O(1) -> will only do one of the if/elif ops
    Elif it doesn't break, set "low" as "middle"    

Return the answer once the loop is broken           O(1)

Calcs:
O(1 + 1) + O(log(n) * 1 + 1) + O(1)
### O(log(n)) -> binary search function