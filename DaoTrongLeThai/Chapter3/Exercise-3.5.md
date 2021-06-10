**The following JUnit test method for the sort() method has a non-syntactic flaw. Find the
flaw and describe it in terms of the RIPR model. Be as precise, specific, and concise as you
can. For full credit, you must use the terminology introduced in the book.**

```Java
@Test
public void testSort()
{

	names.add("Laura");
	names.add("Han");
	names.add("Alex");
	names.add("Ashley");
	names.sort();
	asserTrue("Sort method", names.getFirst().equals("Alex"));
}
```

This test only examines if the first element is correctly sorted. As for the other 4 elements, the test has no way of finding out if they are in the correct order.

RIPR model:

Reachability: If there is a fault with the first element then it is reached. For the other elements, it isn't reached.

Infection: Yes. The incorrect state can totally happen.

Propagation: No. The whole list can be sorted incorrectly but the first element can still be "Alex". The test condition could still be satisfied and return correct while the infected state is still not dectected.

Revealability: No. The test assertion can't reveal the fault.


