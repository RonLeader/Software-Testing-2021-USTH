**Use the following program fragment for questions a-e below.**

![image](https://raw.githubusercontent.com/RonLeader/formdangnhap/master/Exercise-7.4.3.md.png)

**Use the following test inputs:** <br>
**• t1 = f1 (0, 0)** <br>
**• t2 = f1 (1, 1)** <br>
**• t3 = f1 (0, 1)** <br>
**• t4 = f1 (3, 2)** <br>
**• t5 = f1 (3, 4)** <br>

**(a) Draw the call graph for this program fragment.**
**(b) Give the path in the graph followed by each test.** 
**(c) Find a minimal test set that achieves Node Coverage.** 
**(d) Find a minimal test set that achieves Edge Coverage.** 
**(e) Give the prime paths in the graph. Which prime path is not covered by any of the tests above?**

a,

![image]https://github.com/RonLeader/formdangnhap/blob/master/Exercise-7.4.3.jpg)

b,
```
t1: [f1, f3, f5, f6] 
t2: [f1, f3, f4, f6] 
t3: [f1, f2] 
t4: [f1, f3, f4, f6] 
t5: [f1, f2, f3, f4, f6]
```

c,
```
{t1; t2; t3}, {t1; t3; t4}, or {t1; t5}
```
d,
```
{t1; t5}
```
e,

4 prime paths:
```
[f1, f2, f3, f4, f6], [f1, f2, f3, f5, f6], [f1,
f3, f4, f6], [f1, f3, f5, f6] 

The [f1, f2, f3, f5, f6] is not covered by any of the tests
above
```
