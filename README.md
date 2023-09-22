# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
<b>Hardware</b> – PCs, Cyclone II , USB flasher
<b>Software</b> – Quartus prime
<b>Theory</b> - Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.
```
Sum = A’B+AB’ =A ⊕ B Carry = AB
```
### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.
```
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
```
#### Figure -01 HALF ADDER 

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -02 FULL ADDER 

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)


### Procedure
-> Connect the supply (+5V) to the circuit
-> Switch ON the main switch
-> If the output is 1, then the led glows.
### Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: G Venkata Pavan Kumar
RegisterNumber: 212221240013
```
### Half Adder
```
module ex3(A,B,S,C);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
### Full Adder
```
module ex3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
### Logic symbols:

#### Half Adder:
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/e021188a-9999-40d7-a75a-2571ab54b5f9)
#### Full Adder:
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/97e5c831-67dc-427a-a5bf-312b3e58f29c)

### TruthTables:
#### Half Adder:
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/8fcdb646-1da8-49e9-bf8c-2316f6363f3e)
### Full Adder:
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/515989c5-ebba-499b-8a18-e2229ffd10d5)
### Output:
### RTL
#### Half Adder:
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/59c468a4-0441-4567-a9a2-00ee1a444893)
### Full Adder
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/95377b83-bee9-427c-8b65-2c58b975e6a6)

### TIMING DIAGRAM:
#### Half Adder:
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/ee39b01e-e054-42d1-a864-41a242600fa6)
#### Full Adder:
![image](https://github.com/Pavan-Gv/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/94827772/d95c9c27-78ea-45e7-bec8-f4385617e76a)

### Result:
Thus the given logic functions are implemented using half adder and full adder with their operations are verified using Verilog programming.
