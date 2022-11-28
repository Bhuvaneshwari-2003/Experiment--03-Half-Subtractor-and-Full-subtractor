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



Write the detailed procedure here 


Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:bhuvaneshwari.s
RegisterNumber:212221240010
*/
Half subtractor:
module full(output D,B,input x,y,z);
assign D = x^y;Full Subtractor:
assign B = (~x&y);
endmodule

Full Subtractor:
module full(output D,B,input x,y,z);
assign D = x^y^z;
assign B = (~x&(y^z)|(yz));
endmodule

Output:
Truthtable:
Half subtractor:
![192110132-2833496f-c1b0-449b-9f7e-f5348e2446d0](https://user-images.githubusercontent.com/94828604/204279912-241a030b-f50c-4d25-8239-ecc1018df92b.png)

Fulll Subtrctor:
![192110146-f9641772-a09b-4bbe-b837-aaa5d0412831](https://user-images.githubusercontent.com/94828604/204280075-a1e6830d-f9a2-48ff-a445-65305852fcfd.png)





RTL realization:
Half Subtractor:
![192109682-ba1d7669-e1a6-49fb-8977-e1dce0c08a4c](https://user-images.githubusercontent.com/94828604/204280433-c2bfd3a3-2c86-4fce-85a0-7c5de040591f.png)
Full Subtractor:





Timing diagram:
Half Subtractor:
Full subtractor:
![Uploading 192109854-d996f376-b862-40f1-be84-61c9f0912984.png…]()



Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
