# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
## Logic Diagram (using nand gate) and (using nor gate):
![image](https://github.com/MANIKUMARDK/Experiment--02-Implementation-of-combinational-logic-/assets/147215581/4260b9f2-f8e9-4c22-bfcf-fe33ca1f9c67)

## Procedure
*Create a project with required entities.
*Create a module along with respective file name.
*Run the respective programs for the given boolean equations.
*Run the module and get the respective RTL outputs.
*Create university program(VWF) for getting timing diagram.
*Give the respective inputs for timing diagram and obtain the results.
## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: MANIKUMAR D.K
RegisterNumber: 23013588
module combinational(a,b,c,d,w,x,y,z,fl,f2);
input a,b,c,d,w,x,y,z;
output fl,f2;
wire g1=((~a)&(~b)&(~c)&(~d)); 
wire g2=((a)&(~c)&(~d));
wire g3=((~b)&(c)&(~d));
wire g4=((~a)&(b)&(c)&(d)); 
wire g5=((b)&(~c)&(d));
assign fl=g1|g2|g3|g4|g5; 
wire g6=((x)&(~y)&(z));
wire g7=((~x)&(~y)&(z));
wire g8=((~w)&(x)&(y)); 
wire g9=((w)&(~x)&(y));
wire g10=((w)&(x)&(y)); 
assign f2=g6|g7|g8|g9|g10;
endmodule
```
## OUTPUT:
## RTL realization of NAND AND NOR gates:
![image](https://github.com/MANIKUMARDK/Experiment--02-Implementation-of-combinational-logic-/assets/147215581/ec21ccc8-06cf-43d8-b895-519dd087c7a4)

## Truthtable of NAND gate:
![image](https://github.com/MANIKUMARDK/Experiment--02-Implementation-of-combinational-logic-/assets/147215581/0c0ceca5-a3eb-4391-b752-1c05603096dc)

## Truthtable of NOR gate:
![image](https://github.com/MANIKUMARDK/Experiment--02-Implementation-of-combinational-logic-/assets/147215581/8bfb82a0-bd72-4a90-9846-e07e786ef5bc)

## Timing Diagram:
![image](https://github.com/MANIKUMARDK/Experiment--02-Implementation-of-combinational-logic-/assets/147215581/c1be17b8-c04b-4b80-b5ed-cdcb6e9ca9c1)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
