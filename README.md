# ParallelEdits_Reproducing
서울과학기술대학교 일반대학원 딥러닝 응용II:컴퓨터비전(9490033-101)

# ParallelEdits Reproduction & Methodology Comparison

This repository contains the reproduction of **ParallelEdits** (a text-based image editing model) and a comparative study exploring SDXL-based alternatives to overcome its limitations.

We refactored the legacy codebase to run on modern environments (**RTX 4080, CUDA 12.x, Python 3.12**) and conducted extensive experiments to find the optimal trade-off between structural consistency and image quality.

## 📌 Project Overview

### Goal
1.  **Reproduction:** Reproduce the results of the "ParallelEdits" paper using Stable Diffusion v1.5.
2.  **Critical Analysis:** Identify practical limitations in real-world scenarios (e.g., quality, flexibility).
3.  **Comparative Study:** Explore alternative approaches using **SDXL** and **MasaCtrl** to propose a better pipeline.

### Key Features
* **Refactored Pipeline:** Ported legacy code to support `diffusers >= 0.30.0` and `torch >= 2.4.0`.
* **Memory Optimization:** Optimized for consumer-grade high-end GPUs (RTX 4080, 16GB VRAM) using `xformers` and `accelerate`.
* **Experimental Analysis:** Detailed comparison of 4 different editing methodologies.

---

## 🛠️ Environment Setup

Unlike the original implementation which relied on older dependencies, this project is optimized for modern hardware.

| Component | Original Paper | **This Project (Refactored)** |
| :--- | :--- | :--- |
| **GPU** | V100 (Server) | **RTX 4080 (Local)** |
| **Python** | 3.8 | **3.12** |
| **PyTorch** | 1.13 + CUDA 11.x | **2.4.0 + CUDA 12.1** |
| **Diffusers** | 0.11.1 | **0.30.0** |

### Installation
```bash
# Clone the repository
git clone [https://github.com/your-username/ParallelEdits-Reproduction.git](https://github.com/your-username/ParallelEdits-Reproduction.git)
cd ParallelEdits-Reproduction

# Create a virtual environment
conda create -n parallel_edit python=3.12
conda activate parallel_edit

# Install dependencies
pip install -r requirements.txt
