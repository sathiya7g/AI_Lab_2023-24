# Ex.No: 8  Logic Programming –  Medical Diagnosis Expert System
### DATE:                                                                         
### REGISTER NUMBER : 212221220049
### AIM: 
Write a Prolog program to build a medical Diagnosis Expert System.
###  Algorithm:
1. Start the program.
2. Write the rules for each diseases.
3. If patient have mumps then symptoms are fever and swollen glands.
4. If patient have cough, sneeze and running nose then disease is measles.
5. if patient have symptoms headache ,sneezing ,sore_throat, runny_nose and  chills then disease is common cold.
6. Define rules for all disease.
7. Call the predicates and Collect the symptoms of Patient and give the hypothesis of disease.
        

### Program:


% Define symptoms and diseases
symptom(fever).
symptom(cough).
symptom(headache).
symptom(rash).
symptom(joint_pain).

disease(flu, [fever, cough, headache]).
disease(measles, [fever, cough, rash]).
disease(dengue, [fever, rash, joint_pain]).

% Define rules for diagnosis
diagnose(Disease, Symptoms) :-
    disease(Disease, DiseaseSymptoms),
    subset(DiseaseSymptoms, Symptoms).

% Subset predicate to check if one list is a subset of another
subset([], _).
subset([H|T], List) :-
    member(H, List),
    subset(T, List).








### Output:

![image](https://github.com/sathiya7g/AI_Lab_2023-24/blob/main/Screenshot%202023-10-26%20002614.png)

### Result:
Thus the simple medical diagnosis system was built sucessfully.
