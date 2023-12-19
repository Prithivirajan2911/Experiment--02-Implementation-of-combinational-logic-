# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 

## Logic Diagram
![image](https://github.com/Prithivirajan2911/Experiment--02-Implementation-of-combinational-logic-/assets/147020085/a04fa257-6df8-4417-a09a-d60f9349ff9c)

## Procedure
## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

Developed by: PRITHIVIRAJAN V

RegisterNumber:  23003859
*/
```
module Kmap(A,B,C,D,,F1);
input A,B,C,D;
output F1;
wire Abar,Bbar,Cbar,Dbar,v,w,x,y,z;
assign Abar=-A;
assign Bbar=-B;
assign Cbar=-C;
assign Dbar=-D;
assign v=Abar&Bbar&Cbar&Dbar;
assign w=A&Cbar&Dbar;
assign x=Bbar&C&Dbar;
assign y=Abar&B&C&D;
assign z=B&Cbar&D;
assign F1=v|w|x|y|z;
endmodule
```

## RTL realization
![image](https://github.com/Prithivirajan2911/Experiment--02-Implementation-of-combinational-logic-/assets/147020085/1ce65af6-356f-4119-88f3-d4f354dd9a8f)

## Output:
## Timing Diagram
![image](https://github.com/Prithivirajan2911/Experiment--02-Implementation-of-combinational-logic-/assets/147020085/564b8ab8-59d2-4a44-be5f-2f15d53d4b5b)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
