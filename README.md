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


![full-subtractor2](https://github.com/user-attachments/assets/92a13e06-b30e-4f93-8f07-929cbb932fc0)

**Procedure**

Write the detailed procedure here

**Program:**
```
Full Adder:
module fulladder(a, b, cin, sum, carry);
 input a;
 input b;
 input cin;
 output sum;
 output carry;
assign sum=a^b^cin;
assign carry=(a & b) | (b & cin) | (cin & a);
endmodule

Full Subtractor:
module fullsub(a, b, cin, diff, borrow);
 input a;
 input b;
 input cin;
 output diff;
 output borrow;
wire abar;
assign abar= ~ a;
assign diff=a^b^cin;
assign borrow=(abar & b) | (b & cin) |(cin & abar);
endmodule

```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: Mitran R

RegisterNumber: 24006381


**RTL Schematic**

Full Adder:
![4 1 1](https://github.com/user-attachments/assets/7abf0d20-c3f6-49b3-a45c-fbd9c32b0754)

Full Subtractor:
![4 2 1](https://github.com/user-attachments/assets/de8a0aaf-3b05-4b7d-9e24-ae0b31192a10)


**Output Timing Waveform**

Full Adder:
![4 1 2](https://github.com/user-attachments/assets/dfa00610-57ea-4a58-bf42-bfee90ebfc19)

Full Subtractor:
![4 2 2](https://github.com/user-attachments/assets/11dd4a8b-efc1-4077-977b-a5e430b8d146)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



