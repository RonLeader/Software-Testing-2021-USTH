**3.5: Find the flaw of a given testSort() method, and describe it using the RIPR model.**

The assertion only checks a small part of the ultimate state (the first element in the list). So if a test causes a fault to infect, and so propagate to a different a part of the ultimate state, the failure won't be revealed. The test oracle must look the whole list.



