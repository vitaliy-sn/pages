```bash
root@a464313645e1:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.6-35B-A3B-GGUF/Qwen_Qwen3.6-35B-A3B-Q5_K_L.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2985.85 ± 12.10 |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        115.78 ± 1.54 |

build: ff5ef82 (1)
```

```bash
root@a464313645e1:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/Qwen3.6-35B-A3B-UD-Q6_K.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q6_K         |  27.05 GiB |    34.66 B | CUDA       |  99 |  1 |           pp512 |      2688.95 ± 10.51 |
| qwen35moe 35B.A3B Q6_K         |  27.05 GiB |    34.66 B | CUDA       |  99 |  1 |           tg128 |        113.86 ± 1.63 |

build: ff5ef82 (1)
```

```bash
root@b00b7905dc98:/# llama-bench -ctk bf16 -ctv bf16 -fa 1 -p 16384 -n 1024 -m /models/bartowski/Qwen3.6-35B-A3B-GGUF/Qwen_Qwen3.6-35B-A3B-Q5_K_L.gguf 
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |   bf16 |   bf16 |  1 |         pp16384 |      5204.29 ± 21.08 |
| qwen35moe 35B.A3B Q5_K - Medium |  23.58 GiB |    34.66 B | CUDA       |  99 |   bf16 |   bf16 |  1 |          tg1024 |        124.68 ± 0.61 |

build: 2098fd6 (1)

root@b00b7905dc98:/# llama-bench -ctk bf16 -ctv bf16 -fa 1 -p 16384 -n 1024 -m /models/Qwen3.6-35B-A3B-NVFP4-GGUF.gguf
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------: | -------------------: |
| qwen35moe 35B.A3B NVFP4        |  20.94 GiB |    34.66 B | CUDA       |  99 |   bf16 |   bf16 |  1 |         pp16384 |       5127.26 ± 4.31 |
| qwen35moe 35B.A3B NVFP4        |  20.94 GiB |    34.66 B | CUDA       |  99 |   bf16 |   bf16 |  1 |          tg1024 |         88.10 ± 0.38 |

build: 2098fd6 (1)

```
