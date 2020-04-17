# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```


```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

To determine where is f floor.Instead of going floor by floor and throwing eggs from each floor everytime to test if it breaks or not, we will do a binary search and go to the middle of the building.
We will throw one egg from there.If the egg breaks, we will then split in the half the lower part of the building.And we will throw an egg from the middle to see if it breaks.
Otherwise, we will discard the lower half of the building , and go up to the other half.
We will repeat the same process and discard one half, start at the middle everytime, until we succesfully target the floor where the eggs won't break.
We will then return that floor number.