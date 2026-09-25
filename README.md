# Parallel-and-GPU-Computing

## Experiments

### 1. Sequential Matrix Multiplication

A basic matrix multiplication implementation using sequential CPU execution.

It provides a reference for comparing the performance of parallel matrix multiplication methods.

[View Sequential Experiment](./Sequential.md)

### 2. OpenMP Matrix Multiplication

A parallel matrix multiplication implementation using OpenMP with multiple CPU threads.

It divides the work among threads to perform the calculations simultaneously.

[View OpenMP Experiment](./OpenMP.md)

### 3. MPI Matrix Multiplication

A distributed-memory implementation using MPI across multiple processes and virtual machines. 

The computation is divided among different processes to perform the matrix multiplication in parallel.

[View MPI Experiment](./MPI.md)

### 4. CUDA Matrix Multiplication

[View CUDA Experiment](./CUDA.md)

## Problem Definition

The matrix multiplication experiment uses:

- Matrix A: 4000 × 4000
- Matrix B: 4000 × 4000
- Matrix C: A × B
- Matrix elements: 1.0
- Expected verification: C[0][0] = 4000.00

## Technologies Used

- C
- GCC
- Ubuntu
- WSL2
- OpenMP
- MPI
- CUDA

## Repository Structure

```text
Parallel-and-GPU-Computing
│
├── README.md
├── Sequential.md
├── OpenMP.md
├── MPI.md
└── CUDA.md
