**The following exercise is intended to encourage you to think of testing in a more rigorous way than you may be used to. The exercisealso hints at the strong relationship between specification clarity, faults, and test cases**

**(a) Write a Java method with the signature public static Vector union (Vector a, Vector b) The method should return a Vector of objects that are in either of the two argument Vectors.**

**(b) Upon reflection, you may discover a variety of defects and ambiguities in the given assignment. In other words, ample opportunities for faults exist. Describe as many possible faults as you can. (Note: Vector is a Java Collection class. If you are using another language, interpret Vector as a list.)**

**(c) Create a set of test cases that you think would have a reasonable chance of revealing the faults you identified above. Document a rationale for each test in your test set. If possible, characterize all of your rationales in some concise summary. Run your tests against your implementation.**

**(d) Rewrite the method signature to be precise enough to clarify the defects and ambiguities identified earlier. You might wish to illustrate your specification with examples drawn from your test cases.**


a,
```Java
import java.util.Vector;
import java.util.ArrayList;
class Vector_demo 
{
  public static Vector union(Vector a, Vector b)
  {
    Vector c = new Vector();
    c.addAll(a);
    c.addAll(b);
    return c;
  }
  public static void main(String[] arg)
  {
    Vector<String> a = new Vector<>();
    a.add("va");
    Vector<String> b = new Vector<>();
    b.add("vb");
    Vector c = union(a, b);
  }
} 
```

b, Lack of verification statements like checking "vector a" or "vector b" is empty or not.

c,

Test case 1
```Java
Vector<String> a = new Vector<>();
Vector<String> b = new Vector<>();
```
Test case 2
```Java
Vector<String> a = new Vector<>();
a.add("vb")
Vector<String> b = new Vector<>();
```
Test case 3
```Java
Vector<String> a = new Vector<>();
Vector<String> b = new Vector<>();
c.add("vb")
```
d,
```Java
public static Vector union(Vector a, Vector b, boolean inv = False)
{
  if (a.isEmpty() && b.isEmpty()) return Null;
  else
  {
    if (inv)
    {
      Vector<String> c = new Vector<>();
      c.addAll(b);
      c.addAll(a);
      return c;
    }
    else
    {
      Vector<String> c = new Vector<>();
      c.addAll(a);
      c.addAll(b);
      return c;
    }
  }
}
```


