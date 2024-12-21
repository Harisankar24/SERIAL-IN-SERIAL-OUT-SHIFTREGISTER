# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */
Step1: Define the specifications and initialize the design. 
Step2: Declare the name of the entity and architecture by using VHDL source code. 
Step3: Write the source code in VERILOG. 
Step4: Check the syntax and debug the errors if found, obtain the synthesis report. 
Step5: Verify the output by simulating the source code. 
Step6: Write all the possible combinations of input using test bench. 

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:Harisankar s
RegisterNumber:24900861
module exp10(a, b, clk, rst, acc); 
input [7:0] a; 
input [7:0] b; 
input clk; 
input rst; 
output [15:0] acc; 
reg [15:0] acc; 
reg [15:0] pd; 
reg [15:0] adder; 
always @ (posedge(clk) or posedge(rst)) 
begin 
if (rst==1'b1) 
  begin 
  adder=8'b00000000; 
  end 
  else 
  begin 
  pd=a*b; 
  adder=adder+pd; 
  end 
  acc=adder; 
  end 
  endmodule

*/

**RTL LOGIC FOR SISO Shift Register**
![Screenshot 2024-12-21 100210](https://github.com/user-attachments/assets/616d39b7-ba70-407d-8472-e2295df42fbd)


**TIMING DIGRAMS FOR SISO Shift Register**
![Screenshot 2024-12-21 100337](https://github.com/user-attachments/assets/7b91ab74-af2a-419b-aa93-5601ff3c3ee5)


**RESULTS**
 Thus the OUTPUT’s of MAC Unit  are verified by synthesizing and simulating the VHDL and 
VERILOG code. 
