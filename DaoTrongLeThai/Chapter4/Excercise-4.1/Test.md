``` Java  
import org.junit.Test;
import static org.junit.Assert.*;

public class Test 
{
    Calc calc = new Calc();
    private int x = 1;
    private int y = 1;

    @Test
    public void testAdd()
    {
        assertEquals(calc.add(x, y), 2);
    }

    @Test
    public void testMinus() 
    {
        assertEquals(calc.minus(x, y), 0);
    }

    @Test
    public void testMultiply() 
    {
        assertEquals(calc.multiply(x, y), 1);
    }

    @Test
    public void testDivide() 
    {
        assertEquals(calc.divide(x, y), 1);
    }
}
```
