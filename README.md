# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure:**
1. Create a new project in Quartus II software.
2. Type the Verilog program for the 4 Bit Ripple Counter.
3. Compile the program and observe the RTL schematic of the 4 Bit Ripple Counter.
4. Create a new University Program Waveform File.
5. Add input and output nodes using Node Finder.
6. Apply clock pulses for the counter operation.
7. Observe the binary counting sequence in the timing waveform.

**PROGRAM:**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by: RAAGHAVI S  RegisterNumber: 212225040321
*/
```
module DEExp6(
    input clk,
    input rst,
    output reg [3:0] count
);

always @(posedge clk or posedge rst)
begin
    if (rst)
        count <= 4'b0000;
    else
        count <= count + 1'b1;
end

endmodule
```
**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="1919" height="1022" alt="Screenshot 2026-05-28 112450" src="https://github.com/user-attachments/assets/63615679-d900-40a4-9911-9a3870098c36" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1919" height="1022" alt="Screenshot 2026-05-28 113050" src="https://github.com/user-attachments/assets/48b86275-017f-48b5-bf44-da2fb2f32cd0" />

**RESULTS:**
Thus, the 4-BIT-RIPPLE-COUNTER successfully designed and verified using Quartus software.
