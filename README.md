# Full_Adder-using_CMOS_Mirror_Logic_on_28nm
- This repository presents the Design of 1-Bit Full Adder. Performance improvement of Full Adder has been done by using XOR & AND gates.. Design is implemented using Synopsis Custom Compiler on 28nm CMOS Technology.
## Table of Content
- Abstract
- Circuit Details
- Truth Table
- Tools Used
- Reference Circuit
- Reference Waveform
- 1-Bit Full Adder
- Schematic
- Waveform
- Delay
- Average Power
- Netlist
- Conclusion
- Author
- Acknowledgement
- References
 ## Abstract 
-  A full adder circuit is central to most digital circuits that perform addition or subtraction. It is so called because it adds together two binary digits, plus a carry-in digit to produce a sum and carry-out digit. Therefore, it has three inputs and two outputs.1-Bit Full Adder can be used to implement other circuits such as Multipliers,Carry Look Head.A 1-bit full adder using CMOS mirror logic is designed and implemented in this repository. The implementation will be done in 28nm technology node using Synopsys tools.The reference waveforms will be verified with actual waveforms obtained from simulation.The major drawback of the CMOS mirror circuit is that it consumes more power and occupies more area due to the greater number of transistors used.
 ## Circuit Details
![diagram](https://user-images.githubusercontent.com/100487671/156156740-83fb1b4d-3b2c-416f-987f-b1d9e57b109b.PNG)
 ## Truth Table
![Truth_Table](https://user-images.githubusercontent.com/100487671/156156781-79e2704a-7a0a-4fcd-9a50-063644368f41.PNG)
Logical Expression for SUM:
= A’ B’ C-IN + A’ B C-IN’ + A B’ C-IN’ + A B C-IN
= C-IN (A’ B’ + A B) + C-IN’ (A’ B + A B’)
= C-IN XOR (A XOR B)
= (1,2,4,7)

Logical Expression for C-OUT:
= A’ B C-IN + A B’ C-IN + A B C-IN’ + A B C-IN
= A B + B C-IN + A C-IN
= (3,5,6,7)

Another form in which C-OUT can be implemented:
= A B + A C-IN + B C-IN (A + A’)
= A B C-IN + A B + A C-IN + A’ B C-IN
= A B (1 +C-IN) + A C-IN + A’ B C-IN
= A B + A C-IN + A’ B C-IN
= A B + A C-IN (B + B’) + A’ B C-IN
= A B C-IN + A B + A B’ C-IN + A’ B C-IN
= A B (C-IN + 1) + A B’ C-IN + A’ B C-IN
= A B + A B’ C-IN + A’ B C-IN
= AB + C-IN (A’ B + A B’)
Therefore COUT = AB + C-IN (A EX – OR B)
## Tools Used
   1-Synopsys Custom Compiler:  The Synopsys Custom Compiler design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
    
   2-Synopsys Primewave:  PrimeWave Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
    
   3-Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.
    
 ## Reference Circuit
   ![Reference_Schematic](https://user-images.githubusercontent.com/100487671/156157820-590d7c37-bf76-4f81-8296-ae706e24dbf8.jpeg)
   
  ## Reference Waveform
  ![Refernce_Waveform](https://user-images.githubusercontent.com/100487671/156157923-bd770069-c36a-4118-b20b-116cb7e8d6e2.jpeg)
  
## Simulation in Synopsis
   
   # Schematic
   ![schematic_synopsys](https://user-images.githubusercontent.com/100487671/156159551-19f63d93-5b9d-498f-b87f-d51807b18d0b.PNG)
   
   # Waveform
   ![wffff](https://user-images.githubusercontent.com/100487671/156164382-5d791791-364c-4dd5-9a96-9480ef8256e5.PNG)

   # Delay
   ![syn_delay](https://user-images.githubusercontent.com/100487671/156160465-1b5e4f0e-e685-4362-be61-ef361801e97f.PNG)
   
   # Average Power
   ![synopsys_power](https://user-images.githubusercontent.com/100487671/156160520-7d362f6f-d2af-41ab-abc2-ac3c862a4ae5.PNG)
   
## Conclusion
    - The Reference circuit of 1-Bit Full Adder using CMOS mirror logic is successfully implemented using Synopsys tools and simulation waveforms are obtained. The obtained waveforms match with the reference waveforms.

## Author
    - Ishika Maheshwari, BTech Electronics and commuincations, ABESEC, Ghaziabad, Uttar Pradesh.
 
 ## Acknowledgement
     . Cloud Based Analog IC Design Hackathon
     . Synopsys India
     . Kunal Ghosh, Co-founder, VSD Corp. Pvt Ltd.
     . Chinmay panda, IIT Hyderabad
     . Sameer Durgoji, NIT Karnataka
     
 # References
    . S. Dhanjal. 1-Bit Full Adder transistor level implementation using CMOS Mirror Logic
      https://youtu.be/BflzLRjsECM
      
    . Sanjay Vidhyadharan, 1-Bit Full Adder implementation using CMOS Mirror Logic
      https://youtu.be/AXU_J4wr_yA
 

   


