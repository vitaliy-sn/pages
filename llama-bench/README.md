# Qwen3.5-122B-A10B

```bash
root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen_Qwen3.5-122B-A10B-IQ1_M.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 122B.A10B IQ1_M - 1.75 bpw |  27.27 GiB |   122.11 B | CUDA       |  99 |  1 |           pp512 |        724.01 ± 3.49 |
| qwen35moe 122B.A10B IQ1_M - 1.75 bpw |  27.27 GiB |   122.11 B | CUDA       |  99 |  1 |           tg128 |         54.58 ± 0.31 |

build: 463b6a9 (1)

root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen_Qwen3.5-122B-A10B-IQ2_XXS.gguf -ngl 44
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 122B.A10B IQ2_XXS - 2.0625 bpw |  31.47 GiB |   122.11 B | CUDA       |  44 |  1 |           pp512 |        762.62 ± 8.32 |
| qwen35moe 122B.A10B IQ2_XXS - 2.0625 bpw |  31.47 GiB |   122.11 B | CUDA       |  44 |  1 |           tg128 |         32.08 ± 1.10 |

build: 463b6a9 (1)
```



# Qwen3.5-35B-A3B

```bash
root@20a122decb3f:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-35B-A3B-GGUF/Qwen_Qwen3.5-35B-A3B-Q2_K.gguf,/models/bartowski/Qwen3.5-35B-A3B-GGUF/Qwen_Qwen3.5-35B-A3B-Q2_K_L.gguf,/models/bartowski/Qwen3.5-35B-A3B-GGUF/Qwen_Qwen3.5-35B-A3B-Q4_K_L.gguf,/models/unsloth/Qwen3.5-35B-A3B-GGUF/Qwen3.5-35B-A3B-UD-Q2_K_XL.gguf,/models/unsloth/Qwen3.5-35B-A3B-GGUF/Qwen3.5-35B-A3B-UD-Q6_K_S.gguf,/models/AesSedai/Qwen3.5-35B-A3B-Q5_K_M-00001-of-00002.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                           |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2417.31 ± 12.77 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         94.14 ± 0.25 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |       2415.15 ± 7.08 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         91.54 ± 0.33 |
| qwen35moe 35B.A3B Q4_K - Medium |  20.27 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2889.59 ± 13.88 |
| qwen35moe 35B.A3B Q4_K - Medium |  20.27 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         87.12 ± 0.20 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2729.11 ± 20.97 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         92.07 ± 0.45 |
| qwen35moe 35B.A3B Q8_0          |  26.55 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2538.66 ± 18.09 |
| qwen35moe 35B.A3B Q8_0          |  26.55 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         85.15 ± 0.43 |
| qwen35moe 35B.A3B Q8_0          |  24.45 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2967.97 ± 16.30 |
| qwen35moe 35B.A3B Q8_0          |  24.45 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |         80.45 ± 0.30 |

build: 463b6a9 (1)



root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-35B-A3B-GGUF/Qwen_Qwen3.5-35B-A3B-Q2_K.gguf,/models/bartowski/Qwen3.5-35B-A3B-GGUF/Qwen_Qwen3.5-35B-A3B-Q2_K_L.gguf,/models/unsloth/Qwen3.5-35B-A3B-GGUF/Qwen3.5-35B-A3B-UD-Q2_K_XL.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      3047.05 ± 61.44 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |        162.05 ± 0.55 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      3044.33 ± 53.42 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |        158.35 ± 0.23 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      3468.29 ± 68.72 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |        155.40 ± 0.53 |

build: 463b6a9 (1)
root@c5cf8d322703:/app# ./llama-bench -dev CUDA1 -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-35B-A3B-GGUF/Qwen_Qwen3.5-35B-A3B-Q2_K.gguf,/models/bartowski/Qwen3.5-35B-A3B-GGUF/Qwen_Qwen3.5-35B-A3B-Q2_K_L.gguf,/models/unsloth/Qwen3.5-35B-A3B-GGUF/Qwen3.5-35B-A3B-UD-Q2_K_XL.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA1        |           pp512 |      1973.03 ± 18.34 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.76 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA1        |           tg128 |        108.77 ± 2.07 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA1        |           pp512 |       1972.59 ± 8.75 |
| qwen35moe 35B.A3B Q2_K - Medium |  12.22 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA1        |           tg128 |        103.09 ± 2.87 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA1        |           pp512 |      2221.74 ± 12.64 |
| qwen35moe 35B.A3B Q2_K - Medium |  11.31 GiB |    34.66 B | CUDA       |  99 |  1 | CUDA1        |           tg128 |         99.21 ± 0.08 |

build: 463b6a9 (1)

```



# Qwen3.5-27B

```bash
root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q3_K_S.gguf,/models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q4_K_M.gguf,/models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q4_K_L.gguf,/models/unsloth/Qwen3.5-27B-Q4_K_M.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1077.77 ± 0.85 |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         29.88 ± 0.16 |
| qwen35 27B Q4_K - Medium       |  15.94 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1235.89 ± 0.57 |
| qwen35 27B Q4_K - Medium       |  15.94 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         26.13 ± 0.12 |
| qwen35 27B Q4_K - Medium       |  16.82 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1235.61 ± 0.13 |
| qwen35 27B Q4_K - Medium       |  16.82 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         25.70 ± 0.13 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1222.61 ± 0.38 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         26.39 ± 0.01 |


build: 463b6a9 (1)
root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q3_K_S.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      1490.63 ± 35.59 |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |         45.59 ± 0.02 |

build: 463b6a9 (1)

root@c5cf8d322703:/app# ./llama-bench -dev CUDA1 -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q3_K_S.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA1        |           pp512 |        849.76 ± 8.98 |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA1        |           tg128 |         26.21 ± 0.03 |

build: 463b6a9 (1)



root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/Jackrong/Qwen3.5-27B-Claude-4.6-Opus-Reasoning-Distilled-GGUF/Qwen3.5-27B.Q3_K_M.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35 27B Q3_K - Medium       |  12.37 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      1562.24 ± 33.71 |
| qwen35 27B Q3_K - Medium       |  12.37 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |         45.21 ± 0.04 |

build: 463b6a9 (1)



root@94f1374dc896:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q5_K_S.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Small        |  17.79 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1249.66 ± 0.61 |
| qwen35 27B Q5_K - Small        |  17.79 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         24.14 ± 0.03 |



build: 990e4d9 (1)
root@94f1374dc896:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q5_K_L.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Medium       |  19.30 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1197.01 ± 0.58 |
| qwen35 27B Q5_K - Medium       |  19.30 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         22.83 ± 0.04 |

build: 990e4d9 (1)

```



# Qwen3-Coder-Next

```bash
root@fde9ead225db:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/Qwen3-Coder-Next-UD-IQ3_S.gguf,/models/unsloth/Qwen3-Coder-Next-UD-IQ3_XXS.gguf,/models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q2_K_L.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                                  |       size |     params | backend    | ngl | fa |            test |                  t/s |
| -------------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B IQ3_S - 3.4375 bpw   |  27.65 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |      1525.19 ± 10.73 |
| qwen3next 80B.A3B IQ3_S - 3.4375 bpw   |  27.65 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         69.77 ± 0.27 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  26.52 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |      1529.90 ± 18.69 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  26.52 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         70.37 ± 0.34 |
| qwen3next 80B.A3B Q2_K - Medium        |  26.51 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |       1366.93 ± 9.97 |
| qwen3next 80B.A3B Q2_K - Medium        |  26.51 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         76.06 ± 0.36 |

build: 463b6a9 (1)



root@02cbbcd4a580:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-IQ3_XXS.gguf -ncmoe 2
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  29.54 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |      1380.25 ± 13.28 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  29.54 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         80.55 ± 1.05 |

build: 463b6a9 (1)

root@02cbbcd4a580:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q3_K_M.gguf -ngl 40
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B Q3_K - Medium |  34.13 GiB |    79.67 B | CUDA       |  40 |  1 |           pp512 |        682.74 ± 4.94 |
| qwen3next 80B.A3B Q3_K - Medium |  34.13 GiB |    79.67 B | CUDA       |  40 |  1 |           tg128 |         44.44 ± 0.32 |

build: 463b6a9 (1)

root@02cbbcd4a580:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_K_L.gguf -ngl 30
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  30 |  1 |           pp512 |        397.19 ± 4.11 |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  30 |  1 |           tg128 |         27.39 ± 0.31 |

build: 463b6a9 (1)



root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/mradermacher/Huihui-Qwen3-Coder-Next-abliterated.i1-IQ3_XXS.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  28.68 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |      1779.17 ± 10.89 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  28.68 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         75.47 ± 0.18 |

build: 463b6a9 (1)
```



# GLM-4.7-Flash

```bash
root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/zai-org_GLM-4.7-Flash-Q4_K_M.gguf   
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| deepseek2 30B.A3B Q4_K - Medium |  17.20 GiB |    29.94 B | CUDA       |  99 |  1 |           pp512 |       3041.40 ± 8.29 |
| deepseek2 30B.A3B Q4_K - Medium |  17.20 GiB |    29.94 B | CUDA       |  99 |  1 |           tg128 |         82.05 ± 0.16 |

build: 463b6a9 (1)
```



# GLM-4.5-Air

```bash
root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/zai-org_GLM-4.5-Air-Q2_K_L.gguf -ngl 30
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| glm4moe 106B.A12B Q2_K - Medium |  43.49 GiB |   110.47 B | CUDA       |  30 |  1 |           pp512 |        291.32 ± 2.98 |
| glm4moe 106B.A12B Q2_K - Medium |  43.49 GiB |   110.47 B | CUDA       |  30 |  1 |           tg128 |         15.24 ± 0.08 |

build: 463b6a9 (1)
```



# ERNIE-4.5-21B-A3B-PT

```bash
root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/ERNIE-4.5-21B-A3B-PT-UD-Q4_K_XL.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| ernie4_5-moe 21B.A3B Q4_K - Medium |  12.51 GiB |    21.83 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      5731.95 ± 75.41 |
| ernie4_5-moe 21B.A3B Q4_K - Medium |  12.51 GiB |    21.83 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |        229.24 ± 4.22 |

build: 463b6a9 (1)
```



# gpt-oss-20b

```bash
root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/ggml-org/gpt-oss-20b-mxfp4/gpt-oss-20b-mxfp4.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| gpt-oss 20B MXFP4 MoE          |  11.27 GiB |    20.91 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      7784.29 ± 64.52 |
| gpt-oss 20B MXFP4 MoE          |  11.27 GiB |    20.91 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |        223.64 ± 3.46 |

build: 463b6a9 (1)



root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/gpt-oss-20b-GGUF/openai_gpt-oss-20b-bf16.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| gpt-oss 20B BF16               |  12.83 GiB |    20.91 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      7333.37 ± 71.89 |
| gpt-oss 20B BF16               |  12.83 GiB |    20.91 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |        168.42 ± 1.21 |

build: 463b6a9 (1)
```



# gpt-oss-120b

```bash
root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/ggml-org/gpt-oss-120b-mxfp4/gpt-oss-120b-mxfp4-00001-of-00003.gguf -ngl 16
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| gpt-oss 120B MXFP4 MoE         |  59.02 GiB |   116.83 B | CUDA       |  16 |  1 |           pp512 |        310.43 ± 4.26 |
| gpt-oss 120B MXFP4 MoE         |  59.02 GiB |   116.83 B | CUDA       |  16 |  1 |           tg128 |         21.13 ± 0.06 |

build: 463b6a9 (1)
```



# gemma-3-27b-it

```bash
root@c5cf8d322703:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/gemma-3-27b-it-GGUF/google_gemma-3-27b-it-Q6_K_L.gguf,/models/bartowski/gemma-3-27b-it-GGUF/google_gemma-3-27b-it-Q4_K_L.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB (15403 MiB free)
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB (15686 MiB free)
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| gemma3 27B Q6_K                |  20.96 GiB |    27.01 B | CUDA       |  99 |  1 |           pp512 |       1129.50 ± 0.58 |
| gemma3 27B Q6_K                |  20.96 GiB |    27.01 B | CUDA       |  99 |  1 |           tg128 |         21.28 ± 0.02 |
| gemma3 27B Q4_K - Medium       |  15.72 GiB |    27.01 B | CUDA       |  99 |  1 |           pp512 |       1379.93 ± 0.86 |
| gemma3 27B Q4_K - Medium       |  15.72 GiB |    27.01 B | CUDA       |  99 |  1 |           tg128 |         27.21 ± 0.08 |

build: 463b6a9 (1)
```
