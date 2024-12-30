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

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:A.AKILA RegisterNumber:24900889


**RTL Schematic**

FULL SBTRACTOR

**Output Timing Waveform**
![FULL SUBTRACTOR](https://github.com/user-attachments/assets/ef425a6a-2dc6-48b0-ba2f-e5f8faece996)

![FULL ADDER](https://github.com/user-attachments/assets/d1a9e808-5d74-430f-bd62-29ea633ed4fb)



FULL SUBTRACTOR
```
module subtractor (v,j,b,t,s);
input v,j,b;
output t,s;
assign t=v^j^b;
assign s=(~v&b)|(~v&j)|(~j&b);
endmodule
```

FULL ADDER
```
module fulladder (a,b,c,p,q);
input a,b,c;
output p,q;
assign p=a^b^c;
assign q=(a&b)|(b&c)|(a&c);
endmodule
```

![FULL SUBTRACTOR WAVEFORM](https://github.com/user-attachments/assets/193344eb-c627-4e1d-b206-b71a44ff0500)

![FULL ADDER WAVEFORM](https://github.com/user-attachments/assets/b78002f2-8b72-407d-80e0-88187cd157ad)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



