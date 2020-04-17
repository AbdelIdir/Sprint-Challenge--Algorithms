#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) The runtime for a is 0(1), this is a linear operation.
Becaus no matter how big n is, only one operation will be run on the number n each time.


b) The runtime for n is 0(nlogn). The number of operations will increase depending on the size of n in the for loop. The bigger n is , the bigger the loop range will be, and the more operations it will run.


c) The runtime for this recursive function is 0(n).
The function will be called n times before it reaches base case and stops.
The bigger n is, the longest it will run. The smaller n is, the less operations it will run.

## Exercise II


To determine where is f floor.Instead of going floor by floor and throwing eggs from each floor everytime to test if it breaks or not,
 we will do a binary search and go to the middle of the building.
We will throw one egg from there.
If the egg breaks, 
we will then split in the half the lower part of the building.
And we will throw an egg from the middle to see if it breaks.
Otherwise, we will discard the lower half of the building , 
and go up to the other half.
We will repeat the same process and discard one half, start at the middle everytime, until we succesfully target the floor where the eggs won't break.
We will then return that floor number.

The runtime complexity of this operation will be O(log n). With n being the number of floors.
