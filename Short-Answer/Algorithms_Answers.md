Add your answers to the Algorithms exercises here.

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```
### Answer:
```
O(1)
O(n^3)
    O(n^2)

O(n^3) / O(n^2) = O(n)

Runtime is O(n)
```

```
b)  
sum = 0
for i in range(n):
    i += 1
    for j in range(i + 1, n):
    j += 1
    for k in range(j + 1, n):
        k += 1
        for l in range(k + 1, 10 + k):
        l += 1
        sum += 1
```
### Answer:
```
O(1)
O(n)
    O(n) --> here or below
    O(n) --> here or above (this is not actually a nested loop with what's above it)
    O(n)

O(n) * O(n) * O(n) --> O(n^3)

Runtime is O(n^3)
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

### Answer:
```
    O(1)
        O(n)

Runtime is O(n)

This was interesting because I originally thought O(1), but it seems to use recursion so I think O(n).
```

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

###Answer:

```
You could solve this using a binary search. 

You could take the number of stories _n_ and find the midpoint. Drop an egg form there. If it breaks, move down, if it does not, move up. Repeat that process until you find the floor _f_ where the egg stops breaking (or starts breaking). Try until you know the optimum floor.

Runtime of a binary search is O(log n). 
```