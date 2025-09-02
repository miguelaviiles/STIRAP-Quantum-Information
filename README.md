# STIRAP: Stimulated Raman Adiabatic Passage

This project explores **Stimulated Raman Adiabatic Passage (STIRAP)**, a powerful technique to transfer population between quantum states in a three-level lambda system. It was developed as part of my *Physics of Data* master’s program, in the course "Quantum Information with Atoms and Phonons"and implemented in **Python**.

## Project Overview

STIRAP enables a nearly perfect transfer of population from state **|0⟩** to state **|1⟩** without significantly populating the intermediate excited state **|e⟩**. The process is based on the **adiabatic theorem**, where the system follows an instantaneous eigenstate (the *dark state*) throughout the protocol.

The project is divided into two main parts:

### 1. Landau–Zener Model (Two-Level System)

  * Plot the **energy spectrum** as a function of time.
  * Compute the **transition probability** to the excited state numerically.
  * Compare results against the analytical **Landau–Zener formula**:

### 2. STIRAP Protocol (Three-Level Lambda System)

* Steps:

  1. Turn **ON** laser B (|e⟩ ↔ |1⟩).
  2. Slowly turn **ON** laser A (|0⟩ ↔ |e⟩).
  3. Slowly turn **OFF** laser B.
  4. Turn **OFF** laser A.

* Tasks:

  * Compute **instantaneous eigenstates** of the Hamiltonian.
  * Identify the **dark state** that evolves from |0⟩ to |1⟩.
  * Track **energy gaps** between the dark state and other eigenstates.
  * Apply the **adiabatic theorem** to verify population transfer.
  * Perform **numerical integration** to estimate imperfections and test Landau–Zener applicability.

## Technologies & Libraries

* **Python**
* [NumPy](https://numpy.org/) – numerical computations
* [SciPy](https://scipy.org/) – ODE solvers & linear algebra (`solve_ivp`, `eigh`)
* [Matplotlib](https://matplotlib.org/) – visualization of spectra, populations & dynamics
* [Pandas](https://pandas.pydata.org/) – data handling and analysis

## Results

* The **Landau–Zener model** shows excellent agreement between numerical and analytical results, validating the role of adiabaticity.
* In the **STIRAP protocol**, the dark state provides an efficient pathway for population transfer from |0⟩ to |1⟩, with numerical simulations confirming robustness under adiabatic conditions.
* Deviations are quantified to assess the limits of the Landau–Zener approximation in multi-level systems.

## How to Run

Clone the repository and run the Jupyter notebooks or Python scripts:

```bash
git clone https://github.com/miguelaviiles/STIRAP-Quantum-Information.git
cd STIRAP
```

Dependencies can be installed via:

```bash
pip install numpy scipy matplotlib pandas
```

## References

* K. Bergmann, H. Theuer, and B. W. Shore, *Coherent population transfer among quantum states of atoms and molecules*, Rev. Mod. Phys. 70, 1003 (1998).
* C. E. Carroll and F. T. Hioe, *Transition probabilities for the Landau–Zener model*, J. Phys. A 19, 2061 (1986).
