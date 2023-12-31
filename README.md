# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
STEP 1: Use module project name(input,output) to start the Verilog programmming.

STEP 2: Assign inputs and outputs using the word input and output respectively.

STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

STEP 4: Use each output to represnt onre for differnce and the other for borrow.

STEP 5: End the verilog program using keyword endmodule.


Write the detailed procedure here 


## Program:
Half Subtractor:
module halfsub(a,b,Diff,Borrow);
input a,b;
output Diff,Borrow;
assign Diff = (a^b);
assign Borrow = (~a&b);
endmodule
Full Subtractor:
module fullsub(A,B,Bin,diff,borrow);
input A,B,Bin;
output diff,borrow;
assign diff=(A^B^Bin);
assign borrow=((~A&B)|(~(A^B)&Bin));
endmodule

/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: ARJUNSHA NR
RegisterNumber:212223050007  
*/

## Output:

## Truthtable
Half Subtractor:
![image](https://github.com/nrarjun2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155224066/fce47438-0590-450e-8104-aa11d3a4251c)

Full Subtractor:
![image](https://github.com/nrarjun2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155224066/3cd6d6a0-fb37-42f7-bda0-f6cd2be48fa0)


##  RTL realization
Half Subtractor:
![image](https://github.com/nrarjun2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155224066/95795cbb-f8c6-4369-a071-01a15df61b07)

Full Subtractor:
![image](https://github.com/nrarjun2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155224066/efcfb275-2762-410b-a23a-7f70034cccc4)

## Timing diagram 
Half Subtractor:
![image](https://github.com/nrarjun2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155224066/86cf8d1a-f562-41a6-909c-58a3a710f569)

Full Subtractor:
![image](https://github.com/nrarjun2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155224066/078ba228-2acc-4d55-85fc-27b02dc1124f)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
