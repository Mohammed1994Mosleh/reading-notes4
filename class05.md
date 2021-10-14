# class04 Reading Notes:

## Big O:

 describe the efficiency of an algorithm or function by 2 factor:
 1. Running Time
 2. Memory Space
 ![complexity](https://adrianmejia.com/images/time-complexity-examples.png)

 ####  4 Key Areas:
 1. Input Size
 2. Units of Measurement 
 in order to measure time efficieny then ,using three measurement:
 - The time in milliseconds from the start of a function execution until it ends
 - The number of operations that are executed
 - The number of “Basic Operations” that are executed

 in order to measure space efficieny then ,using three measurement:

 1. space needed to hold the code for the algorithm.
 2. space needed to hold the input data.
 3. space needed for the output data.
 4. space needed to hold working space during the calculation

 #### Orders of Growth:
 as n describes the space efficiency  As the value of n grows, the Order of Growth represents the increase in Running Time or Memory Space. 

1. Constant Complexity it always uses the same amount of time or space whatever input is.

2. Logarithmic Complexity:
 decrease in the rate of complexity growth, the greater our value of n.

3. Linear Complexity:
 he size of our inputs ‘n’ will directly determine the amount of Memory Space used and Running Time length

4. Linearithmic Complexity 
determine complexity in lgn

5. Quadratic Complexity (n^2)

6. Cubic Complexity(n^3)

#### Worst Case, Best Case, Average Case:
- Worst Case for n for example if i searched for number and i iterate over array and isnt exist .
- Best Case: as previous example if i found number from the first iteration.
- verage Case: between worst case and best case.


## linked lists:
![linked lists](https://study.com/cimages/multimages/16/circularly_linked_lists.png)

### Linear data structures:
![Linear vs non-linear](https://techdifferences.com/wp-content/uploads/2018/07/linear-vs-non-linear-data-structure.jpg)

where data elements are arranged sequentially or linearly where the elements are attached to its previous and next adjacent in what is called a linear data structure.

##### linked list dosent need to be contigues in memory on the other hand array need to be contigues .

#### the linked list is Dynamic data structure ,and this is also be reliable.
#### Parts of a linked list:
1. head
2. node consists of
  - data structure
  -next node.
3. null

#### Lists for all shapes and sizes:
- Singly linked lists 
- doubly linked list
-  circular linked list : easy to add something to the end of the list

##### we can add elements and remove elements from a linked list