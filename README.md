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

FULL ADDER

![Screenshot 2024-11-13 133747](https://github.com/user-attachments/assets/df3b1680-929d-46b5-b3b0-c04150015d28)

FULL SUBTRACTOR

![Screenshot 2024-11-13 133805](https://github.com/user-attachments/assets/04a22a57-1a4c-4439-9142-6fe5ef6f024b)


**Procedure**

Write the detailed procedure here

**Program:**

FULL ADDER
```
module exp5(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor(sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and(c2,sl,cin);
or(cout,c2,cl);
endmodule
```

FULL SUBTRACTOR
```
module exp6(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:Vikaskumar M

RegisterNumber:24900247


**RTL Schematic**

FULL ADDER

![exp5](https://github.com/user-attachments/assets/03a040f9-7a93-4fb9-a6e1-c8aebc30070d)

FULL SUBTRACTOR

![exp6](https://github.com/user-attachments/assets/cba92280-0073-4663-835c-96a44af7be03)


**Output Timing Waveform**

FULL ADDER

![Screenshot 2024-11-12 112536](https://github.com/user-attachments/assets/c60928b4-37e1-41c0-a7ef-15627b2a3591)

FULL SUBTRACTOR

![Screenshot 2024-11-13 000156](https://github.com/user-attachments/assets/f046966e-9a43-4a82-9705-41cd3e8d1b2c)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



