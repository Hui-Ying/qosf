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
The code is implemented using Pennylane.
In this task, a quantum variational circuit is desgined. In this model, there are 8 layers and each layer contain 4 Rot gates and 6 CNOT gates. The 6 CNOT gates are fully connected to each other.   

The loss function is designed as L = sum(abs(l - f)), where l is label and f is fidelity. We use the absolute loss function to rapidly converge the loss.

The batch size of the dataset is 8. 

If the radom input states are [1, 1, 1, 0], [0, 1, 1, 0], [1, 0, 0, 1], [1, 0, 1, 0], the average fidelity for the outputs given by the task is 91%. 
