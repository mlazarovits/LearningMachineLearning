---
title: "7/17/19 Paper Discussion: Quantum Machine Learning"
---

We discussed the paper [Quantum Machine Learning]("assets/papers_summer19/quantum_ML.pdf") by Jacob Biamonte, et. al. Ryan and Ty led our discussion, which mainly focused on the feasibility of quantum computation. This paper is a survey of current state of quantum machine learning. It addresses the feasability of quantum machine learning and potential applications as well as pitfalls. According to Quantum Machine Learning, most of the quantum computation applications focus on linear algebra operations, like Fourier transforms, finding eigenvectors/eigenvalues and solving linear sets of equations. This paper dives in on this last application, which uses the HHL algorithm to solve sets of equations. It takes the HHL algorithm as an example of how quantum computing can speed up operations. Classical computers take O(NlogN) steps to solve the HHL algorithm while quantum computers take O((logN)^2) steps.

While computational speed-up is one advantage of quantum computers, an issue with employing machine learning algorithms with quantum computers is the input/output problem. Quantum computers must take in quantum states as inputs, where classical computers take in vectors. These are two of the "four fundamental problems" discussed towards the end of the paper. The authors assert taht "while quantum algorithms can provide dramatic speedups for processing data they seldom provide advantages for reading data." The same goes for learning the quantum solution that is output by the algorithm. This issue of reading data can often dominate the cost of quantum algorithms. We discussed some potential remedies to these problems. One point that Ty brought up was that the expectation value of the quantum output of the algorithm could be taken to map the quantum output to a classical one. Another way we could potentially minimize the high cost of reading quantum output is to apply the quantum algorithm to a classification problem with only 2 categories. However, this would leave a whole area of machine learning, regression or fitting, to be determined.

While the majority of our conversation focused on the technical aspects of quantum computing and the applications/issues with the field, it is important to discuss these points to understand further applications of quantum machine learning.