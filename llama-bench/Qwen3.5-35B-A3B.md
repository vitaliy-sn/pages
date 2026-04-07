```bash
root@0e9649ed9a23:/models/bartowski/Qwen3.5-35B-A3B-GGUF# /app/llama-bench -ctk f16 -ctv f16 -fa 1 -m Qwen_Qwen3.5-35B-A3B-Q2_K.gguf,Qwen_Qwen3.5-35B-A3B-Q2_K_L.gguf,Qwen_Qwen3.5-35B-A3B-Q4_K_L.gguf,Qwen_Qwen3.5-35B-A3B-Q5_K_L.gguf,Qwen_Qwen3.5-35B-A3B-Q6_K.gguf,Qwen_Qwen3.5-35B-A3B-Q6_K_L.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                           |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2471.98 ± 15.60 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         95.63 ± 0.48 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |       2466.72 ± 9.33 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         93.02 ± 0.53 |
| qwen35moe 35B.A3B Q4_K - Medium |  20.27 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2961.62 ± 16.74 |
| qwen35moe 35B.A3B Q4_K - Medium |  20.27 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         87.57 ± 0.30 |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2933.00 ± 22.00 |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         84.45 ± 0.30 |
| qwen35moe 35B.A3B Q6_K          |  27.96 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2729.20 ± 19.47 |
| qwen35moe 35B.A3B Q6_K          |  27.96 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         83.37 ± 0.44 |
| qwen35moe 35B.A3B Q6_K          |  28.19 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2732.91 ± 16.56 |
| qwen35moe 35B.A3B Q6_K          |  28.19 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         81.69 ± 0.14 |

build: 990e4d9 (1)
```


```bash
root@eb4a6c7037f0:/models/bartowski/Qwen3.5-35B-A3B-GGUF# /app/llama-bench -ctk f16 -ctv f16 -fa 1 -m Qwen_Qwen3.5-35B-A3B-Q2_K.gguf,Qwen_Qwen3.5-35B-A3B-Q2_K_L.gguf,Qwen_Qwen3.5-35B-A3B-Q4_K_L.gguf,Qwen_Qwen3.5-35B-A3B-Q5_K_L.gguf,Qwen_Qwen3.5-35B-A3B-Q6_K.gguf,Qwen_Qwen3.5-35B-A3B-Q6_K_L.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                           |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2433.88 ± 11.44 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        134.82 ± 2.90 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |       2435.63 ± 7.02 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        128.63 ± 2.29 |
| qwen35moe 35B.A3B Q4_K - Medium |  20.27 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2925.81 ± 13.82 |
| qwen35moe 35B.A3B Q4_K - Medium |  20.27 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        123.82 ± 1.43 |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2889.20 ± 22.67 |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        113.92 ± 1.78 |
| qwen35moe 35B.A3B Q6_K          |  27.96 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2694.98 ± 18.38 |
| qwen35moe 35B.A3B Q6_K          |  27.96 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        113.15 ± 1.73 |
| qwen35moe 35B.A3B Q6_K          |  28.19 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2701.37 ± 17.28 |
| qwen35moe 35B.A3B Q6_K          |  28.19 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        109.71 ± 1.76 |

build: 9f102a1 (1)
```



```bash
root@0e9649ed9a23:/models/unsloth/Qwen3.5-35B-A3B-GGUF# /app/llama-bench -ctk f16 -ctv f16 -fa 1 -m Qwen3.5-35B-A3B-UD-Q2_K_XL.gguf,Qwen3.5-35B-A3B-UD-Q6_K_S.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                           |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2810.91 ± 18.36 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         92.85 ± 0.62 |
| qwen35moe 35B.A3B Q8_0          |  26.55 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |       2610.81 ± 8.00 |
| qwen35moe 35B.A3B Q8_0          |  26.55 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         85.95 ± 0.37 |

build: 990e4d9 (1)
```


```bash
root@eb4a6c7037f0:/models/unsloth/Qwen3.5-35B-A3B-GGUF# /app/llama-bench -ctk f16 -ctv f16 -fa 1 -m Qwen3.5-35B-A3B-UD-Q2_K_XL.gguf,Qwen3.5-35B-A3B-UD-Q6_K_S.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                           |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2773.65 ± 18.49 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        125.66 ± 1.37 |
| qwen35moe 35B.A3B Q8_0          |  26.55 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |       2573.69 ± 8.07 |
| qwen35moe 35B.A3B Q8_0          |  26.55 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        115.97 ± 0.77 |

build: 9f102a1 (1)
```


