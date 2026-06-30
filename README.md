# Entropy-Degree Theorem for Alexandrov Spaces

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/downloads/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)  
[![Research Paper](https://img.shields.io/badge/ArXiv-2606.30403v1-b31b1b.svg)](https://arxiv.org/pdf/2606.30403v1)  
[![Build Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)](#)  

---

## Overview

This repository contains a Python implementation of the core results and algorithms described in the research paper **"The Entropy-Degree Theorem for Alexandrov Spaces"** by P. Suárez-Serrato. The paper extends the classical entropy-rigidity results of Besson, Courtois, and Gallot to Alexandrov spaces with curvature bounded below, which are a generalization of Riemannian manifolds that allow for singularities. 

The implementation focuses on:
1. **Entropy-Degree Theorem**: Establishing the relationship between the entropy of Lipschitz maps and their degree in Alexandrov spaces.
2. **Degree Theorem**: Demonstrating the equivalence between analytical and topological degrees using the Ambrosio–Kirchheim theory of integral currents.
3. **Applications**: Computing geometric obstructions, volume bounds, and asymptotic translation lengths for various geometric objects.

This project provides a computational framework to explore these concepts, including tools to calculate entropy, degree, and related geometric properties for Alexandrov spaces.

---

## Core Idea of the Paper

The **Entropy-Degree Theorem** generalizes the classical entropy-rigidity results to Alexandrov spaces, which are metric spaces with curvature bounded below. These spaces can have singularities, making them more general than smooth Riemannian manifolds. The key contributions of the paper include:

1. **Entropy-Degree Relationship**: Establishing a quantitative relationship between the entropy of Lipschitz maps and their topological degree in Alexandrov spaces.
2. **Degree Theorem**: Using the Ambrosio–Kirchheim theory of integral currents to prove the equivalence of analytical and topological degrees in singular spaces.
3. **Applications**: 
   - Geometric obstructions for negatively curved Einstein metrics on 4-orbifolds.
   - Volume bounds for cone-manifolds and cone-orbifolds.
   - Quantitative inequalities for hyperbolic convex cores.
   - Lower bounds on asymptotic translation lengths of end-periodic surface homeomorphisms.

These results provide new insights into the geometry and topology of Alexandrov spaces, particularly in the context of metric singularities and Gromov–Hausdorff limits.

---

## How It Works

The implementation is structured around the following key components:

1. **Entropy Calculation**: 
   - Computes the entropy of Lipschitz maps between Alexandrov spaces.
   - Uses numerical integration techniques to approximate the volume growth of geodesics.

2. **Degree Computation**:
   - Implements the analytical and topological degree calculations using integral currents.
   - Verifies the equivalence of these degrees as per the Degree Theorem.

3. **Applications**:
   - Provides tools to compute volume bounds for cone-manifolds and cone-orbifolds.
   - Implements algorithms to calculate asymptotic translation lengths for end-periodic surface homeomorphisms.
   - Simulates Gromov–Hausdorff limits and detects metric singularities.

4. **Visualization**:
   - Includes visualization utilities for Alexandrov spaces, geodesics, and curvature bounds.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/entropy-degree-alexandrov.git
   cd entropy-degree-alexandrov
   ```

2. Create a virtual environment and activate it:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

The main functionality is implemented in the `implementation.py` script. Below are the instructions to use the script:

### 1. Calculate Entropy of a Lipschitz Map

To calculate the entropy of a given Lipschitz map between two Alexandrov spaces, use the following command:

```bash
python implementation.py --task entropy --input input_data.json
```

- **`--task`**: Specifies the task to perform. Use `entropy` for entropy computation.
- **`--input`**: Path to the JSON file containing the input data (e.g., metric tensors, curvature bounds, and map parameters).

### 2. Compute Degree of a Map

To compute the analytical and topological degrees of a map, run:

```bash
python implementation.py --task degree --input input_data.json
```

- **`--task`**: Use `degree` for degree computation.
- **`--input`**: Path to the JSON file containing the input data.

### 3. Analyze Applications

To explore specific applications (e.g., volume bounds, asymptotic translation lengths), use:

```bash
python implementation.py --task application --app_type <app_type> --input input_data.json
```

- **`--task`**: Use `application` for application-specific computations.
- **`--app_type`**: Specify the application type. Options include:
  - `volume_bounds`
  - `translation_lengths`
  - `gromov_hausdorff`
- **`--input`**: Path to the JSON file containing the input data.

### 4. Visualize Results

To visualize the results (e.g., geodesics, curvature bounds), use:

```bash
python implementation.py --task visualize --input results.json
```

- **`--task`**: Use `visualize` for generating visualizations.
- **`--input`**: Path to the JSON file containing the results data.

---

## Example

Here is an example of how to calculate the entropy of a Lipschitz map between two Alexandrov spaces:

1. Prepare an input JSON file (`input_data.json`) with the following structure:
   ```json
   {
       "space1": {
           "type": "Alexandrov",
           "curvature_bound": -1,
           "dimension": 3
       },
       "space2": {
           "type": "Alexandrov",
           "curvature_bound": -1,
           "dimension": 3
       },
       "map": {
           "type": "Lipschitz",
           "parameters": {
               "L": 2.0
           }
       }
   }
   ```

2. Run the script:
   ```bash
   python implementation.py --task entropy --input input_data.json
   ```

3. The output will display the computed entropy of the map.

---

## Contributing

We welcome contributions to this project! If you have suggestions for new features, bug fixes, or improvements, please feel free to submit a pull request or open an issue. Make sure to follow the contribution guidelines in `CONTRIBUTING.md`.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## References

- P. Suárez-Serrato, "The Entropy-Degree Theorem for Alexandrov Spaces", [arXiv:2606.30403v1](https://arxiv.org/pdf/2606.30403v1).