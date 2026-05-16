# String Builder Methods
- 
----

1.) `.setLength(newLength)` & `.trimToSize()` </br> </br>

- `.setLength(newLength)` : </br> </br>
  1.1) Set OG Length To New Length, by Deleting Characters (from Memory) if NEW Length Is Smaller than OG and Adds NULL characters (/u0000) if NEW is bigger than OG. </br> </br>
  1.2) Space (capacity) of SB will not delete from memory, just length of SB will decrease. </br> </br>
  1.3) 

- `.trimToSize()` : </br> </br>
  1.1) It Shrinks the internal storage capacity of the StringBuilder to match its current length exactly (basically deletes memory and length=capacity where capacity become equals to length). It is used exclusively to free up wasted RAM. </br> </br>
  1.2) Core Concept: Length vs. Capacity </br> </br>
       To understand trimming, you must look at how StringBuilder manages memory under the hood </br>
          - `Length`: The number of characters currently visible in your text. </br> 
          - `Capacity`: The actual size of the character array (char[]) reserved in computer memory. </br> </br>
       When you append and delete text, the Capacity often stays much larger than the Length. .trimToSize() forces them to become equal. </br> </br>

  1.3) A common point of confusion is mixing up StringBuilder.trimToSize() with String.trim(). It does not delete whitespace characters (like spaces or tabs) from your text.
