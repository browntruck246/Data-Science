## Ch02/02_02

Let's start looking into Numpy arrays. So first we import Numpy as np. And now I'm creating an array of three elements with 1, 2 and 3 run this. And we have an array 1, 2 and for starts. Arrays look very much like lists.    

```
import numpy as np

arr = np.array([1,2,3])

print( arr )
```
[1 2 3]



So we can ask for the length. 

```
import numpy as np

arr = np.array([1,2,3])

len(arr)
```
3


We can get the second element and arrays are 0 based indexing like the rest of Python. 

```
import numpy as np

arr = np.array([1,2,3])

print( arr[1] )
```
2

But if you look closer, for example type of the 1st element, we see that it's not a Python integer but a Numpy int32.

```
import numpy as np

arr = np.array([1,2,3])

print( type ( arr[1] ) )
```
<class 'numpy.int32'>

For you can ask array what is the data type of the array using the dtype attribute. When you create an array, Numpy will determine the default type for the array for the input. However, you can specify explicitly the data type of the array to be created. This here is saying dtype np.int32 and we're going to get an array of int 32 comparing to any 64. This takes half the memory, but you need to make sure that all of your values fits inside a 32 bit integer. 

```
import numpy as np

arr32 = np.array([1,2,3], dtype=np.int32)
arr32.dtype
```
dtype('int32')


You can multiply an array by itself. And what you're going to get is an elementwise multiplication, so 1 * 1 = 1, 2 * 2 = 4 and 3 * 3 = 9. I talked about Numpy and being fast. Let's have a look. 

```
import numpy as np

arr = np.array([1,2,3])
arr * arr
```
array([1, 4, 9])


So I'm creating 2 arrays, each one with 1,000,000 random elements which are floats, and then I'm going to use the time magic to see how much time it takes. To multiply them and that took 6.27 milliseconds.

```
import numpy as np

v1 = np.random.rand(1_000_000)
v2 = np.random.rand(1_000_000)
%time v1 * v2
```
CPU times: user 0 ns, sys: 0 ns, total: 0 ns      
Wall time: 8 ms           
array([0.34457429, 0.35776736, 0.43376311, ..., 0.04245104, 0.11236527,
       0.16326489])         

If you'd like to get the Dot Product of a matrix. Use the @ sign, which is the Python matrix multiplication operator.

```
import numpy as np

arr = np.array([1, 2, 3])

arr @ arr
```
np.int32(14)

## NOTE (calculate the Dot Product)

arr @ arr =
[1,2,3] @ [1,2,3] =
[1, 4, 9 ] =

1 + 4 + 9 = 

14

If we want to sell now, we're going to see 14, which is a dot product of these two arrays, we can move to more dimensions. So here's an array with three rows and three columns, and we can run this one. And now we can see the. That's a lot of code to write for a small sample metrics. Let's use one of the many utilities we have in Numpy to create arrays NA range. It's very much like Python range, but returns an array. So if you do v = a range of 12, you're going to get an array from zero to 12, and now we can use the reshape. To reshape the array. So if you're going to run this one now, we're going to get an array with four rows and three columns. So in a single line we can run matte equal Numpy, a range 12, reshape 4:00 and 3:00, and then get our matrix. We can call the dot shape attribute to know what is the current shape or how many rows, columns, and maybe other dimensions a matrix has. Let's create another matrix by reshaping the original 1 instead of 4 rows and three columns, 3 rows and four columns, and now we're going to change the value in. This reshaped metrics and then take a look at the original 1. And we see that the original matrix is affected as well when you do a reshape, you get a view of the underlying data. It's not a copy. There are many other methods and functions that work with Numpy arrays. For example, you can transfer the metric by calling. The T attribute. You'll pick more as you go, but I think this is enough for understanding the basics. Of Numpy arrays.
