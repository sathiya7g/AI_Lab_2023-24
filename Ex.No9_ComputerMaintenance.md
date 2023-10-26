# Ex.No: 9  Logic Programming –  Computer Maintenance Expert System
### DATE: 26/10/23                                                                           
### REGISTER NUMBER : 212221220049
### AIM: 
Write a Prolog program to build a computer maintenance expert system.
###  Algorithm:
1. Start the program.
2. Write the rules for each fault in computer.
3. If system have printing problem, missing dots and no uniform printing then system fault on printer head.
4. If system have not printing, missing dots and spread inks then system fault on ribbon
5. If system have not printing, paper jam and out of paper then system fault on paper stuck in printer
6. Similarly define rules for all faults.
7. Define facts for system problems.
8. Find the fault of computer by passing query to system.
     
### Program:


% Define components and issues
component(cpu).
component(memory).
component(hard_drive).
component(graphics_card).
component(power_supply).

issue(no_power, [power_supply]).
issue(blue_screen, [memory, graphics_card]).
issue(system_slow, [hard_drive, memory]).
issue(fan_noise, [cpu]).
issue(no_display, [graphics_card]).

% Define rules for diagnosis
diagnose_issue(Issue, Components) :-
    issue(Issue, RequiredComponents),
    subset(RequiredComponents, Components).

% Subset predicate to check if one list is a subset of another
subset([], _).
subset([H|T], List) :-
    member(H, List),
    subset(T, List).








### Output:
![image](https://github.com/sathiya7g/AI_Lab_2023-24/blob/main/Screenshot%202023-10-26%20004026.png)


### Result:
Thus the simple omputer maintenance expert system was built sucessfully.
