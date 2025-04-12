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
**FULL ADDER**

![Screenshot 2024-12-07 105703](https://github.com/user-attachments/assets/fe96b657-c587-44ae-a8b5-2b8ec94a6bd5)

**FULL SUBRACTOR**

![Screenshot 2024-12-07 105754](https://github.com/user-attachments/assets/631a1a32-10bb-4d54-870a-3bd0795cd102)

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```python
Developed by:Tharshini.M
RegisterNumber:24900038
```
```python
**Full adder**

    module fa(a,b,cin,sum,carry);
    input a,b,cin;
    output sum,carry;
    assign sum=( (a ^ b)^cin);
    assign carry= ( (a & b)| ( cin &(a ^ b )));
    endmodule

**Full subractor**

    module fs(a,b,bin,difference,borrow);
    input a,b,bin;
    output difference,borrow;
    assign difference= ( (a ^ b)^bin);
    assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
    endmodule
```

**RTL Schematic**
![Screenshot 2024-12-07 161748](https://github.com/user-attachments/assets/f52b9eba-ae47-4b68-86fc-0f8438e0a024)

![Screenshot 2024-12-07 162127](https://github.com/user-attachments/assets/d755d0cb-1669-4621-99c2-89ff5d741bd0)

**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/7991dc63-56be-4839-ad9e-f80408593d27)

![image](https://github.com/user-attachments/assets/cda2a52d-8fc0-4130-afc3-7936e0f6859d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



