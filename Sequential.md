# PART A - Sequential Matrix Multiplication

## 1. Introduction

The sequential implementation performs matrix multiplication using CPU-based execution without parallel processing.

Two 4000 × 4000 matrices are multiplied using three nested loops to calculate the resulting matrix.

The execution time obtained from this implementation is used as a reference point for evaluating parallel and GPU-based implementations.

## 2. Environment Setup

### WSL2 Verification

WSL2 was set up and Ubuntu was opened successfully before starting the experiment.

The Linux environment was checked and was ready for the experiment.

The setup was completed successfully and was ready to run the program.

### GCC Verification

The GCC compiler was set up successfully in the Ubuntu environment, and the installed version was checked to confirm that it was ready for compiling the C program.

## 3. Sequential Matrix Multiplication Program

The sequential matrix multiplication program was developed in C using three nested loops to compute the elements of the resulting matrix.

The program performs multiplication on two matrices, each having a size of 4000 × 4000.

The execution time is measured to evaluate the performance of the sequential implementation.

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define N 4000

int main()
{
    int i, j, k;
    double *A, *B, *C;
    clock_t start, end;

    A = (double *)malloc(N * N * sizeof(double));
    B = (double *)malloc(N * N * sizeof(double));
    C = (double *)malloc(N * N * sizeof(double));

    if (A == NULL || B == NULL || C == NULL)
    {
        printf("Memory allocation failed\n");
        return 1;
    }

    printf("Initializing %d x %d matrices...\n", N, N);

    for (i = 0; i < N; i++)
    {
        for (j = 0; j < N; j++)
        {
            A[i * N + j] = 1.0;
            B[i * N + j] = 1.0;
            C[i * N + j] = 0.0;
        }
    }

    start = clock();

    for (i = 0; i < N; i++)
    {
        for (j = 0; j < N; j++)
        {
            for (k = 0; k < N; k++)
            {
                C[i * N + j] +=
                    A[i * N + k] * B[k * N + j];
            }
        }
    }

    end = clock();

    printf("\nSequential Matrix Multiplication Completed\n");
    printf("Matrix Size = %d x %d\n", N, N);
    printf("Execution Time = %f seconds\n",
           (double)(end - start) / CLOCKS_PER_SEC);
    printf("Verification C[0][0] = %.2f\n", C[0]);

    free(A);
    free(B);
    free(C);

    return 0;
}
```
## 3. Working and Output

The Sequential matrix multiplication program was compiled and executed successfully. The generated output was checked to confirm the correctness of the 4000 × 4000 matrix multiplication.

<img width="880" height="252" alt="sequential_olp" src="https://github.com/user-attachments/assets/4f112442-c2f8-46e4-a04a-1c5d3599150a" />

## 4. Result

The program completed successfully, and the output was correct.
