2 - Data structures and dynamic arrays. 
Interface (API/ADP (abstract data type)) vs Data structure
Interface - what you want to do. Like a specification - what data can you store - what data can store - what operation are supported and what they can do - think about it as a problem statement
Data structure - representation - how to store data. - algorithms to support data - solution to problem

2 main interfaces: 
	- set
	- sequence

We might want to store 'n' things.

2 main DS approaches:
	- arrays
	- pointer based

Static sequence interface:
	Amount of items doesn't change, but items might. 

A word is a unit of data (16bits). wordRAM = wordSize matches problem size? 

Key: wordRAM - model of computation
	- memory = array of w-bit words. 
	- "array" = contingues chunk of memory. 
	- -> arr[i] is the same as accessing (address(array) + i)
	- array access is constant time 
Solution (narutal): static array
	-O(l) get/set
	-O(n) per build
	Memory allocation model - allocate an array of size 'n' in O(n) time. 
	- space = O(time)

w >- log(n) = each time data is iterated over reduces the size of the data.
When our n's expand too much, we're doing to need more w (wordsize/RAM)

