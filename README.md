## Notes

- GPU: NVIDIA GeForce GTX 1660 Ti
- `nvcc matrix_cuda.cu`
- `nvcc -Xcompiler -fopenmp mm_omp_vs_cuda.cu` (requires linking to OpenMP I'd guess?)


```
(py310) vsaraph@carbon:~/matrix-cuda$ ./a.out
please type in m n and k
1000 1000 1000
Time elapsed on matrix multiplication of 1000x1000 . 1000x1000 on GPU: 5.057536 ms.

Time elapsed on matrix multiplication of 1000x1000 . 1000x1000 on CPU: 2746.421875 ms.

all results are correct!!!, speedup = 543.035522
```

543x seems like a huge speedup to me! Though it's against naive matrix multiplication that doesn't use any CPU parallelism.

See original README here: [link](https://github.com/lzhengchun/matrix-cuda/blob/master/README.md)
