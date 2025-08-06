This repository provides the implementation and examples from our paper on ensuring Lipschitz continuity for optimization-based controllers by reformulating Quadratic Programs (QPs) as **Second-Order Cone Programs (SOCPs)**.

## 🔍 Motivation
Optimization-based controllers, such as those derived from constrained QPs, are powerful tools for controlling dynamical systems. However, when multiple constraints are involved, the resulting control law $\pi_{\rm qp}$ may lack regularity properties like Lipschitz continuity. This lack of continuity can result in:
- Discontinuous control inputs,
- chattering behavior in closed-loop systems,
- Non-unique or ill-posed system trajectories.


To address this, we propose a novel **SOCP reformulation** that ensures Lipschitz continuity of the control law, *regardless of the structure of the constraint matrices*.


## 🧩 Key Features
✅ Guaranteed Lipschitz continuity of the optimizer $\pi_{\rm socp}$

✅ Closed-form solution, unlike generic multi-constraint QPs

✅ Faster computation, enabling real-time deployment

✅ Independence from constraint regularity (e.g., no need for linearly independent gradients)

## 📁 In This Repo
- The main script is `main.ipynb`, which includes two working examples.
- Additional notebooks `example_1.nb` and `example_2.nb` provide more detailed analysis and visualizations of the two examples in the main script.


## 📈 How to Use
To get started, open the main script `main.ipynb`. This notebook demonstrates how to use the `LipschitzControllers` module to convert general QPs into our Lipschitz-continuous SOCP formulation. 
Two example problems are included to illustrate the performance and structure of the controller. 

### Examples
We provide two examples whose original QPs admit non-Lipschitz minimizers (as shown in the animations below) and show that our reformulations do admit Lipschitz continuous minimizers.
#### Example 1
![example1](https://github.com/user-attachments/assets/baba75f8-4c3a-47ee-badf-126f1e4b3db4)
#### Example 2
![example2](https://github.com/user-attachments/assets/a295eb77-84f1-44e1-9362-dc1d6405a001)

<!--For more detailed analyses of these examples, please refer to our paper.

## 📜 Citation
If you use this work, please cite:
```bibtex
@article{your2025paper,
  title     = {Guaranteed Lipschitz Reformulations of Quadratic Programs with Multiple Constraints},
  author    = {Agrawal, Devansh and Lee, Haejoon and Panagou, Dimitra},
  journal   = {...},
  year      = {2025},
  note      = {}
}
-->
