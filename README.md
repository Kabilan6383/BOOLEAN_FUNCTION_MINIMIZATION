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
module booleanmin(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
assign x1=(~a)&(~b)&(~c)&(~d);
assign x2=(a)&(~c)&(~d);
assign x3=(~b)&(c)&(~d);
assign x4=(~a)&(b)&(c)&(d);
assign x5=(b)&(~c)&(d);
assign f1=x1|x2|x3|x4|x5;
assign x6=(x)&(~y)&(z);
assign x7=(~x)&(~y)&(z);
assign x8=(~w)&(x)&(y);
assign x9=(w)&(~y)&(y);
assign x10=(w)&(x)&(y);
assign f2=x6|x7|x8|x9|x10;
=endmodule
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: RegisterNumber:*/24900859 P.Kabilan


**RTL realization**

**Output:**

**RTL**![WhatsApp Image 2024-12-05 at 18 44 21_c0368338](https://github.com/user-attachments/assets/6569a80f-349a-4db9-884c-dad9482dbcf7)


**Timing Diagram**
![WhatsApp Image 2024-12-05 at 18 44 22_eacb1ae3](https://github.com/user-attachments/assets/0e644280-1ee9-4c17-82c0-aceed9bf4818)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

