Half Adder using Verilog HDL

📌 Project Description

A Half Adder is a combinational digital circuit used to add two single-bit binary numbers.

It has:

- 2 inputs: A and B
- 2 outputs: Sum and Carry

🎯 Objective

To design and simulate a Half Adder using Verilog HDL and verify its functionality using a testbench.

🔧 Inputs and Outputs

Signal| Description
A| First input bit
B| Second input bit
Sum| Sum output
Carry| Carry output

🧮 Boolean Expressions

Sum

Sum = A XOR B

Carry

Carry = A AND B

📊 Truth Table

A| B| Sum| Carry
0| 0| 0| 0
0| 1| 1| 0
1| 0| 1| 0
1| 1| 0| 1

🏗️ Block Diagram

        ┌─────────┐
A ─────►│   XOR   │─────► Sum
        └─────────┘

        ┌─────────┐
A ─────►│   AND   │─────► Carry
        └─────────┘
B ─────►

💻 Verilog Implementation

module half_adder(
    input A,
    input B,
    output Sum,
    output Carry
);

assign Sum = A ^ B;
assign Carry = A & B;

endmodule

🧪 Testbench

The testbench applies all four possible input combinations:

00
01
10
11

The corresponding Sum and Carry outputs are displayed in the console.

🖥️ Expected Console Output

A B | Sum Carry
----------------
0 0 |  0    0
0 1 |  1    0
1 0 |  1    0
1 1 |  0    1

📈 Simulation

The testbench generates a "waveform.vcd" file.

The waveform can be viewed using GTKWave.

The waveform should contain the following signals:

- A
- B
- Sum
- Carry

Take a screenshot of the waveform and save it as:

simulation/waveform.png

▶️ How to Run the Project

Using Icarus Verilog

Compile the Verilog files:

iverilog -o half_adder_sim half_adder.v half_adder_tb.v

Run the simulation:

vvp half_adder_sim

Open the waveform:

gtkwave waveform.vcd

🛠️ Tools Used

- Verilog HDL
- Icarus Verilog
- GTKWave
- Visual Studio Code
- GitHub

📚 Applications

Half Adders are basic building blocks used in:

- Digital arithmetic circuits
- Full Adder circuits
- ALUs
- Binary addition circuits
- Digital processors

👩‍💻 Author

JAINY INDHU

Electronics and Communication Engineering