# AIM: 
To simulate and synthesis  SR flilflop  using vivado. 
# APPARATUS REQUIRED: 
vivado 2023.2 software. 
# PROCEDURE: 
STEP:1 Start the vivado software, Select and Name the New project. 
STEP:2 Select the device family, device, package and speed. 
STEP:3 Select new source in the New Project and select Verilog Module as the 
Source type. 
STEP:4 Type the File Name and module name and Click Next and then finish 
button. Type the code and save it. 
STEP:5 Select the run simulation and then run Behavioral Simulation in the 
Source Window and click the check syntax. 
STEP:6 Click the simulation to simulate the program and give the inputs and 
verify the outputs as per the truth table. 
STEP:7 compare the output with truth table.
# SR_FLIPFLOP
![image](https://github.com/RESMIRNAIR/SR_FLIPFLOP/assets/154305926/c17acfa3-84d9-4ef6-99ab-d36655169f63)
# Circuit Diagram
![image](https://github.com/RESMIRNAIR/SR_FLIPFLOP/assets/154305926/51cb1738-6112-466e-a1b0-f9dd9f2e9d25)
# Truth Table
![image](https://github.com/RESMIRNAIR/SR_FLIPFLOP/assets/154305926/0946849a-bd0a-445b-b27e-0833dee20e51)
# verilog code
module sr(clk,s,r,rst,q ); 
input s,r,clk,rst; 
output reg q; 
always@(posedge clk) 
begin 
if(rst==1) 
q=1'b0; 
else 
begin 
case({s,r}) 
2'b00: q=q; 
2'b01:q=1'b0; 
2'b10:q=1'b1; 
2'b11:q=1'bx; 
endcase 
end 
end 
endmodule 
# output
![Screenshot (59)](https://github.com/lathika024/SR_FLIPFLOP/assets/165888553/d1e0aea3-6731-4540-9846-72e6b1df3d58)
# result
thus the SR flipflop is verified successfully 

