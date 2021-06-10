**Answer the following questions for the method search() below:

![image](https://raw.githubusercontent.com/RonLeader/formdangnhap/master/6.1.2.png)

**Base your answer on the following characteristic partitioning:**

![image](https://github.com/RonLeader/formdangnhap/blob/master/6.1.2.1.png)

**(a) “Location of element in list” fails the disjointness property. Give
an example that illustrates this.**

**(b) “Location of element in list” fails the completeness property.
Give an example that illustrates this.**

**(c) Supply one or more new partitions that capture the intent of
“Location of element in list” but do not suffer from
completeness or disjointness problems.**

a. “Location of element in list” fails the disjointness property. Give an example that illustrates this:
    If the element is first entry in list, Block 1 and Block 2 will be jointed.
b. “Location of element in list” fails the completeness property. Give an example that illustrates this:
    If the element is last entry, it can either be null or not in the list.
c. Supply one or more new partitions that capture the intent of “Location of element in list” but do not suffer from completeness or disjointness problems:
    - Block 1: element is not null but it still in the list.
    - Block 2: element is either not null or not in the list.
    - Block 3: element is null.
