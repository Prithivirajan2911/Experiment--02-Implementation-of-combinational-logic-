# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
  
## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime

## Theory:
A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.
 
## Logic Diagram
![image](https://github.com/Prithivirajan2911/Experiment--02-Implementation-of-combinational-logic-/assets/147020085/a04fa257-6df8-4417-a09a-d60f9349ff9c)

## Procedure:
Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.
Compile the Project:

To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
Analyze and Fix Errors:*

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table amd then simulate the Output waveform

## Program:
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
~~~
Developed by: PRITHIVIRAJAN V
RegisterNumber:  23003859
~~~
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
