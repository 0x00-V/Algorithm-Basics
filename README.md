## Algorithms (Basics)



### Big O notation
- O(n^2) - Quadratic
- O(n log n) - n log n
- O(n) - ==Linear time==
- O(log n) - Logarithmic
- O(1) - ==Constant time==

**==Big O - Upper bound (Worst case)==**
**==Ω (Omega)- Lower bound  (Best case)==**
- Ω(n^2) 
- Ω(n log n) 
- Ω(n) 
- Ω(log n) 
- Ω(1) 

**==θ (Theta) (Best and worst case || Same)==**
- θ(n^2) 
- θ(n log n) 
- θ(n) 
- θ(log n) 
- θ(1) 

***

### Linear Search
Search in a straight line 
- No skipping,
- Just do in a linear way
- **Iterate across array left to right** 
```pseudocode
Repeat, starting at first element:
	if first element == target, stop.
	Otherwise, move to next element
```

**Worst case:** We have to look through entire element **==O(n)==**

**Best-case:** Might find instantly **==Ω(1) ==**
***
### Binary Search 
- Divide and conquer
- Reduce search area by half each time
	- **==array must be sorted first==**
```pseudocode
Repeat until array is size 0:
	- Calculate middle point of current (sub)array
	- If target is middle, stop
	- Otherwise, if target less than middle, repeat. Changing endpoint to be to left of middle
	- Otherwise, if target is greater than middle, repeat, changing starting point to be right of middle
```

Worst Case: Divide list of n elements repeatedly to find target element, it will be found at the end of the last division or doesn't exist at all **==O(log n)==**

**Best case:** Element is at midpoint of full array **==Ω(1)==** 


***


## Bubble Sort
- move higher valued elements towards the right and lower towards left
```pseudocode
- Set swap counter to a non-zero value
- Repeat until swap counter is 0:
	- Reset swap counter to 0
	- Look at each adjacent pair
		- If two adjacent elements are not in order, swap them and add one to swap counter
```

**Worst case**: Array is in reverse order, we have to "bubble" each of the n elements all the way across the array, since we can only fully bubble one element per pass, do this n times **==O(n^2)==**

**Best case:** Array is already perfectly sorted, no swaps in first place (**==Ω(n)==**)

***

## Selection sort
- Find ==smallest== unsorted element, ==add it to the end of list==
```pseudocode
- Repeat until no unsorted elements remain:
	- Search unsorted part to find smallest value
	- Swap smallest found val with first element of unsorted part
```

**Worst case:** Iterate over each of the n elements of the array and repeat this process n times. One element gets sorted each pass **==O(n^2)==**

**Best case:** Same as worst case. **==Ω(n^2)==**


***

## Recursion
- Calls itself as part of its execution
- Requires: **Base case** and **recursive case**
***


## Merge sort
- Sort smaller arrays, and merge them in sorted order
- Merge leverages recursion

```pseudocode
- sort left half of array
- sort right half of array
- merge two halves
```

**Worst case:** Split n element up and recombine them, doubling sorted arrays as we build them up **==O(n log n)==**

**Best case:** Array is already sorted. But a split must happen and recombine with this algorithm **==Ω(n log n)==**



