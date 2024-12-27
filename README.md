# BOOLEAN_FUNCTION_MINIMIZATION
Date:09.11.2024

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

Developed by: PRIYAADARSHINI K
RegisterNumber:212223240126*/
```
module booleanfunction(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule
```

**RTL realization**
![Screenshot 2024-12-27 101800](https://github.com/user-attachments/assets/520ce2ed-dcab-4631-a817-88229eecf885)


**Truth Table**
![Screenshot 2024-12-27 101813](https://github.com/user-attachments/assets/f3891c6d-b6a4-40ff-a162-4b018b96f06e)



**Timing Diagram**
![Screenshot 2024-12-27 101825](https://github.com/user-attachments/assets/d55f42d4-90a4-4ce6-a899-ae0c582ff326)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

