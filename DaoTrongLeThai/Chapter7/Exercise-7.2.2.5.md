**Answer questions a–g for the graph defined by the following sets:**

**• N = {1; 2; 3; 4; 5; 6; 7}<br>
• N0 = {1}<br>
• Nf = {7}<br>
• E = {(1; 2); (1; 7); (2; 3); (2; 4); (3; 2); (4; 5); (4; 6); (5; 6); (6; 1)}<br>
Also consider the following (candidate) test paths:<br>
• p1 = [1; 2; 4; 5; 6; 1; 7]<br>
• p2 = [1; 2; 3; 2; 4; 6; 1; 7]<br>
• p3 = [1; 2; 3; 2; 4; 5; 6; 1; 7]**

**(a) Draw the graph**

**(b) List the test requirements for Edge-Pair Coverage.**

**(c) Does the given set of test paths satisfy Edge-Pair Coverage? If not, state what is
missing**

**(d) Consider the simple path [3, 2, 4, 5, 6] and test path [1, 2, 3, 2, 4, 6, 1, 2, 4, 5, 6,
1, 7]. Does the test path tour the simple path directly? With a sidetrip? If so, write
down the sidetrip.**

**(e) List the test requirements for Node Coverage, Edge Coverage, and Prime Path Coverage
on the graph.**

**(f) List test paths from the given set that achieve Node Coverage but not Edge Coverage
on the graph.**

**(g) List test paths from the given set that achieve Edge Coverage but not Prime Path
Coverage on the graph.**


**a,**

Graph:

![image](https://raw.githubusercontent.com/RonLeader/formdangnhap/master/Exercise-7.2.2.5.jpg)

**b,List the test requirements for Edge-Pair Coverage:**<br>
The Edge-Pair Coverage are: [1, 2, 3], [1, 2, 4], [2, 3, 2], <br>
                            [2, 4, 5], [2, 4, 6], [3, 2, 3], <br>
                            [3, 2, 4], [4, 5, 6], [4, 6, 1], <br>
                            [5, 6, 1], [6, 1, 2], [6, 1, 7]  <br>

**c,Does the given set of test paths satisfy Edge-Pair Coverage?**<br>
No, it doesn't. 
t0 and t1 do not tour edges: [3, 2, 3], [6, 1, 2].

**d,Consider the simple path [3, 2, 4, 5, 6] and test path [1, 2, 3, 2, 4, 6, 1, 2, 4, 5, 6,
1, 7]. Does the test path tour the simple path directly? With a sidetrip? If so, write
down the sidetrip.**<br>

The test path tours with a sidetrip is [4, 6, 1, 2, 4].

**f,List test paths from the given set that achieve Node Coverage but not Edge Coverage on the graph.**<br>

The path that achieve Node Coverage but not Edge Coverage on the graph is [1, 2, 3, 2, 4, 5, 6, 1, 7]

**g,List test paths from the given set that achieve Edge Coverage but not Prime Path Coverage on the graph.**<br>

The path that achieve Edge Coverage but not Prime Path Coverage on the path are: [1, 2, 3, 2, 4, 5, 6, 1, 7] and [1, 2, 4, 6, 1, 7]

**e,List the test requirements for Node Coverage, Edge Coverage, and Prime Path Coverage on the graph.**<br>

Node coverage: TR = {1,2,3,4,5,6,7}
