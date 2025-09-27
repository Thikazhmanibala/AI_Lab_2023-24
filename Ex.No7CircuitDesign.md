# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 29/09/25                                                                        
### REGISTER NUMBER : 212222060277
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.
### Program:
xor(0,1,1).

xor(0,0,0).

xor(1,0,1).

xor(1,1,0).

and(1,1,1).

and(0,0,0).

and(0,1,0).

and(1,0,0).

not(0,1).

not(1,0).

or(0,1,1).

or(1,0,1).

or(0,0,0).

or(1,1,1).

halfadder(A,B,Sum,Carry):-

    xor(A,B,Sum),
    
    and(A,B,Carry).
    
halfsubtractor(A,B,Diff,Carry):-

    xor(A,B,Diff),
    
    not(A,C),
    
     and(C,B,Carry).
     
fulladder(A,B,Cin,S,Cout):-

    xor(A,B,X),
    
    xor(X,Cin,S),
    
    and(X,Cin,Y),
    
    and(A,B,Z),
    
    or(Y,Z,Cout).

### Output:

<img width="923" height="311" alt="Screenshot 2025-09-27 091508" src="https://github.com/user-attachments/assets/5576deab-6fad-4705-910e-2dc6a842f5a4" />

<img width="919" height="313" alt="Screenshot 2025-09-27 091617" src="https://github.com/user-attachments/assets/fdaadcbd-a1fa-4279-b427-ee616fc55776" />

<img width="915" height="321" alt="Screenshot 2025-09-27 091646" src="https://github.com/user-attachments/assets/c0a6ad49-037a-4541-891f-5d94c7b75d13" />


### Result:
Thus the truth table of circuit verified sucessfully.
