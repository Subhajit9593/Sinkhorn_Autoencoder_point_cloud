# Sinkhorn_Autoencoder_point_cloud
# Permutation-Invariant 3D Point-Cloud Sinkhorn Autoencoders

**PyTorch | Optimal Transport | Wasserstein Autoencoders | ModelNet40**

## Overview

This project explores permutation-invariant representation learning for unordered 3D point clouds using autoencoder architectures and Optimal Transport.

Unlike images, point clouds are represented as unordered sets of 3D coordinates, making reconstruction challenging because there is no predefined correspondence between input and reconstructed points.

The project investigates Sinkhorn Optimal Transport as a correspondence-free reconstruction objective and Sliced Wasserstein Distance for regularizing latent representations.

## Key Contributions

- **Permutation-Invariant Autoencoders:** Developed autoencoder architectures for unordered N × 3 point clouds, learning representations of 3D geometry independently of input point ordering.

- **Sinkhorn Optimal Transport:** Implemented entropy-regularized Sinkhorn Optimal Transport from scratch using fully vectorized, differentiable PyTorch operations.

- **Set-to-Set Reconstruction:** Used optimal transport as a reconstruction objective to compare input and reconstructed point clouds without requiring explicit point-to-point correspondences.

- **Wasserstein Autoencoder:** Developed a Wasserstein Autoencoder (WAE) using Sliced Wasserstein Distance to regularize the aggregate posterior towards a Gaussian prior.

- **Sliced Wasserstein Distance:** Projected latent representations onto random directions to approximate distribution matching through one-dimensional Wasserstein distances.

## Methodology

The implementation focuses on two complementary approaches:

### 1. Sinkhorn Autoencoder

A permutation-invariant autoencoder learns to encode and reconstruct unordered point clouds. The reconstruction objective uses entropy-regularized Optimal Transport to measure geometric discrepancies between the input and reconstructed point sets.

### 2. Wasserstein Autoencoder

A Wasserstein Autoencoder extends the reconstruction framework with latent distribution regularization. Sliced Wasserstein Distance is used to match the aggregate posterior to a Gaussian prior through random projections.

## Dataset

**ModelNet40**

ModelNet40 is a benchmark dataset of 3D CAD models spanning 40 object categories. The models are represented as point clouds for geometric representation learning and reconstruction.

## Technology Stack

- Python
- PyTorch
- NumPy
- Optimal Transport
- Sinkhorn Algorithm
- Sliced Wasserstein Distance
- ModelNet40

## Repository Structure

```text
.
├── README.md
├── Sinkhorn_Autoencoder_code.ipynb
│   
└── LICENSE
