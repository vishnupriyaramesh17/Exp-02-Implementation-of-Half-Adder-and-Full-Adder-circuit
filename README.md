# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:

/*

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Vishnupriya R

RegisterNumber:  212222110054

*/

module Halfadder(a,b,sum,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule




module fulladd(A,B,Ci,S,Co)

input A,B,Ci;

output S,Co;

wire d,e,f;

xor(d,A,B);

xor(S,d,Ci);

and(e,Ci,d);

and(f,A,B);

or(Co,e,f);

endmodule



Logic symbol & Truthtable

![truth table](https://user-images.githubusercontent.com/119393589/228587081-64a2fef0-d284-4206-b141-a10e544a6292.png)

RTL realization
![half adder output](https://user-images.githubusercontent.com/119393589/228587213-a1706676-8c06-4c51-9f24-ef2d56fe8557.png)

![full adder output](https://user-images.githubusercontent.com/119393589/228587249-742bfe05-8d80-46a8-9a77-8bc61b43b446.png)

Timing Diagram
![half add timing](https://user-images.githubusercontent.com/119393589/228587531-992c9fdd-52ea-47cc-a9cd-2deeacc1bb87.png)

![full add timing](https://user-images.githubusercontent.com/119393589/228587571-de74f60b-2ca2-4833-b286-aafceea3b945.png)

Result:

thus the output for the half adder and full adder are successfully done
