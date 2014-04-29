Lab5_Agnolutto
==============
### First Program Operation

This program loads the value 8 into the accumulator and adds one to it until it reaches 0 (values in hex); each value got outputted to 
outport 3. Once the value was greater than 0, it entered an infinite loop. The values outported were: 9, A, B, C, D, E, F,
and 0. 

### First Program Instruction Cycles






### Functionality

Program 1 - Checked off by Capt Trimble on 21 April
Program 2 - Checked off by Capt Trimble on 25 April
FPGA Demo - Checked off by Capt Trimble on 25 April
Cool thing - Not accomplished


### Answers to Questions

1) When the controller's current state is "FETCH," what is the status of the following control lines:
  a) PCLd - 1 (high)
  b) IRLd - 1 (high)
  c) ACCLd - 0 (low)

2) The current state is Decode LoAddr and the IR contains "OUT." What are the control signals asserted, and what will the 
next state be?
   Signals Asserted: AddrSel, EnAccBuffer, IOSel, R/W 
   Next State: Direct IO Execute
  
3) What are the three status signals sent from the PRISM datapath to the PRISM controller?
  IR, AccLessZero, AcceqZero
  
4) Why is it important that ACCLd signal be active during the execute state for the ADDI instruction?
  ADDI adds the current value to the value in the accumulator. So the value in the accumulator must be loaded to the data 
  bus which means ACCLd is active. 
  
5) What changes are necessary to the PRISM datapath to add another instruction (SUBI, which would subtract an immediate 
value from the accumulator) to the instruction set?
  The main change would be 5 bits would be needed, as opposed to the current 4, to store all the instructions. This would effect the ALU, the data bus, and the control bus. This would increase complexity when the commands NEG and ADDI can do the same function. It wouldn't be worth it. 
  
