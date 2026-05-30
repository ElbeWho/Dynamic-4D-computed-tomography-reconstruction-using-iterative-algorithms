Dynamic 4D Computed Tomography: Reconstruction & Deep Learning Post-Processing
This repository contains a suite of Jupyter Notebooks dedicated to the reconstruction and enhancement of dynamic 4D Computed Tomography (CT) data. The project focuses on multiphase fluid dynamics, specifically targeting the reduction of severe motion artifacts (such as "comet tails") caused by the limited temporal resolution of CT scanners when imaging fast-moving objects in high-viscosity media.

The codebase encompasses the entire pipeline: from classical analytical and iterative tomographic reconstruction to advanced, deep learning-based post-processing.

🚀 Key Features:
Classical & Iterative Reconstruction: Implementation of standard analytical methods (FBP, FDK) alongside advanced iterative algorithms like SIRT (Simultaneous Iterative Reconstruction Technique) and WBP (Weighted Back Projection) from PUBLICATION: Improving image quality in fast,      time‑resolved micro‑CT by weighted back projection Marjolein Heyndrickx1, Tom Bultreys2, Wannes Goethals1, Luc Van Hoorebeke1 & Matthieu N. Boone1 doi.org/10.1038/s41598-020-74827-x .

Deep Learning Enhancement: A custom 3D U-Net architecture designed to act as an intelligent spatial filter, effectively mitigating motion blur and restoring the true geometric fidelity of the reconstructed objects.

Synthetic Data Generation: Tools for simulating volumetric target data to train the neural network effectively without relying solely on ground-truth experimental scans.

End-to-End Workflow: Step-by-step Jupyter Notebooks guiding through raw projection loading, sinogram processing, mathematical reconstruction, and final neural network post-processing.

Data: CT scanner X-Ray150 raw data is provided for dynamic experiment containing plastic pipe of glycerine and floating air-bubles. 

🛠️ Prerequisites & Installation:
To run the notebooks, you will need a Python 3 environment. Due to the heavy computational requirements of 3D volumetric processing, a CUDA-enabled GPU is highly recommended.

The primary external dependencies include:

PyTorch (for the 3D U-Net implementation and tensor operations)

ASTRA Toolbox (for high-performance tomographic reconstruction algorithms)

NumPy & SciPy (for matrix operations and scientific computing)

Matplotlib (for cross-sectional visualization)

Clone the repository and install the required packages:

📄 License:
This project is licensed under the MIT License - see the LICENSE file for details.

Contact: 
If any questions arise please contact elbewho@gmail.com. 
If data for static reconstruction (three probes with different contrast fluid) is needed please contact elbewho@gmail.com.
