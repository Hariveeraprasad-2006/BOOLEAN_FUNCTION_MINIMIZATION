# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:Arikatla Hari Veera Prasad
RegisterNumber:212223240014
'''
module Booleanminimization(
    input a, b, c, d, w, x, y, z,
    output f1, f2
);

wire adash, bdash, cdash, ddash, ydash, zdash, wdash;
not(adash, a);
not(bdash, b);
not(cdash, c);
not(ddash, d);
not(ydash, y);
not(zdash, z);
not(wdash, w);

wire p, q, r, s, t, u, term1, term2, term3;

and(p, bdash, ddash);
and(q, adash, b, d);
and(r, a, b, cdash);
and(term1, ydash, z);
and(term2, x, y);
and(term3, w, y);

or(f1, p, q, r);
or(f2, term1, term2, term3);

endmodule
'''
*/


**RTL realization**
![image](https://github.com/Hariveeraprasad-2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/145049988/c4ccc351-335d-4f44-9673-512f1d2a0dd5)

**Output:**
![image](https://github.com/Hariveeraprasad-2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/145049988/b5613c8c-d088-4737-8149-18af1386c27a)

**Truth Table**
![image](https://github.com/Hariveeraprasad-2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/145049988/c7456d0f-f32f-48db-a57f-59201c375c5c)
**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

