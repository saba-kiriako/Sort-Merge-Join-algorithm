# Sort-Merge-Join Algorithm
 Single-threaded and multi-threaded implementations 


This join algorithm is actually a two-step process. The first step is to sort both inputs in
the same order. The second step is the Merge Join step.It is widely used in Database Management Systems, especially when the inputs are
already sorted because of an index or because of another sort requirement in the same
query.

## Sorting phase

 ![alt text](https://github.com/saba-kiriako/Sort-Merge-Join-algorithm/blob/Images/Sort.png?raw=true)
 
## Merge phase

### Algorithm :
  1. We associate each relation with a pointer starting at the first element.
  2. Move the pointers towards the next element as soon the algorithm proceeds, this
depends on whether the right value is bigger or smaller than the left value.
  4. Whenever we find a matching tuple, we will mark this tuple with a marker pointer,
concatenate the two tuples and place them in the output relation.
  4. Move the right pointer to the next element to see if we have another matching
tuple.
  5. If there is no further matching tuple we reset the left pointer to the marker, iterate
the left pointer by one and repeat step 2-5.
  
 
 ![alt text](https://github.com/saba-kiriako/Sort-Merge-Join-algorithm/blob/Images/Merge.png?raw=true)
