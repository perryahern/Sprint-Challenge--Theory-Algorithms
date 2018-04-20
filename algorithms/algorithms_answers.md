# Exercise 1:
a) O(n) since it will only run a limited number of times.

b) O(log n) since it is dividing n by a number greater than 1 and discarding large chunks of the n set with each iteration.

c) Outer loop is log n, first inner is n, 2nd inner is n, so you have something along the lines of O(n(n log n)) if that's an option.

d) O(n log n) as the outer loop runs log n times or less but the inner loop runs n times.

e) O(n^4) as the outer loop has 3 nested loops. 

f) O(n) since this will run once for every value from n to 0.

g) O(n) since this will run once for every arraySize value from n to 1.

# Exercise 2:

a) I can't think of a way to do this in linear time as all the solutions I'm thinking of involve either a) nested loops, which is non-linear or b) sorting the numbers in ascending order and then returning a[n-1] - a[0], which I'm pretty sure wouldn't be linear as I believe sorting adds too much complexity.

b)  Start on floor 1 and drop an egg. If it breaks, return f = -1 as it's not possible to drop an egg without breaking it.

    Go to floor n and drop an egg. If it doesn't break, return f = n as the top floor is low enough not to break the egg.

    If it does break when dropped from floor n, begin a testing loop that continues until the difference between the lowest tested floor where it broke and the highest floor where it doesn't break is one (they're sequential floors).
      During this testing phase:
      If the egg breaks, go down half the difference between the current floor and the highest tested floor where it didn't break.
      If it doesn't break, go up half the difference between the current floor and lowest tested floor where it did break.
    Once sequential break/non-break floors are found, return f = highest non-breaking floor found.

# Exercise 3:
a) I believe this is O(n) as the number of steps is equal to the number of elements. It doesn't matter whether it is pre-sorted or not, this is going to handle every element and place it in an n-1 length array recursively until they are single element arrays, then reassemble them in order.

b) Again, I believe it's O(n) as a pivot sort takes n recursive steps to break the elements into single-element arrays and then combine them back together in order.
