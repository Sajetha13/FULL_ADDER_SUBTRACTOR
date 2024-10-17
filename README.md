# EXP 04: FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

## AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor:

### Full Adder:

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

Figure -1 FULL ADDER

## Full Subtractor:

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## Truthtable:

### Full-Adder:

![image](https://github.com/user-attachments/assets/9f349480-e938-44c5-8ff8-66fd2c1c8def)

### Full-Subtractor;

![image](https://github.com/user-attachments/assets/5c5b23e2-46ee-4f95-bda3-22c192eb7b6c)


## Procedure:

1. Define the module with inputs and outputs for Full Adder/Subtractor.
2. Implement the logic for Sum and Carry (Full Adder) or Difference and Borrow (Full Subtractor) using XOR and AND gates.
3. Create a testbench to simulate different input combinations.
4. Compile and synthesize the Verilog code using Quartus Prime.
5. Verify outputs against expected truth tables to ensure correct functionality.

## Program:

#### Developed By: S Sajetha
#### Register Number: 212223100049

### Program to design a Full Adder circuit and verify its truth table in Quartus using Verilog programming.

```
module ep4(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
```

![image](https://github.com/user-attachments/assets/f46892c3-c24a-4d2e-a7a5-d3c2eb07be7b)

### Program to design a Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

```
module ep41(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```

![image](https://github.com/user-attachments/assets/7c792222-19ed-45c3-b2ea-d6534568496a)


## RTL Schematic:

### Full-Adder:

![image](https://github.com/user-attachments/assets/b16426dd-9380-42c2-869e-a5698f1d737c)

### Full-Subtractor:

![image](https://github.com/user-attachments/assets/cb06e629-fe2e-4ff9-8fcb-7bd15a075e21)

## Output / Timing Waveform:

### Full-Adder:

![image](https://github.com/user-attachments/assets/a5378185-9ef0-4fc7-b2ea-11375c9a2692)

### Full-Subtractor:

![image](https://github.com/user-attachments/assets/d9cf8cf1-75dc-413f-9b3f-530e03fb89ab)


## Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
