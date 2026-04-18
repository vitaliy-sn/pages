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
