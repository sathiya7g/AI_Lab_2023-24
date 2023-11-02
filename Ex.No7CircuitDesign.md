# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:                                                                         
### REGISTER NUMBER : 212221220049
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
% Define XOR gate
xor_gate(0, 0, 0).
xor_gate(0, 1, 1).
xor_gate(1, 0, 1).
xor_gate(1, 1, 0).

% Define AND gate
and_gate(0, 0, 0).
and_gate(0, 1, 0).
and_gate(1, 1, 1).
and_gate(1, 0, 0).

% Define OR gate
or_gate(0, 0, 0).
or_gate(0, 1, 1).
or_gate(1, 0, 1).
or_gate(1, 1, 1).

% Define half adder
half_adder(A, B, Sum, Cout) :-
    xor_gate(A, B, Sum),
    and_gate(A, B, Cout).

% Define half subtractor
half_subtractor(A, B, Diff, Bout) :-
    xor_gate(A, B, Diff),
    not_gate(B, B_not),
    and_gate(A, B_not, Bout).

% Define NOT gate
not_gate(0, 1).
not_gate(1, 0).


### Output:

![image](https://github.com/sathiya7g/AI_Lab_2023-24/blob/main/Screenshot%202023-10-20%20175357.png)


### Result:
Thus the truth table of circuit verified sucessfully.
