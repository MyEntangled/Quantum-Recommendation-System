# Quantum Recommendation System 
## Project Overview

The project aim to implement the paper [Quantum Recommendation System](https://arxiv.org/pdf/1603.08675.pdf) using **Qiskit**. 
Quantum Recommendation System (QRS) is a quantum algorithm that provides personalized recommendation to individual users given their partial information. The information is given as an <img src="https://render.githubusercontent.com/render/math?math=m \times n"> preference matrix, which is assumed to have a good rank-<img src="https://render.githubusercontent.com/render/math?math=k"> approximation. It is the first algorithm to have polylogarithmic runtime in dimensions <img src="https://render.githubusercontent.com/render/math?math=mn">, <img src="https://render.githubusercontent.com/render/math?math=O(\text{poly}(k)\text{polylog}(mn))">. The advantage comes from an efficient sampling from an approximation of the preference matrix without reconstructing the entire matrix. This provides one of the first examples of application of quantum machine learning in real-world problems.
This is the first implementation of the paper [Quantum Recommendation System](https://arxiv.org/pdf/1603.08675.pdf) in **Qiskit**.

## Quantum Recommendation System in a nutshell

Quantum Recommendation System can be described briefly with 5 steps.

* **Step 1** : Prepare the preference matrix <img src="https://render.githubusercontent.com/render/math?math=T"> .
* **Step 2** : Uniform subsample from matrix <img src="https://render.githubusercontent.com/render/math?math=T"> to achieve <img src="https://render.githubusercontent.com/render/math?math=\hat{T}"> .
* **Step 3** : Perform QSVE ( Quantum Singular Value Estimation ) to achieve <img src="https://render.githubusercontent.com/render/math?math=\hat{T}_k"> (<img src="https://render.githubusercontent.com/render/math?math=\left \| T-T_k \right \| < \varepsilon \left \| T \right \|_F">
 for some small <img src="https://render.githubusercontent.com/render/math?math=\varepsilon > 0"> ) .
* **Step 4** : Apply quantum projection algorithm with threshold <img src="https://render.githubusercontent.com/render/math?math=\sigma = \sqrt{\frac{\varepsilon^2 p}{2k}}\left \| \hat{T} \right \|_F">
 to <img src="https://render.githubusercontent.com/render/math?math=T">, the vector corresponding to the <img src="https://render.githubusercontent.com/render/math?math=i">-th row <img src="https://render.githubusercontent.com/render/math?math=\hat{T}_i"> .
* **Step 5** : Measure projected state to get the recommendation .

For more details, visit the link: [Quantum Recommendation System](https://arxiv.org/pdf/1603.08675.pdf)

## Programming Languages and Services Used

* **Python**
* **Qiskit**
* **Jupyter Notebook**

## About us
[Trong Duong Dinh](https://github.com/MyEntangled)- Korea Advanced Institute of Science and Technology, Year 2

[Bao Bach Gia](https://github.com/bachbao) - Ho Chi Minh University of Technology, Year 2 