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

**Procedure**

Write the detailed procedure here

**Program:**<br>
module exp4 a(df, bo, a, b, bin);<br>
 output df;<br>
 output bo;<br>
 input a;<br>
 input b;<br>
 input bin;<br>
 wire w1,w2,w3;<br>
 assign w1=a^b;<br>
 assign w2=(~a&b);<br>
 assign w3=(~w1&bin);<br>
 assign df=w1^bin;<br>
 assign bo-w2/w3;<br>
 endmodule<br>
module exp4a (df, bo, a, b, bin);<br>
 output df;<br>
 output bo;<br>
 input a;<br>
 input b;<br>
 input bin;<br>
 wire w1,w2, w3;<br>
 assign w1=a^b;<br>
 assign w2=(~a&b);<br> 
 assign w3=(~w1&bin);<br>
 assign df=w1^bin;<br>
 assign bo=w2|w3;<br>
 endmodule<br>

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:HARIHARASUDHAN N RegisterNumber:*/24900208

**RTL Schematic**<br>
Full adder<br>
![385154484-0c67dfbc-ce03-41dd-917e-e802f122aa69](https://github.com/user-attachments/assets/2185cf58-d5b3-405d-9d0b-570ead6f7068)
Full sbtracter<br>
![385154932-c637d884-caf0-499c-89e3-a391eb05b433](https://github.com/user-attachments/assets/d6392d9a-0b7a-402b-89c5-0c4fea7f6b88)



**Output Timing Waveform**<br>
Output Timing Waveform Full adder<br>
![385155287-a299f5fd-90d9-4b80-82ff-91d5a507ed35](https://github.com/user-attachments/assets/2fb3e4e8-83b9-4aa8-9f86-8344282d92be)
Full sbtracter
![385155358-ca015316-dcf1-4f01-a8ff-e51401190fc2](https://github.com/user-attachments/assets/f702cb1c-80a0-417e-92f4-b9c4602143ed)


**Result:**<br>

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



