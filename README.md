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

Developed by: MONISH KUMAR N
RegisterNumber:24012059


**RTL realization**
![Screenshot 2024-11-29 111319](https://github.com/user-attachments/assets/86a4d827-f94d-4775-bc07-51d031a627f4)

**Truth Table**
![Screenshot 2024-11-29 113048](https://github.com/user-attachments/assets/c07bc83b-2ed9-4763-a1a5-07946a033379)


**RTL**
![Screenshot 2024-11-29 111403](https://github.com/user-attachments/assets/9ba7f0ea-c709-45cb-8ae7-2d0d4096cb40)




**Result:**
module deexp(a,b,c,d,F1,F2,w,x,y,z);
input a,b,c,d,w,x,y,z;
output F1,F2;
 wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
 assign x1=(~a)&(~b)&(~c)&(~d);
 assign x2=(a)&(~c)&(~d);
 assign x3=(~b)&(~c)&(~d);
 assign x4=(~a)&(b)&(c)&(d);
 assign x5=(b)&(~c)&(d);
 assign x6=(x)&(~y)&(z);
 assign x7=(~x)&(~y)&(z);
 assign x8=(~w)&(x)&(y);
 assign x9=(w)&(~x)&(y);
 assign x10=(w)&(x)&(y);
 assign F1=x1|x2|x3|x4|x5;
 assign F2=x6|x7|x8|x9|x10;
 endmodule


Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

