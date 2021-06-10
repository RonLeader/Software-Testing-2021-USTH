**Answer questions a{d for the graph defined by the following sets:**

**• N = {1; 2; 3}** <br>
**• N0 = {1}** <br>
**• Nf = {3}** <br>
**• E = {(1; 2); (1; 3); (2; 1); (2; 3); (3; 1)}** <br>
Also consider the following (candidate) paths:**<br>
**• p1 = [1; 2; 3; 1]** <br>
**• p2 = [1; 3; 1; 2; 3]** <br>
**• p3 = [1; 2; 3; 1; 2; 1; 3]** <br>
**• p4 = [2; 3; 1; 3]** <br>
**• p5 = [1; 2; 3; 2; 3]** <br>

**(a) Which of the listed paths are test paths? For any path that is not a test path, explain
why not.** <br>
**(b) List the eight test requirements for Edge-Pair Coverage (only the length two subpaths).**<br>
**(c) Does the set of test paths from part (a) above satisfy Edge-Pair Coverage? If not, state
what is missing.**<br>
**(d) Consider the prime path [3; 1; 3] and path p3. Does p3 tour the prime path directly?
With a sidetrip?**

a, 
```
p2 and p3 are test paths. p1 does not terminate at a final node. p4 does not
start at an initial node. p5 contains an edge that doesn't exist in the graph (3; 2).
```

b,

The edge pairs are:
```
{ [1; 2; 1]; [1; 2; 3]; }
{ [1; 3; 1]; [2; 1; 2]; }
{ [2; 1; 3]; [2; 3; 1]; }
{ [3; 1; 2]; [3; 1; 3]  }
```
c,

No. Neither p2 nor p3 tours either of the following edge-pairs:
```
{ [2; 1; 2]; [3; 1; 3] }
```

d,
```
p3 doesn't directly tour the prime path. On the other hand, p3 does tour the prime path
with the sidetrip [1; 2; 1]



