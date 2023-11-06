# Lab Report 3
## Bugs and Commands (Week 5)

**Part 1:**

The bug in question is the one in `reverseInPlace` in `ArrayExamples`.

*Failure-inducing input:*

```
@Test 
public void testRIPFail() {
  int[] input1 = { 1, 2 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 2, 1 }, input1);
}
```

*Non-failure-inducing input:*

```
@Test 
public void testRIPSucceed() {
  int[] input1 = { 5 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 5 }, input1);
}
```

*Symptom:*

![Image](CSE15L_Lab3_1a.png)

*The bug:*

```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

*The bug, fixed:*

```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length/2; i += 1) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
```

*Explanation of the fix:*

The bug is that the program overwrote the first half of the array with the second half of the array, effectively discarding the first half of the array. The bug was fixed by changing the program to swap pairs of elements.

**Part 2:**

