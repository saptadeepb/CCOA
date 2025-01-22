# Chaotic Crayfish Optimization Algorithm (CCOA)

## Overview
The Chaotic Crayfish Optimization Algorithm (CCOA) is a metaheuristic optimization technique that leverages chaotic maps to enhance the exploration capabilities of the search process. This implementation is designed for use with various benchmark functions and demonstrates the effectiveness of chaos in optimization.

## Authors
- **Binanda Maiti**: [binandamath.sch@nita.ac.in](mailto:binandamath.sch@nita.ac.in)
- **Saptadeep Biswas**: [saptadeepmath.sch@nita.ac.in ](mailto:saptadeepmath.sch@nita.ac.in )

## System Requirements
- MATLAB 2021a or later
- Intel(R) Core(TM) i7-11700 processor (2.50GHz)
- 16GB RAM
- Operating System: Windows 11 (64-bit)

## Features
- Supports multiple chaotic maps, including:
  - Chebyshev
  - Circle
  - Gauss
  - Iterative
  - Logistic
  - Piecewise
  - Sine
  - Singer
  - Sinusoidal
  - Tent
- Visualization of optimization results, including convergence curves and parameter space.

## Getting Started

### Installation
1. Clone the repository or download the source code.
2. Open the MATLAB environment.
3. Navigate to the directory containing the source code.

### Usage
1. **Initialization**: Set the number of search agents (`N`), the name of the benchmark function (`F_name`), and the maximum number of iterations (`T`).
2. **Function Call**: Execute the main function `choaticCOA(N, T, LB, UB, Dim, F_obj, chaos_type)` to start the optimization process.
   - `LB` and `UB` are the lower and upper bounds for the search space.
   - `Dim` is the dimensionality of the problem.
   - `F_obj` is the objective function to be minimized.
   - `chaos_type` specifies the chaotic map to be used.

### Example
```matlab
N = 100;                % Number of search agents
F_name = &#39;F1&#39;;         % Benchmark function name
T = 200;               % Maximum iterations
chaos_type = &#39;Logistic&#39;; % Type of chaotic map

[LB, UB, Dim, F_obj] = Get_F(F_name); % Retrieve function details
[best_fun, best_position, curve_f, global_cov] = choaticCOA(N, T, LB, UB, Dim, F_obj, chaos_type);
