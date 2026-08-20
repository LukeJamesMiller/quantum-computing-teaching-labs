$\huge{\textbf{Mathematics Review for Quantum Computing}}$
# Session Overview


## Objective: 
Review linear algebra and probability concepts essential for quantum computing
## Agenda:
- Importance of mathematical foundations
- Linear algebra: Vectors, matrices, and operations
- Tensor products and Dirac notation
- Probability basics for quantum mechanics
- Practice problems
- Q&A and course expectations

---

# Why Mathematics for Quantum Computing?

## Role in Course: 
Quantum computing relies on linear algebra for state representation and probability for measurement outcomes
## Prerequisites Recap: 
Linear Algebra, Calculus, Python (from course outline)
## Key Areas:
### Linear Algebra: 
Qubits, gates, circuits
### Probability: 
Measurement, uncertainty in quantum AI


## Connection to AI: 
Mathematical tools underpin quantum algorithms (e.g., QSVM, QNN)
## Question: 
Which math topic feels most unfamiliar?

---

# Linear Algebra: Vectors and Hilbert Spaces

## Vectors:
- Elements in ( $\mathbb{C}^n$ ), e.g., ( $|v\rangle = \begin{bmatrix} v_1 \ v_2 \ \vdots \ v_n \end{bmatrix}$ )
- Qubit: ( $|ψ\rangle = \alpha|0\rangle + \beta|1\rangle$ ), where ( $\alpha, \beta \in \mathbb{C}$ ), ( $|\alpha|^2 + |\beta|^2 = 1$ )


- Hilbert Space: Complex vector space with inner product
- Inner product: ( $\langle u | v \rangle = u^\dagger v = \sum_i u_i^* v_i$ )
- Norm: ( $|v| = \sqrt{\langle v | v \rangle}$ )


- Basis: Orthonormal vectors, e.g., ( $|0\rangle = \begin{bmatrix} 1 \ 0 \end{bmatrix}$ ), ( $|1\rangle = \begin{bmatrix} 0 \ 1 \end{bmatrix}$ )
- AI Use: Vectors represent quantum states for feature encoding


---

# Linear Algebra: Matrices

## Matrices: 
Linear operators on vectors, e.g., ( $A: \mathbb{C}^n \to \mathbb{C}^n$ )
### Key Properties:
- Hermitian: ( $A^\dagger = A$ ), e.g., Pauli matrices ( $X = \begin{bmatrix} 0 & 1 \ 1 & 0 \end{bmatrix}$ ), ( $Z = \begin{bmatrix} 1 & 0 \ 0 & -1 \end{bmatrix}$ )
- Unitary: ( $U^\dagger U = I$ ), preserves norms (quantum gates)
- Eigenvalues/vectors: ( $A|v\rangle = \lambda |v\rangle$ )


## Matrix Operations: 
- Addition, multiplication, conjugate transpose (( $A^\dagger$ ))
- AI Context: Matrices represent quantum gates, Hamiltonians in VQE


---

# Tensor Products

- Definition: Combines vector spaces for multi-qubit systems
- Single Qubit: ( $|ψ\rangle = \alpha|0\rangle + \beta|1\rangle$ )
- Two Qubits: ( $|ψ_1\rangle \otimes |ψ_2\rangle$ ), dimension ( $2 \times 2 = 4$ )
- Example: ( $|0\rangle \otimes |1\rangle = \begin{bmatrix} 1 \ 0 \end{bmatrix} \otimes \begin{bmatrix} 0 \ 1 \end{bmatrix} = \begin{bmatrix} 0 \ 1 \ 0 \ 0 \end{bmatrix} = |01\rangle$ )


## Matrix Tensor Product: 
For ( $A$ ), ($ B$ ), ( $A \otimes B$ ) applies to respective qubits
- Example: 
$$
( X \otimes I = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} \otimes \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \\ 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \end{bmatrix} )
$$

---

# Dirac Notation and Outer Product

## Dirac Notation:
- Ket: ( $|v\rangle$ ), vector in Hilbert space
- Bra: ( $\langle v|$ = ($v^\dagger$) ), conjugate transpose
- Inner product: ( $\langle u | v \rangle$ )
- Outer Product: ( $|u\rangle \langle v|$ ), matrix mapping ( $|w\rangle \to \langle v | w \rangle |u\rangle$ )
- Example: ( $|0\rangle \langle 1| = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \begin{bmatrix} 0 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$ )


- Properties: ( ($|u\rangle \langle v|)^\dagger = |v\rangle \langle u|$ )
- Applications: Density matrices (( $\rho = \sum p_i |ψ_i\rangle \langle ψ_i|$ )), projectors in QPE
- AI Context: Represents quantum states in QNNs, kernels

---

# Probability Basics for Quantum Mechanics

## Classical Probability:
- Events with probabilities ( $p_i$ ), ( $\sum p_i = 1$ )
- Expectation: ( $E[X] = \sum x_i p_i$ )


## Quantum Probability:
= Measurement outcomes: Probabilities from amplitudes, e.g., ( $P(|0\rangle) = |\alpha|^2$ )
- Density Matrix: ( $\rho$ ), probability via ( $P(i) = \langle i | \rho | i \rangle$ )
- Expectation: ( $\langle A \rangle = \text{Tr}(A \rho)$ )


- Born Rule: Probability of outcome ( $|i\rangle$ ) is ( $|\langle i | ψ \rangle|^2$ )
- AI Use: Measurement outcomes in QML, e.g., QSVM predictions

---

# Probability and Quantum Measurements

## Measurement Operators: 
Projectors ( $P_i = |i\rangle \langle i|$ )
- Example: Measure in computational basis, ( $P_0 = |0\rangle \langle 0|$ )


## Expectation Value: 
For observable ( $A$ ), ( $\langle A \rangle = \langle ψ | A | ψ \rangle$ )
- Example: Pauli-Z on ( $|ψ\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) )
( \langle Z \rangle = \langle ψ | \begin{bmatrix} 1 & 0 \ 0 & -1 \end{bmatrix} | ψ \rangle = 0$ )


- Uncertainty: Variance ( $\Delta A = \sqrt{\langle A^2 \rangle - \langle A \rangle^2}$ )
- AI Relevance: Probabilistic outcomes in QNN, quantum Bayes

---

# Practice Problem 1: Vector Operations

## Problem: 
For ( $|ψ\rangle = \frac{1}{\sqrt{2}}(|0\rangle + i|1\rangle)$ ), compute norm and ( $\langle Z \rangle$ )
## Solution:
- Norm: ( $|ψ| = \sqrt{\langle ψ | ψ \rangle} = \sqrt{\frac{1}{2} \cdot 1 + \frac{1}{2} \cdot 1} = 1$ )
- ($ \langle Z \rangle = \langle ψ | Z | ψ \rangle = \frac{1}{2} \begin{bmatrix} 1 & -i \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix} \begin{bmatrix} 1 \\ i \end{bmatrix} = 0$ )


- Question: What does ( \langle Z \rangle = 0 ) imply for measurement?
- AI Use: State preparation in feature encoding

---

# Practice Problem 2: Tensor Product

## Problem: 
Compute ( $|ψ\rangle = |0\rangle \otimes \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$ ) and apply ( $X \otimes I$ )
## Solution:
- ( $|ψ\rangle = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \otimes \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \\ 0 \\ 0 \end{bmatrix} $)
- ( $X \otimes I = \begin{bmatrix} 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \\ 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \end{bmatrix}$ )
- Result: ( $\frac{1}{\sqrt{2}} \begin{bmatrix} 0 \\ 0 \\ 1 \\ 1 \end{bmatrix} = \frac{1}{\sqrt{2}}(|10\rangle + |11\rangle) $)


- AI Context: Multi-qubit encoding for QSVM

---

# Practice Problem 3: Outer Product

## Problem: 
Compute ( $|0\rangle \langle 1|$ ) and apply to ( $|ψ\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$ )
## Solution:
- ( $|0\rangle \langle 1| = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \begin{bmatrix} 0 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$ )
- ( $|0\rangle \langle 1| |ψ\rangle = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 0 \end{bmatrix} = \frac{1}{\sqrt{2}} |0\rangle$ )


- Question: What’s the physical meaning of this operation?
- AI Use: Projectors in quantum kernels

---

# Practice Problem 4: Probability

## Problem: 
For ( $|ψ\rangle = \frac{\sqrt{3}}{2}|0\rangle + \frac{1}{2}|1\rangle$ ), compute probabilities and ( $\langle X \rangle$ )
## Solution:
- Probabilities: ( $P(|0\rangle) = \left|\frac{\sqrt{3}}{2}\right|^2 = \frac{3}{4}$ ), ( $P(|1\rangle) = \left|\frac{1}{2}\right|^2 = \frac{1}{4}$ )
- ( $\langle X \rangle = \langle ψ | \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} | ψ \rangle = \frac{\sqrt{3}}{2} \cdot \frac{1}{2} + \frac{1}{2} \cdot \frac{\sqrt{3}}{2} = \frac{\sqrt{3}}{2} \approx 0.866 $)


- AI Context: Probabilities in QNN outputs

---

# Course Expectations

## Math in Course:
- Sessions 1-3: Use vectors, tensor products for qubits, gates
- Sessions 4-7: Matrices for algorithms (QPE, Shor’s)
- Sessions 9-21: Probabilities, expectations in QML


## Resources:
- Linear Algebra: Strang’s “Introduction to Linear Algebra”
- Probability: Ross’s “First Course in Probability”
- Quantum Math: Nielsen & Chuang Ch. 2


## Python Practice: 
NumPy for vectors/matrices; Qiskit for quantum states
# Homework 0: 
Includes math exercises to reinforce concepts

