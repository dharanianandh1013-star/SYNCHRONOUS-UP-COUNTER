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



**PROGRAM**

UP COUNTER
module ex11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule

DOWN COUNTER
module ex12(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule

Developed by: dharani a
RegisterNumber: 25013947

**RTL LOGIC UP COUNTER**

UP COUNTER

![WhatsApp Image 2025-12-15 at 14 21 57_3891ebe6](https://github.com/user-attachments/assets/ade09c2d-810d-43e0-bd48-0c3c458d0d5b)

DOWN COUNTER

![WhatsApp Image 2025-12-15 at 14 21 56_612ba0db](https://github.com/user-attachments/assets/cb272605-4cb7-449d-8810-952caf01d91c)


**TIMING DIAGRAM FOR IP COUNTER**

UP COUNTER

![WhatsApp Image 2025-12-15 at 14 21 57_d5cc3c59](https://github.com/user-attachments/assets/c4ea4785-2a21-44ad-8a90-01127b035eb8)

DOWN COUNTER

![WhatsApp Image 2025-12-15 at 14 21 56_7833d651](https://github.com/user-attachments/assets/c2ab2b6a-c0b4-4934-9f5a-39a828493eee)

**RESULTS**

Thus the program To implement 4 bit synchronous up counter and validate functionality has been executed successfully and the output is verified
