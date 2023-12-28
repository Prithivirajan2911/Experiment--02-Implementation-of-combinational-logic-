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
 

## Procedure:
1. *Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. *Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. *Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4. *Compile the Project:

To compile the project, click on "Processing" > "Start Compilation" in the menu.

Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. *Analyze and Fix Errors:*

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.

6. *Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table amd then simulate the Output waveform

## Program:
```
\*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: PRITHIVIRAJAN V
RegisterNumber:  212223100042
\*
module KMAP(a,b,c,d,w,x,y,z,F1,F2); 
input a,b,c,d,w,x,y,z; 
output F1,F2; 
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5; 
assign A1=(~a&(~b)&(~c)&(~d)); 
assign A2=(a&c&(~d)); 
assign A3=((~b)&c&(~d));
assign A4=((~a)&b&c&d);
assign A5=(b&(~c)&d);
assign F1=A1|A2|A3|A4|A5; 
assign B1=(x&(~y)&z); 
assign B2=(~x&(~y)&z); 
assign B3=(~w&x&y);
assign B4=(w&(~x)&y);
assign B5=(w&x&y);
assign F2=B1|B2|B3|B4|B5;
endmodule
```

## Output:
## RTL realization:
![289911250-df6247c7-27ac-421b-bb36-6d26dc5d7ba2](https://github.com/Prithivirajan2911/Experiment--02-Implementation-of-combinational-logic-/assets/147020085/7a4a55e4-1fb4-4626-81e7-da0d232061c1)

## Truth Table:

![image](https://github.com/Prithivirajan2911/Experiment--02-Implementation-of-combinational-logic-/assets/147020085/e8e14387-6c1b-4b13-a7ff-990d922b07fa)

## Timing Diagram
![289911377-0d8a359e-dca2-4a2a-9cd6-2d371a883feb](https://github.com/Prithivirajan2911/Experiment--02-Implementation-of-combinational-logic-/assets/147020085/2db5b65d-6129-4102-a140-293809eee66c)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
