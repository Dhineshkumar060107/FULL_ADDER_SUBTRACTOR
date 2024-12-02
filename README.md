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
![full adder](https://github.com/user-attachments/assets/f770c709-3e33-4c86-8bf6-8ea08cb3d16a)(truth table for full adder)
![full subractor](https://github.com/user-attachments/assets/37338be2-2163-4fda-90f2-784c08d8c2af)(truth table for full subractor)



**Procedure**
```
full adder
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
```
full subractor
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```





Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Dhineshkumar.L
RegisterNumber:24900785


**RTL Schematic**
![Screenshot 2024-12-02 195839](https://github.com/user-attachments/assets/e0faea39-8ca1-4dc7-a96a-6d055f5ec00d)(full adder)
![Screenshot 2024-12-02 200618](https://github.com/user-attachments/assets/69b4133b-67a6-4466-bab3-f421106f8348)(full subractor)



**Output Timing Waveform**
![Screenshot 2024-12-02 200102](https://github.com/user-attachments/assets/8fdbd39f-a855-4668-b835-8272b80ff5ee)(full adder wave form)
![Screenshot 2024-12-02 200855](https://github.com/user-attachments/assets/fd908239-6cd8-4f5a-903d-609f20fb5a41)(full subractor wave form)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



