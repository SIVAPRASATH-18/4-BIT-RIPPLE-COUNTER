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

**Procedure**
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram

**PROGRAM**
```
module ripple_counter_4bit (
    input  wire clk,
    input  wire reset,
    output reg [3:0] q
);

    always @(posedge clk or posedge reset) begin
        if (reset)
            q <= 4'b0000;
        else
            q <= q + 1'b1;   // increments like a ripple counter
    end

endmodule

```

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by: SIVAPRASATH B RegisterNumber:25016007
*/

**RTL LOGIC FOR 4 Bit Ripple Counter**

<img width="910" height="349" alt="Screenshot 2025-12-10 184750" src="https://github.com/user-attachments/assets/c1f827cb-2674-467b-8033-3a0f32bf4ed7" />


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

<img width="1247" height="253" alt="Screenshot 2025-12-10 184809" src="https://github.com/user-attachments/assets/11ac07e9-7cf0-4cd0-a91d-fd778f80f280" />


**RESULTS**
Thus To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables is verified
