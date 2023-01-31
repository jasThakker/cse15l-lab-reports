## Part 2 
**The input below induces a failure for a buggy program**

```
 @Test
  public void testReversed() {
    int []input2={1,2,3,4,5};
    assertArrayEquals(new int[]{5,4,3,2,1}, ArrayExamples.reversed(input2));
  }
  ```
  
  
**The next code block of input below for the same sniipet of the buggy program does not induce a failure**

```
@Test
  public void testReversed2() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
  ```
  **As it can be seen one of the 2 tests fails because one input induced a failure and the other didn't**
  
  ![Image](2testonefail.png)
  
