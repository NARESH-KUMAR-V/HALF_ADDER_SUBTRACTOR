# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

Half adder:
![img 15](https://github.com/NARESH-KUMAR-V/HALF_ADDER_SUBTRACTOR/assets/145842937/45d11a54-0804-4f81-aa5d-0aae4e2dba79)

Half subtractor:
![img 16](https://github.com/NARESH-KUMAR-V/HALF_ADDER_SUBTRACTOR/assets/145842937/10105105-04c2-46a1-b4b0-7538fbfac195)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:Naresh Kumar V RegisterNumber:212223040126*/

half adder:
```
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
assign sum = a^b;
assign carry = a & b;
endmodule
```
half subtractor:
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
assign Bo = ~a & b;
endmodule
```

**RTL Schematic**
Half adder:
![img 17](https://github.com/NARESH-KUMAR-V/HALF_ADDER_SUBTRACTOR/assets/145842937/5dd64107-3327-4f79-98c8-a833f72357ee)

Half subtractor:
![img 18](https://github.com/NARESH-KUMAR-V/HALF_ADDER_SUBTRACTOR/assets/145842937/dbe8bd24-1d92-48b4-8368-0b6248b486eb)


**Output/TIMING Waveform**
Half adder:
![img 19](https://github.com/NARESH-KUMAR-V/HALF_ADDER_SUBTRACTOR/assets/145842937/33eb029e-8b15-4dcb-8b50-7829899ecea4)

Half subtractor:
![img 20](https://github.com/NARESH-KUMAR-V/HALF_ADDER_SUBTRACTOR/assets/145842937/188ae379-582d-4e82-859a-1a36e71c1c22)

**Result:**
Thus the program was successfully verified.
