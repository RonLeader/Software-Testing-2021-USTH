**Replace each occurrence of a set with a list in the JUnit theory removeThenAddDoesNotChangeSet. Is the resulting theory valid or invalid? How many of the tests that pass the precondition also pass the postcondition? Explain**


The resulting theory is invalid because order matters in lists. When we remove then add an element back, its position in the list could have been changed and thus, the list is different.

The the three test cases, just one can pass the test.

Conclusion: The JUnit theory fails.
```Java
import org.junit.*;
import org.junit.runner.RunWith;
import static org.junit.Assert.*;
import static org.junit.Assume.*;

import org.junit.experimental.theories.DataPoint;
import org.junit.experimental.theories.DataPoints;
import org.junit.experimental.theories.Theories;
import org.junit.experimental.theories.Theory;

import java.util.*;

@RunWith (Theories.class)
public class ListTheoryTest
{
   @DataPoints
   public static String[] string = {"apple", "grape", "orange", "pear"};

   @DataPoints
   public static List[] lists = {
      Arrays.asList ("apple", "grape", "orange"),
      Arrays.asList ("orange", "pear", "strawberry"),
      Arrays.asList ("strawberry")
   };


   @Theory
   public void removeThenAddDoesNotChangeList
                   (List<String> list, String string)  // Parameters!
   {
      assumeTrue (list != null);            // Assume
      assumeTrue (list.contains (string));  // Assume
      List<String> copy = new ArrayList<String>(list);   // Act
      copy.remove (string);                       
      copy.add (string);
      assertTrue (list.equals (copy));      // Assert
    }
}
