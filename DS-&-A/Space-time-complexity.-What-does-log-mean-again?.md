You might be wondering if I accidentally added some physics pages here - don't worry, we're not going to be covering special relativity anytime soon (quantum computing allowing). For us, space refers to memory, and time, well, also to time. 

When writing our code, we want to consider two things when implementing an algorithm for our problem ->

	How many operations are we executing?
	How much memory are we using to solve the issue?

This sounds great, but practically, it's difficult to exactly test the impact our algorithm is having - there are a lot of factors outside our control, like the speed of the machine it's running on, the OS, the particular processor, the language and if it's interpreted or complied or both, or it's *Java*. 

## Running Time 


![[../imgs/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio+17.png]]


Some helpful maths ideas to know about - don't worry! 😰 This is it. Plus, it's more so you can understand what it means when we say an algorithm is O(log<sub>n</sub>) - we won't actually be doing any maths ourselves. 

- **Exponent:** A number that identifies how many times that base number or expression must be multiplied by itself, its shown as a superscript (tiny number to the upper right of some other “base” number or mathematical expression). **An exponent is a way to show repeated multiplication of a number. It's like a shortcut.** =>  `2 x 2 x 2 = 8` is the same as 2<sup>3</sup> = 8
- Power - 2<sup>3</sup> is a power, which are made of two parts - two being the base and 3 being the exponent. 
- **Logarithms**: are the inverse of exponents and help us find the exponent required to produce a specific value. The logarithm of a number with a given base represents the power to which the base must be raised to obtain that number. For example, log₂(8) = 3, which means 2<sup>3</sup> = 8.
- When we calculate log₂(16), we are asking the question: "To what power must 2 be raised to equal 16?" The answer is 4, as 2 raised to the power of 4 (2^4) equals 16.
- Orders of Magnitude: Orders of magnitude describe the relative size of numbers. For example, 10^3 (1,000) is three orders of magnitude larger than 10^0 (1)

Let's break it down a bit more with an example: 

