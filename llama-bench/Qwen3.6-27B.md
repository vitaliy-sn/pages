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
