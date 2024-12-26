### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

1.Compile and run the program.

2.Generate the RTL schematic and save the logic diagram.

3.Create nodes for inputs and outputs to generate the timing diagram.

4.For different input combinations generate the timing diagram

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: KESHAVARTHINI B  RegisterNumber:24900033
*/

module expd11(clk,rst,q);

input clk,rst;

output[2:0]q;

reg[2:0]q;

always@(posedge clk)

if(~rst==0)

    q<=3'b0;
    
else

    q<=q+1'b1;
    
endmodule


**RTL LOGIC UP COUNTER**

![Screenshot (73)](https://github.com/user-attachments/assets/6a7d9787-480c-41e7-aae6-77ba24d193bd)

**TIMING DIAGRAM FOR IP COUNTER**

![Screenshot (74)](https://github.com/user-attachments/assets/cdd2418c-61e0-4e41-8129-a14f7feacf99)

**TRUTH TABLE**

![WhatsApp Image 2024-12-26 at 23 39 36_72529e7d](https://github.com/user-attachments/assets/b5dc43b9-bdc7-491f-a8a9-54a28ee50b97)

**RESULT**

Thus the OUTPUT’s of Synchronous and counter are verified by synthesizing and simulating the
VERILOG code.

