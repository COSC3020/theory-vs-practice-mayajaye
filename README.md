# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  1. Asymptotic analysis only looks at the growth rate of an algorithm based
     on the amount of work a program is doing. Other factors such as cache
     handling and memory allocation can affect the runtime of a program.  
  2. We ignore constant factors when analyzing runtimes, but a constant could 
     have a dominant growth rate for small n. For example, $10(n)$ would 
     dominate $n log(n)$ for small data sets, but Big-O notation would ignore 
     the 10 and have $n log(n)$ be the dominant term since $n log(n)$ will 
     overtake $10(n)$.
  3. Runtimes increase predictably on graphs for runtime analysis, but if any
     of the cases from part 3 occur, the runtime could start fluctuating 
     unpredictably.                                              

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  Since the asymptotic complexity of a binary search algorithm is O(log n), we
  can say that 5 seconds = log(1000). 5 $\not{=}$ log(1000), so we can't just 
  compute log(10000) to find how long a search with 10000 elements would take.
  Instead, we can set it up like this:

  $\frac{T}{5}=\frac{log(10000)}{log(1000)} \equiv \frac{T}{5}=\frac{4}{3}$
  $T=5*\frac{4}{3}=\frac{20}{3}$
  So, a search with 10000 elements should take about 6.67 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  1. As the data set grew, the cache hit rate became extremely low. Most of 
     the data set had cache misses, causing more clock cycles and therefore 
     a higher runtime.
  2. The elements that were added could be more complex and need more compares
     to be differentiated from each other.                                  
  3. Your machine only has 8 MB of RAM, and once that gets fully utilized,
     the computer will have to read and write to and from the hard drive.
     Therefore, the program will slow down a lot while approaching 10000 
     elements.


SOURCES AND PLAG
#### Sources

I looked at this[https://cr.yp.to/bib/1999/lamarca-sorting.pdf] for cache handling affecting runtimes.

"I certify that I have listed all sources used to complete this exercise,
including the use of any Large Language Models. All of the work is my own, except
where stated otherwise. I am aware that plagiarism carries severe penalties and
that if plagiarism is suspected, charges may be filed against me without prior
notice."

Add your answers to this markdown file.
 