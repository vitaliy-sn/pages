## build: ff5ef82

```bash
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
```

```bash
root@a64d23b65e7b:/# llama-bench -ctk f16 -ctv f16 -fa 0 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q4_K_L.gguf
| model                          |       size |     params | backend    | ngl |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | --------------: | -------------------: |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |           pp512 |      1230.00 ± 12.75 |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |           tg128 |         27.11 ± 0.01 |

root@a64d23b65e7b:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q4_K_L.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |      1240.30 ± 12.23 |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         27.24 ± 0.05 |

root@a64d23b65e7b:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q5_K_L.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Medium       |  19.83 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |      1235.08 ± 12.05 |
| qwen35 27B Q5_K - Medium       |  19.83 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         24.06 ± 0.00 |

root@a64d23b65e7b:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q6_K_L.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q6_K                |  22.19 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1106.40 ± 9.70 |
| qwen35 27B Q6_K                |  22.19 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         21.65 ± 0.00 |
```

```bash
root@a64d23b65e7b:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/Qwen3.6-27B-GGUF/Qwen3.6-27B-UD-Q5_K_XL.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Medium       |  18.65 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |      1212.84 ± 11.86 |
| qwen35 27B Q5_K - Medium       |  18.65 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         24.94 ± 0.04 |
```

# f16 vs bf16

```bash
root@97e103558474:/# llama-bench -ctk bf16 -ctv bf16 -fa 1 -p 16384 -n 1024 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q4_K_L.gguf 
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------: | -------------------: |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 |  1 |         pp16384 |       1776.62 ± 2.07 |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 |  1 |          tg1024 |         27.89 ± 0.01 |

build: 2098fd6 (1)
root@97e103558474:/# llama-bench -ctk f16 -ctv f16 -fa 1 -p 16384 -n 1024 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q4_K_L.gguf 
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |  1 |         pp16384 |       1793.06 ± 3.54 |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |  1 |          tg1024 |         27.88 ± 0.02 |

build: 2098fd6 (1)
```

# `-sm tensor`

```bash
root@69a054550fc6:/# llama-bench -ctk bf16 -ctv bf16 -fa 1 -p 16384 -n 1024 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q4_K_L.gguf -sm tensor 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | type_k | type_v |     sm | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -----: | -: | --------------: | -------------------: |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 | tensor |  1 |         pp16384 |        537.08 ± 0.02 |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 | tensor |  1 |          tg1024 |         35.12 ± 0.04 |

build: 2098fd6 (1)
```

# NVFP4

```bash
root@b00b7905dc98:/# llama-bench -ctk bf16 -ctv bf16 -fa 1 -p 8192 -n 256 -m /models/Freenixi/Abiray-Qwen3.6-27B-NVFP4.gguf                          
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------: | -------------------: |
| qwen35 27B NVFP4               |  17.50 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 |  1 |          pp8192 |       2614.15 ± 1.04 |
| qwen35 27B NVFP4               |  17.50 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 |  1 |           tg256 |         28.19 ± 0.06 |

build: 2098fd6 (1)
```

# b8998

```bash
root@b00b7905dc98:/# llama-bench -ctk bf16 -ctv bf16 -fa 1 -p 8192 -n 256 -m /models/bartowski/Qwen3.6-27B-GGUF/Qwen_Qwen3.6-27B-Q4_K_L.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------: | -------------------: |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 |  1 |          pp8192 |       1822.26 ± 2.96 |
| qwen35 27B Q4_K - Medium       |  17.20 GiB |    26.90 B | CUDA       |  99 |   bf16 |   bf16 |  1 |           tg256 |         27.91 ± 0.06 |

build: 2098fd6 (1)
```
