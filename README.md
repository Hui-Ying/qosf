# qosf
## Task 2
Prepare 4 random 4-qubit quantum states of your choice.
Create and train a variational circuit that transforms input states into predefined output states.   

Namely
- if random state 1 is provided, it returns state |0011>
- if random state 2 is provided, it returns state |0101>
- if random state 3 is provided, it returns state |1010>
- if random state 4 is provided, it returns state |1100>

## Experiment
In this task, a quantum variational circuit is desgined. In this model, there are 8 layers and each layer contain 4 Rot gates and 6 CNOT gates. The 6 CNOT gates are fully connected to each other.   

The loss function is designed as L = sum(abs(l - f)), where l is label and f is fidelity. 

