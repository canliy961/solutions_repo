# Problem 1
# Equivalent Resistance Using Graph Theory

## Introduction and Motivation

Calculating equivalent resistance is a fundamental task in electrical circuit analysis. Traditionally, this is done by simplifying series and parallel connections step by step. However, as circuits grow in complexity—with many nested or cyclic components—these methods become less efficient and prone to error.

By applying graph theory, we gain a structured and scalable approach to simplifying resistor networks. Each resistor is modeled as a weighted edge in a graph, and nodes represent circuit junctions. The total resistance between two terminals is then reduced algorithmically, leveraging insights from graph traversal and reduction.

This method is not only more efficient for computational tools but also provides a deeper understanding of the interconnectivity and structure within circuits.

## Learning Objectives

After completing this task, you should be able to:

- Represent a resistor network as a graph.
- Identify and reduce series and parallel resistor combinations using graph-based methods.
- Understand and implement a simplification algorithm that handles arbitrary circuit complexity.
- Apply the algorithm to both simple and complex circuit topologies.

## Theory Refresher

### Series Connection

If two resistors $R_1$ and $R_2$ are in series:

$$
R_{eq} = R_1 + R_2
$$

### Parallel Connection

If two resistors $R_1$ and $R_2$ are in parallel:

$$
\frac{1}{R_{eq}} = \frac{1}{R_1} + \frac{1}{R_2}
$$

or

$$
R_{eq} = \left( \frac{1}{R_1} + \frac{1}{R_2} \right)^{-1}
$$

Graph theory allows us to detect these configurations algorithmically and apply such reductions iteratively.

![alt text](image-4.png)

This plot includes:

- **6 resistors** with specified values (in $ \Omega $).
- **Clear node positions and labels** for all junctions.
- A **title** indicating it's **Step 1**.

![alt text](image-5.png)

This version:

- **Keeps all nodes visible** for clarity.
- **Highlights the new** $B \rightarrow \text{END}$ **path in red**.
- **Updates the resistance to** $4.24\,\Omega$  
  (resulting from the parallel combination of two paths: $4\,\Omega + 5\,\Omega$ and a direct $8\,\Omega$ connection).

![alt text](image-6.png)

**Why 7.24 Ω?**

This is the result of:

- $A \rightarrow B = 3\,\Omega$
- $B \rightarrow \text{END} \approx 4.24\,\Omega$ (from Step 2)

So:

$$
R_{A \rightarrow B \rightarrow \text{END}} = 3 + 4.24 = 7.24\,\Omega
$$

![alt text](image-7.png)

**Why 4.36 Ω?**

It results from the **parallel combination** of:

- $A \rightarrow \text{END} = 7.24\,\Omega$ (from Step 3)
- $A \rightarrow C \rightarrow \text{END} = 6 + 5 = 11\,\Omega$

Using the parallel formula:

$$
\frac{1}{R_{eq}} = \frac{1}{7.24} + \frac{1}{11} \approx 0.229
\quad \Rightarrow \quad
R_{eq} \approx 4.36\,\Omega
$$

## Task Description

### Choose One:

**Option 1: Simplified Task – Algorithm Description**

Describe a general-purpose algorithm that calculates equivalent resistance using graph-theoretical principles.

Include pseudocode for:

- Detecting series and parallel components.
- Iteratively simplifying the network.

Explain how your algorithm manages nested combinations (e.g., a parallel branch containing a series connection).

---

**Option 2: Advanced Task – Full Implementation**

Develop a full implementation in a language such as Python (recommended with `networkx`).

Your implementation must:

- Accept a circuit graph as input.
- Handle:
  - Series and parallel connections.
  - Nested and cyclic structures.
- Output the equivalent resistance between any two terminals.

## Expected Deliverables

- Pseudocode and/or working code.
- Step-by-step walkthrough of 3 sample circuits:
  - Pure series
  - Pure parallel
  - Complex nested configuration
- Discussion of:
  - Algorithm correctness
  - Efficiency
  - Potential enhancements (e.g., use of disjoint-set structures or symbolic resistance handling)

## Helpful Hints

- Use graphs: Nodes = junctions, edges = resistors (with resistance as weight).
- Use traversal: Use DFS or BFS to detect series chains or parallel branches.
- Iterate reduction: Collapse detected subgraphs until one equivalent edge remains.
- Check for cycles: Useful for identifying parallel paths.
- Libraries like `networkx` can significantly speed up development.

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

🔹 **Step 1: Initial Configuration**  
Multiple paths from **START** to **END** via nodes **A**, **B**, and **C**.  
Resistors span various branches of the graph.

🔹 **Step 2: Identify Parallel Paths**  
Focus on paths:  
- $\text{START} \rightarrow A \rightarrow C$  
- $\text{START} \rightarrow B \rightarrow C$  

These converge at node $C$, forming a **parallel configuration**.

🔹 **Step 3: Combine to Simplified Path**  
Combine the two paths into **one equivalent resistor** between $\text{START}$ and $C$.  
Then include the resistor from $C$ to $\text{END}$.

🔹 **Step 4: Final Equivalent Resistance**  
Network simplified into a **single edge** between $\text{START}$ and $\text{END}$.  

**Total equivalent resistance** $\approx 10.2\,\Omega$

## My Colab (Canliy961)

[Equivalent Resistance](https://colab.research.google.com/drive/1WQOjRSSeJFwXCIz9FGuK2AYQrQzfH3Tc#scrollTo=aX2vbhOwus2n)
