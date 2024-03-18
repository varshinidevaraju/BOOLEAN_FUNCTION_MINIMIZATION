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

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: Varshini D
RegisterNumber: 212223230234

```

module verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule

```


**RTL realization**

![image](https://github.com/varshinidevaraju/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870750/692d125e-c638-4199-92bf-c77d11222908)

**Truthtable**

![image](https://github.com/varshinidevaraju/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870750/cded3525-e9e9-48da-bdf6-230f95c7002d)

**Timing Diagram**

![image](https://github.com/varshinidevaraju/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870750/c228bd98-3f3d-4383-b8ec-75b9433b1760)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
