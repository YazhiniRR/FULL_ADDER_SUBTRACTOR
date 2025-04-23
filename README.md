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


![Screenshot 2025-04-23 224333](https://github.com/user-attachments/assets/c4c136c3-1e5b-4551-abbb-76f290aadf9b)

FULL SUBTRACTOR


![Screenshot 2025-04-23 224333](https://github.com/user-attachments/assets/1323800a-deac-4536-8af4-22547a1faeef)

**Procedure**

Write the detailed procedure here

**Program:**

FULL ADDER
```
module ex4a(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b;
input cin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule
```
FULL SUBTRACTOR
```
module ex4b(df, bo, a, b, bin);
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
#Developed by:YAZHINI R R
#RegisterNumber:212224100063
*/

**RTL Schematic**
FULL ADDER


![Screenshot 2025-04-23 223610](https://github.com/user-attachments/assets/e3e2eb78-3d92-41ff-9310-7f39643b3142)
FULL SUBTRACTOR


![Screenshot 2025-04-23 223719](https://github.com/user-attachments/assets/36591ea5-7167-43cb-b5e1-f1852d6461cf)


**Output Timing Waveform**
FULL ADDER


![Screenshot 2025-04-23 223627](https://github.com/user-attachments/assets/31766043-ee6c-4370-88a2-5e6a86f80c9b)
FULL SUBTRACTOR


![Screenshot 2025-04-23 223731](https://github.com/user-attachments/assets/af10c9b6-5739-44ff-9a11-d36eac953a7d)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



