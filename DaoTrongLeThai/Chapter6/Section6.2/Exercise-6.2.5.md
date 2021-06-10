**Use the following characteristics and blocks for the questions below.**

!["Image"](https://raw.githubusercontent.com/RonLeader/formdangnhap/master/Exercise%206.2.5.png)

**(a) Give tests to satisfy the Each Choice criterion**

**(b) Give tests to satisfy the Base Choice criterion. Assume base choices are Value 1 = > 0, Value 2 = > 0, and Operation = +.**

**(c) How many tests are needed to satisfy the All Combinations criterion? (Do not list all the tests.)**

**(d) Give tests to satisfy the Pair-Wise Coverage criterion**


a, 

There are 4 tests needed: 
```
(-2, -2, +)
(0, 0, -)
(2, 2, x) 
(2, 2, /)
```

b,

There are eight tests needed:
```
(2, 2, +), (-2, 2, +), (0, 2, +), (2, -2, +)
(2, 2, +), (-2, 2, +), (0, 2, +), (2, -2, +)
```

c,

There are (3 x 3 x 4) = 36 tests.

d,

We have : 7 + 7 + 7 + 4 + 4 + 4 = 33 ( pairs )

Since each test can accommodate 3 pairs, at least 11 tests are needed. The best solution
involves one extra test, for a total of 12 tests:

```
(-2, -2, +), (-2, 0, -), (-2, 2, x)
(2, -2, /),(2, 0, +), (0, 2, -)
(0, -2, x), (0, 0, /), (0, 2, +)
(2, -2, -), (2, 0, x), (-2, 2, /)
```
