# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
### Truth table for full adder:
![image](https://github.com/23008859/FULL_ADDER_SUBTRACTOR/assets/139117979/4dc0a371-685d-42d1-b738-5ac7f5ec2370)
### Truth table for full subtractor:
![image](https://github.com/23008859/FULL_ADDER_SUBTRACTOR/assets/139117979/8993c3eb-0ee4-4123-9d14-06bd73cbfae1)

**Procedure**

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder and full subtractor circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Shashin prasad S
RegisterNumber:212222230144
*/
```
module FullAddSub(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule
```
![image](https://github.com/23008859/FULL_ADDER_SUBTRACTOR/assets/139117979/e1658e06-9d94-4bd2-b52a-e67a8ed2fcf4)

**RTL Schematic**

![image](https://github.com/23008859/FULL_ADDER_SUBTRACTOR/assets/139117979/d770185e-70e7-4cc8-9330-2f58b250f911)

**Output Timing Waveform**
![image](https://github.com/23008859/FULL_ADDER_SUBTRACTOR/assets/139117979/10335b6a-28c4-4b8b-85ea-0e4de12beb8c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



