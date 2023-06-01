# quantum-project1

 (Established under the Presidency University Act, 2013 of the Karnataka Act 41 of 2013)
DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING CSE3008 QUANTUM COMPUTING (SECTION : 6CAI01)
Mini - Project Report Submitted by
RITU NAIK
GANNE SREYA CHAITANYA LAKSHMI ANANYA J SHETTY VARSHA J
KHUSHI K KOTIAN
20211LCA0001 20201CAI0010
20201CAI0025 20201CAI0031 20201CAI0046
20201CAI0048
In partial fulfillment for the requirement of 6th Semester
CSE3008 QUANTUM COMPUTING Under the Guidance of
Dr. Jayakumar Vaithiyashankar
𝐈𝐁𝐌 Quantum Educator & Qiskit Advocate Mentor and Developer Senior IEEE Member
PRESIDENCY UNIVERSITY
Academic Year 2022 - 2023

Topic :
4. More theoretical :
If you preferred the mathematical side of things:
1. Work out how many times Grover’s algorithm needs to query the oracle if there are multiple solutions. Write up your working as a short blog post.
2. Write an introduction to “math for quantum computing”. Research the maths needed to read other quantum computing textbooks and build a guide for new learners.
3. Investigate how you would combine schrodinger’s algorithm with Grover’s algorithm. What would a circuit for this look like? Are there any potential problems?
1. Work out how many times Grover’s algorithm needs to query the oracle if there are multiple solutions. Write up your working as a short blog post.
Grover’s Algorithm: Querying Multiple Solutions
Grover's algorithm, proposed by Lov Grover in 1996, is a quantum algorithm that offers a significant speedup for searching unstructured databases. It leverages the principles of quantum superposition and interference to efficiently locate a desired solution in a large solution space. Originally designed to find a single solution, Grover's algorithm can also be adapted to handle scenarios where multiple solutions exist. In this blog post, we will explore how Grover's algorithm can be applied to query an oracle when multiple solutions are present.
Grover's Algorithm: A Brief Overview:
    
Grover's algorithm is a quantum algorithm that provides a
quadratic speedup over classical algorithms for searching unsorted databases. It is particularly useful in situations where the search space is large and the desired solution is unknown. The algorithm employs a combination of quantum superposition and interference to iteratively narrow down the search space until the solution is found.
The algorithm starts by creating an equal superposition of all possible states using the Hadamard transform. Then, an oracle is applied to mark the target solution(s) in the superposition. The oracle is essentially a black box that evaluates whether a given state is a solution or not. Following the oracle, a reflection operator is applied, which amplifies the amplitude of the marked solutionwhile suppressing the amplitudes of other states. This process is repeated iteratively to increase the probability of measuring the correct solution.
Grover's algorithm is a powerful quantum algorithm that provides a quadratic speedup over classical search algorithms. Originally designed for finding a single solution, it can be adapted to handle scenarios with multiple solutions by adjusting the number of iterations required. By leveraging quantum superposition and interference, Grover's algorithm offers a more efficient approach to querying an oracle and identifying multiple solutions within a large solution space. As quantum computing continues to advance, Grover's algorithm holds immense potential for various applications in fields such as optimization, machine learning, and cryptography.
Finding Multiple Solutions:
In the original formulation, Grover's algorithm is designed to find a single solution. However, with slight modifications, it can be adapted to handle situations where multiple solutions exist. The general

approach involves adjusting the amplitude amplification step to account for the presence of multiple marked solutions.
To find multiple solutions, we need to define the number of marked solutions, denoted as M. Instead of performing the usual √N iterations, the number of iterations required to find multiple solutions can be approximated as approximately √(N/M). This adjustment ensures that the algorithm amplifies the probability amplitudes of the marked solutions proportionally to their occurrence in the search space.
By applying this modified version of Grover's algorithm, we can efficiently query the oracle and identify all the desired solutions in a time complexity that is significantly faster than classical methods.
Setting up the Problem:
Let's consider a scenario where we have a search space with N elements, and within this search space, there are M marked solutions that we want to identify using Grover's algorithm. The task is to determine the number of iterations required to query the oracle and find all the marked solutions efficiently.
Solution:
In Grover's algorithm, the number of iterations required to find a single solution is approximately √N. However, when we have multiple solutions, the algorithm needs to be adjusted to account for the presence of M marked solutions.
To find multiple solutions, we need to modify the amplitude amplification step of Grover's algorithm. The number of iterations required to find multiple solutions can be approximated as approximately √(N/M). This adjustment ensures that the algorithm

amplifies the probability amplitudes of the marked solutions proportionally to their occurrence in the search space.
By increasing the number of marked solutions (M), the number of iterations needed to query the oracle and find all the solutions decreases. When the number of marked solutions is close to the total number of elements (M ≈ N), the algorithm converges to approximately √(N/N) = 1 iteration, which implies that only one iteration is needed to find all the solutions.
On the other hand, when the number of marked solutions is relatively small (M << N), the algorithm still provides a substantial speedup compared to classical search algorithms. However, the number of iterations required to find all the solutions may be higher than in the case of a single solution.
It's important to note that the approximation of the number of iterations (√(N/M)) assumes an ideal scenario. In practice, the number of iterations needed may vary depending on factors such as the quality of the oracle, the size of the search space, and the level of precision required.
When applying Grover's algorithm to a scenario with multiple solutions, the number of iterations required to query the oracle and find all the solutions can be approximated as approximately √(N/M), where N represents the total number of elements in the search space, and M represents the number of marked solutions. This adjustment ensures that the algorithm amplifies the probability amplitudes of the marked solutions proportionally to their occurrence in the search space. Grover's algorithm provides a significant speedup compared to classical search algorithms, even when multiple solutions exist within the search space. As quantum computing continues to advance, Grover's algorithm holds

tremendous potential for solving complex search problems efficiently.
Calculating the Number of Queries:
To determine the number of queries or iterations required by Grover's algorithm when there are multiple solutions, we can use the formula √(N/M), where N represents the total number of elements in the search space, and M represents the number of marked solutions. Let's walk through an example to illustrate the calculation.
Example:
Suppose we have a search space with N = 100 elements, and there are M = 10 marked solutions within this search space. We want to find all the marked solutions using Grover's algorithm.
Using the formula √(N/M), we can calculate the number of iterations or queries needed:
√(N/M) = √(100/10) = √10 ≈ 3.16
Since the number of iterations cannot be a fraction, we round up to the nearest integer. Therefore, the algorithm would require approximately 4 iterations or queries to find all the marked solutions in this example.
It's important to note that the formula provides an approximation, and the actual number of iterations may vary based on factors such as the quality of the oracle and the level of precision required. Additionally, if the number of marked solutions is close to the total number of elements (M ≈ N), the algorithm may converge to only 1 iteration, as mentioned in the previous section.

Suppose we have a problem with N = 64 possible solutions, and we
know that k = 4 of them are marked solutions. Let's calculate the number of queries required by Grover's algorithm:
Iterations = π√(N/(2k))
Iterations = π√(64/(2*4))
Iterations = π√(64/8)
Iterations = π√8
Iterations ≈ 4.44
Therefore, in this scenario, Grover's algorithm would need approximately 4.44 iterations, which is not a whole number since
the formula provides an estimation
By using the formula √(N/M), we can estimate the number of iterations or queries required by Grover's algorithm when there are multiple solutions. This calculation provides a rough approximation of the time complexity of the algorithm in such scenarios. However, it's important to consider other factors and variations that may affect the actual number of iterations, such as the quality of the oracle and the specific characteristics of the problem at hand. Grover's algorithm continues to be a valuable tool for efficiently searching unstructured databases, even in cases where multiple solutions need to be identified.
In the classical linear search algorithm, it becomes easier to find a solution as the number of solutions in the database increases. In Grover's algorithm this is not true.
Let us visualize the Grover's iterations (yes, I had simulated it sometime back). Note that after 'k' number of steps, the probability amplitude would have been divided equally among all possible

solutions. Subsequent measurement of the system would still have yielded the solution, but with a lower probability. More the number of solutions, lesser is the maximum value of the probability amplitudes of each solution.

  

If you are not convinced yet, let us look at it mathematically.
Recall that the angle by which the quantum state is rotated as a result of Grover's operation is given by:
𝜃=𝑠𝑖𝑛−1(2√𝑀(𝑁−𝑀)/𝑁)
My calculations say that if M=N/2, then
𝜃=𝜋/2
, and if M=N, then
𝜃=0 .
It can be concluded that
𝜃
gets smaller as M varies from N/2 to N, meaning that it gets closer to the superposition of all the elements which do not satisfy the quantum oracle!
Irony is that the number of iterations needed by the quantum search algorithm increases with 𝑀≥𝑁/2
, much unlike its classical analogue. There are two simple ways to troubleshoot this problem:
• Use random brute force to pick a random element from the database, and check if it is the solution using the quantum oracle. There is a good chance of picking up
a solution if we are lucky, since the number of solutions is more than half the size of the database.
• Add extra N dummy items in the search space such that no dummy item is a solution. As a consequence, less than half of

the items will be solutions in the new search space. In this case, we must form a new augmented oracle for our search problem. I will not go into the details of that since it is outside the scope of your question.
2. Write an introduction to “math for quantum computing”. Research the maths needed to read other quantum computing textbooks and build a guide for new learners.
Introduction to Math for Quantum Computing
Quantum computing is an emerging field at the intersection of mathematics, physics, and computer science, promising to revolutionize various industries and transform the way we process information. Understanding quantum computing requires a solid foundation in mathematics, as it relies heavily on mathematical concepts and principles.
This guide aims to provide an overview of the mathematical prerequisites for studying quantum computing. Whether you are a beginner with little mathematical background or an experienced mathematician looking to delve into quantum computing, this guide will equip you with the necessary mathematical tools to read other quantum computing textbooks and navigate the intricacies of this fascinating field.
To embark on the journey of learning quantum computing, one must have a solid understanding of linear algebra, calculus, and probability theory. These branches of mathematics form the backbone of quantum mechanics, the underlying theory behind quantum computing.
Linear algebra plays a central role in quantum computing, as quantum states are represented by vectors in a complex vector space known as a Hilbert space. Concepts such as vector spaces, matrices, eigenvectors, and eigenvalues are
   
fundamental to understanding the quantum state, quantum gates, and quantum operations.
Calculus is crucial for comprehending the dynamics and evolution of quantum systems. Differential calculus helps us describe the time evolution of quantum states, while integral calculus enables us to compute quantities like probabilities and expectation values.
Probability theory provides the mathematical framework to analyze and predict the outcomes of quantum measurements. Quantum mechanics introduces probabilistic phenomena, and understanding concepts like probability distributions, conditional probabilities, and statistical ensembles is essential for working with quantum systems.
In addition to these foundational topics, knowledge of other mathematical areas such as graph theory, complex analysis, and information theory can be advantageous for a deeper understanding of advanced quantum computing concepts. However, they are not necessarily prerequisites and can be explored as the need arises during your journey into quantum computing.
This guide will provide an accessible introduction to these mathematical concepts, explaining their relevance to quantum computing and providing examples and exercises to reinforce your understanding. With a firm grasp of the necessary mathematics, you will be well-equipped to dive into quantum computing textbooks and explore the exciting and rapidly evolving field of quantum computing.
Get ready to unlock the mysteries of quantum information processing and embark on a fascinating mathematical journey that will empower you to tackle the challenges and opportunities of quantum computing.
To build a guide for new learners on math for quantum computing, we can structure it into several key sections that progressively introduce the necessary mathematical concepts. Here's a suggested outline for the guide:

1.Introduction to Linear Algebra:
• Vectors and vector spaces
• Matrices and matrix operations
• Eigenvalues and eigenvectors
• Inner product spaces
• Norms and orthogonality
2.Complex Numbers:
• Basics of complex numbers
• Complex conjugates and modulus
• Polar form and Euler's formula
• Complex vector spaces and operations
3.Probability Theory:
• Basicprobabilityconcepts
• Probabilitydistributions
• Conditional probability and Bayes' theorem
• Expected values and variance
• Random variables and their properties
4.Quantum Mechanics Essentials:
• Postulates of quantum mechanics
• Quantum states and wavefunctions
• Superposition and measurement
• Observablesandoperators
• The concept of a qubit
5.Quantum Gates and Quantum Circuits:
• Unitary matrices and their properties
• Quantum gates and their operations
• Composite systems and tensor products
• Quantum circuits and circuit representations
6.Quantum Measurement Theory:

• Measurement postulates in quantum mechanics
• Measurement operators and their properties
• Measurement outcomes and probabilities
• Measurement in different bases
Additional Advanced Topics:
• Quantum entanglement and Bell's inequality
• Quantum algorithms: Grover's algorithm and Shor's algorithm
• Quantum error correction and fault tolerance
• Quantumcomplexitytheory
• Quantum simulation and adiabatic quantum computing
Each section should include explanations of the relevant mathematical concepts, along with examples and exercises to reinforce understanding. It's important to strike a balance between providing clear explanations and delving into the necessary mathematical rigor without overwhelming beginners.
Additionally, visual aids such as diagrams, graphs, and illustrations can greatly enhance the learning experience and help learners visualize abstract concepts. Providing references to external resources, textbooks, and research papers can also encourage further exploration for those who want to deepen their knowledge.
Remember to emphasize the practical applications and significance of each mathematical concept in the context of quantum computing, as this can motivate learners and highlight the relevance of the mathematics they are studying.
By following this structured guide, new learners will gradually develop the mathematical foundation needed to read other quantum computing textbooks, research papers, and eventually contribute to the advancement of quantum computing itself.
The link for reference textbook for math quantum computing:

https://www.google.co.in/books/edition/Quantum_Computing/VdHJs TdoyAMC?hl=en&gbpv=1&dq=Quantum+Computing:+From+Linear +Algebra+to+Physical+Realizations%22+by+Mikio+Nakahara+and+ Tetsuo+Ohmi&printsec=frontcover
Mathematics plays a crucial role in various real-life applications of quantum computing. Here are a few examples:
Cryptography: Quantum computing has the potential to revolutionize cryptography by providing more secure encryption algorithms. Mathematics, particularly number theory and modular arithmetic, is fundamental to understanding cryptographic protocols such as RSA and elliptic curve cryptography. Developing and analyzing quantum-resistant encryption schemes heavily relies on mathematical concepts and algorithms.
Drug Discovery: Quantum computing can significantly speed up the process of drug discovery by simulating molecular interactions and properties. Quantum chemistry, which involves solving complex equations and approximations, relies on mathematical techniques such as linear algebra and calculus to model quantum systems accurately. The use of quantum algorithms for molecular simulation can potentially lead to the discovery of new drugs and materials.
Optimization Problems: Many real-world optimization problems, such as supply chain management, portfolio optimization, and scheduling, can be tackled more efficiently using quantum computing. Mathematical techniques, including linear programming, quadratic programming, and combinatorial optimization, are essential for formulating and solving these problems in the quantum domain. Quantum algorithms, such as the quantum approximate optimization algorithm (QAOA), leverage mathematical optimization techniques to find optimal solutions.
Machine Learning: Quantum machine learning combines concepts from quantum computing and classical machine learning to develop novel algorithms and models. Mathematical techniques such as

linear regression, matrix factorization, and optimization methods form the basis for traditional machine learning algorithms. Incorporating quantum computing into machine learning opens up new possibilities for solving complex problems, including pattern recognition, data clustering, and deep learning.
Financial Modeling: Quantitative finance relies heavily on mathematical models and algorithms to analyze and predict market behavior. Quantum computing has the potential to enhance financial modeling by enabling more accurate pricing of financial derivatives, portfolio optimization, and risk analysis. Mathematical techniques such as stochastic calculus, Monte Carlo simulations, and option pricing models are crucial components of quantum finance.
Supply Chain Optimization: Optimizing supply chains involves complex mathematical models and algorithms to minimize costs, improve efficiency, and optimize logistics. Quantum computing can help solve large-scale optimization problems related to supply chain management, such as inventory control, transportation planning, and facility location optimization. Mathematical techniques such as linear programming, network flow algorithms, and graph theory play a vital role in designing and optimizing supply chains using quantum computing.

3. Investigate how you would combine Schrodinger’s algorithm with Grover’s algorithm. What would a circuit for this look like? Are there any potential problems?
Schrodinger's Algorithm: A Brief Overview:
Schrodinger's algorithm is a quantum simulation algorithm that aims to simulate quantum systems efficiently. It focuses on superpositions of different paths to enhance the efficiency of solving computational problems. It involves using coherent superpositions of different computational paths to perform computations in parallel, potentially leading to exponential speedup compared to classical algorithms. It utilizes the notion of wavefunctions and evolves them over time using the Schrodinger equation.It was devised by Erwin Schrodinger.
The Schrodinger equation is a partial differential equation and looks like this:
Grover's Algorithm: A Brief Overview:
In Quantum computing,Grover’s algorithm,also known as the quantum search algorithm,refers to a quantum algorithm for unstructured search finds with high probability the unique input to black box function that produces a partcular output value,using just O(square root of N) evaluations of the function,where N is the siuze of the function’s domain.
It is particularly useful for the problems where the solution can be represented as binary string and the search space is unstructured.Grover's algorithm combines amplitude amplification and phase kickback to amplify the amplitude of the target state,
      
allowing for more efficient search.It was devised by Lov Grover in 1996.
How you would combine Schrodinger’s algorithm with Grover’s algorithm?
Combining Schrodinger's algorithm with Grover's algorithm
would likely involve utilizing the superposition and interference properties of Schrodinger's algorithm to enhance the amplitude amplification and phase kickback steps of Grover's algorithm.It would likely involve using the simulation capabilities of Schrodinger's algorithm to enhance the search capabilities of Grover's algorithm.
Let's consider a problem of searching for a specific state in a quantum system that evolves over time according to Schrodinger's equation. The goal is to find the state with a high probability by leveraging the principles of Grover's algorithm.
Here's a conceptual outline of how one could approach this problem:
1.Prepare the initial quantum state: Start by preparing an initial quantum state that represents the problem we want to solve. This can be done using quantum gates and algorithms specific to the problem. Let's assume we have a quantum circuit that prepares an initial superposition state.
2.Time evolution simulation: Utilize quantum gates and operations to simulate the time evolution of the quantum state based on Schrodinger's equation. This involves applying a unitary operator that represents the time evolution of the system. The specific circuit implementation would depend on the dynamics described by Schrodinger's equation for the particular system we are considering.
3.Measurement of the evolved state: After simulating the time evolution, perform a measurement on the quantum state to obtain

measurement outcomes. This measurement collapses the state into one of the possible measurement results.
4.Amplify the target state: If the measurement outcome does not correspond to the desired state, we can use Grover's algorithm to amplify the amplitude of the target state. This involves applying the Grover iteration, which consists of several iterations of applying specific quantum gates such as the oracle and the diffusion operator. The exact number of iterations would depend on the problem size and desired success probability.
5.Repeat steps 2 to 4: Depending on the problem and the obtained measurement outcomes, you may need to iterate steps 2 to 4 multiple times to increase the likelihood of finding the desired state.
The specific circuit implementation would involve applying the necessary quantum gates and operations for time evolution simulation, measurement, and the application of Grover's algorithm. The exact structure and composition of the circuit would depend on the problem being solved, the dynamics described by Schrodinger's equation, and the available quantum resources.
Code :
import numpy as np
from qiskit import QuantumCircuit, Aer, execute
# Define the quantum state we want to find
desired_state = np.array([0, 0, 1]) / np.sqrt(2) # Example desired state: |011⟩
# Step 1: Apply Schrödinger's algorithm to simulate the time evolution
qc = QuantumCircuit(3, 3) # Create a 3-qubit quantum circuit initial_state = np.array([1, 0, 0, 0, 0, 0, 0, 0]) / np.sqrt(2) # Initial state: |000⟩
qc.initialize(initial_state, [0, 1, 2]) # Initialize the qubits qc.barrier()

# Apply gates and operations to simulate the time evolution
# (This part depends on the specific problem being solved) # Let's assume we apply some arbitrary gates and operations here qc.h(0) qc.cx(0, 1) qc.cx(0, 2) qc.barrier()
qc.draw()
# Step 2: Apply Grover's algorithm to search for the desired state iterations = 1 # Number of iterations for Grover's algorithm qc.h([0, 1, 2])
qc.barrier()
# Apply Grover's diffusion operator qc.x([0, 1, 2])
qc.h(2) qc.cx(0,
2) qc.h(2)
qc.x([0, 1, 2]) qc.h([0, 1, 2]) qc.barrier()
# Measure the qubits to obtain the final result qc.measure([0, 1, 2], [0, 1, 2])
# Execute the quantum circuit on a simulator simulator = Aer.get_backend('qasm_simulator') job = execute(qc, simulator, shots=1000)
result = job.result()
counts = result.get_counts()
# Print the measurement results print("Measurement results:") for state in counts:
print(state)
# Check if the desired state is found in the results if desired_state in counts:

print("Desired state found!") else: print("Desired state not found.")
Circuit will possibly look like this :
 Potential problems and challenges that could arise from combining the two algorithms :
1.Complexity and computational resources: Both Schrodinger's algorithm and Grover's algorithm require significant computational resources, especially as the size of the quantum system or the search space increases. Combining these algorithms could potentially amplify the computational requirements, making it challenging to implement on near-term quantum computers.
2.Interference and coherence: The combination of these algorithms could introduce additional interference and coherence challenges. Maintaining the coherence and minimizing the decoherence effects during the simulation and search process would be crucial to obtain meaningful results.
3.Lack of well-established circuit designs: Since Schrodinger's algorithm is not widely known or studied, there may not be established circuit designs available for combining it with Grover's algorithm. Developing new circuit designs and ensuring their correctness could be a significant challenge.
3.Compatibility: It is necessary to ensure that the individual algorithms being combined are compatible with each other. This

includes checking the input and output requirements, gate operations, and qubit resources needed for each algorithm. If there are conflicting requirements or dependencies, it may be challenging to merge them seamlessly.
4.Overlapping resources: Combining multiple algorithms may require a significant number of qubits and gates, leading to resource constraints. Quantum computers currently have limited qubit counts and gate fidelities, so combining complex algorithms could exceed the available resources and hinder successful execution.
5.Quantum noise and error correction: Quantum computers are inherently noisy, and errors can occur during quantum operations. Combining multiple algorithms increases the chance of errors and may make error correction more challenging. Implementing error correction codes, such as the surface code, could help mitigate these issues but comes with additional overhead in terms of qubit requirements and computational complexity.
6.Algorithm interference: Combining algorithms may introduce interference between different parts of the circuit, affecting the overall performance. Interference can arise due to incompatible gate sequences, overlapping qubit operations, or unwanted entanglement between qubits.
