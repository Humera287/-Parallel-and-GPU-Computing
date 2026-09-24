# Part B - OpenMP Matrix Multiplication

## 1. OpenMPI Setup

OpenMPI and OpenSSH were set up on the required Ubuntu systems for running the matrix multiplication program.

The configuration allowed the systems to communicate and run the MPI program across multiple processes.

## 2. MPI Program

The matrix multiplication program was implemented using MPI, with the computation divided among multiple processes.

Each process handles a part of the matrix calculation to perform the multiplication efficiently.

## 3. Working and Output

The OpenMP matrix multiplication program was compiled and executed successfully using 8 threads.

The program multiplied two 4000 × 4000 matrices and completed the calculation successfully.

The output was verified to ensure that the matrix multiplication result was correct.

<img width="762" height="294" alt="openmp" src="https://github.com/user-attachments/assets/553569cd-33ad-4bb8-90e2-89ffd1049572" />

## 4. Result

The OpenMP matrix multiplication program was executed successfully.

The program completed the calculation in 40.545825 seconds.

The verification value **C[0][0] = 4000.00** was obtained, confirming that the result was correct.
