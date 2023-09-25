# RTL-Day-6-Parallel-Adder-Subtractor

### Problem Statement: Implementing a 4-Bit Parallel Adder / Subtractor using Structural Style of Implementation.
### Theory: 
In Digital Circuits, A Binary Adder-Subtractor is capable of both the addition and subtraction of binary numbers in one circuit itself. The operation is performed depending on the binary value the control signal holds. It is one of the components of the ALU (Arithmetic Logic Unit).

 ![image](https://github.com/tusharshenoy/RTL-Day-6-Parallel-Adder-Subtractor/assets/107348474/31e1faf6-31cc-4201-9c91-8572f7e29010)

FIG: 4-Bit Parallel Adder / Subtractor

As shown in the figure, the first full adder has a control line directly as its input (input carry Cin), the input A0 (The least significant bit of A) is directly input in the full adder. The third input is the exor of B0 and K. The two outputs produced are Sum/Difference (S0) and Carry (C0). 

If the value of K (Control line) is 1, the output of B0 (exor) K=B0′ (Complement B0). Thus the operation would be A+ (B0′). Now 2’s complement subtraction for two numbers A and B is given by A+B’+Cin. This suggests that when K=1, the operation being performed on the four-bit numbers is subtraction. 

Similarly If the Value of K=0, B0 (exor) K=B0. The operation is A+B which is simple binary addition. This suggests that When K=0, the operation is performed on the four-bit numbers in addition. 

Then C0 is serially passed to the second full adder as one of its outputs. The sum/difference S0 is recorded as the least significant bit of the sum/difference. A1, A2, A3 are direct inputs to the second, third and fourth full adders. Then the third input is the B1, B2, B3 EXORed with K to the second, third and fourth full adder respectively. The carry C1, C2 are serially passed to the successive full adder as one of the inputs. C3 becomes the total carry to the sum/difference. S1, S2, S3 are recorded to form the result with S0.

### Drawback of Parallel Adder or Subtractor
As the architecture of parallel adder or subtractor is very similar to that of a parallel adder (and also to that of a parallel subtractor), even this design is prone to the effect of ripple propagation delay. Nevertheless, these kind of circuits find their application in the field of computers as a part of arithmetic and logic (ALU) unit, aiding numerous computations.


Simulation Output:
•	Parallel Adder, K=0

![image](https://github.com/tusharshenoy/RTL-Day-6-Parallel-Adder-Subtractor/assets/107348474/6f1fd630-6acd-4b2b-b20f-e0b48d026d4a)
 
•	Parallel Subtractor, K=1
 
![image](https://github.com/tusharshenoy/RTL-Day-6-Parallel-Adder-Subtractor/assets/107348474/acf2e047-b9ec-4afe-b1bc-582e39d931d7)



Schematics:

![image](https://github.com/tusharshenoy/RTL-Day-6-Parallel-Adder-Subtractor/assets/107348474/bc54d7b0-2825-4235-b951-15ab45cbb032)
                              
 #### FIG: Block Diagram of full_adder_1bit

 ![image](https://github.com/tusharshenoy/RTL-Day-6-Parallel-Adder-Subtractor/assets/107348474/42a14d91-785a-41b4-bc6f-757745791156)

 #### FIG: Schematic of full_adder_1bit

 ![image](https://github.com/tusharshenoy/RTL-Day-6-Parallel-Adder-Subtractor/assets/107348474/e01002be-f859-46e3-b599-d5e736fa2173)

 #### FIG: Schematic of Parallel Adder/Subtractor


### References
1. [Parallel Adder/Subtractor](https://www.geeksforgeeks.org/parallel-adder-and-parallel-subtractor/)
