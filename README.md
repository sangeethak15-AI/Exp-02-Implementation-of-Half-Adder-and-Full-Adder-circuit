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

1. Connect the supply (+5V) to the circuit
2. Switch ON the main switch
3. If the output is 1, then the led glows.
### 
Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Sangeetha K
RegisterNumber: 212221230085

HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

Logic symbol & Truthtable
RTL realization

## Output:
## Half Adder :
### Logic symbol:
![halfgate](https://user-images.githubusercontent.com/93992063/165713952-acff3f6c-c52e-41fe-8477-2d062670d495.png)
### RTL Realization:
![hrtl](https://user-images.githubusercontent.com/93992063/165714105-f0ffff04-cd7b-427c-8b23-d662eacf18b5.png)
### Truthtable:
![haddtable](https://user-images.githubusercontent.com/93992063/165714174-db40c4dc-b6a8-431b-9bba-28009639947a.png)
### Timing Diagram:
![htiming](https://user-images.githubusercontent.com/93992063/165714220-b4beccac-9c13-4517-ae28-5e4fc7b71094.png)

## Full Adder :
### Logic Symbol:
![fullgate](https://user-images.githubusercontent.com/93992063/165714344-ec69fee8-e776-4784-9e25-8853c3c5c5fe.png)
### RTL Realization:
![frtl](https://user-images.githubusercontent.com/93992063/165714399-182b20bf-61a0-4421-8a70-4d8b95c740ac.png)
### Truthtable:
![faddtable](https://user-images.githubusercontent.com/93992063/165714523-a873952f-7e80-485d-a0db-16411bfe4394.png)
### Timing Diagram:
![ftiming](https://user-images.githubusercontent.com/93992063/165714611-6d8b7c4f-de91-4bd5-9e66-2e9ee16ddd1e.png)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
