# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  1. One algorithm may appear to perform better than another asymptotically,
     but if the worst case data set for the algorithm with a better average case 
     ends up being a very common data set for the problem at hand, then you'll
     want to choose the algorithm that has an asymptotically worse average case,
     but a less likely and/or less detrimental worst case.
  2. Some algorithms (like insertion sort) work better than more complicated
     algorithms (like quicksort) when applied to very small data sets. Terms
     that are asymptotically insignificant on large data sets can be much more
     significant on small data sets.
  3. An algorithm could be asymptotically favorable, but take up so much memory
     that it would be more efficient to implement another algorithm than try and 
     implement in place memory.

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
  1. The tree could be completely unbalanced after the first thousand elements
     and turn into more of a linked list.
  2. The elements that were added could be more complex and need more compares
     to be differentiated from each other.                                  
  3. The storage and CPU on your machine are really bad and can only handle
     3000 elements before algorithm starts getting really slow.


"I certify that I have listed all sources used to complete this exercise,
including the use of any Large Language Models. All of the work is my own, except
where stated otherwise. I am aware that plagiarism carries severe penalties and
that if plagiarism is suspected, charges may be filed against me without prior
notice."

Add your answers to this markdown file.
 