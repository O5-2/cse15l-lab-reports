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

[todo: image]
