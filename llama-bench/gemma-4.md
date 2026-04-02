# gemma-4-31B-it

```bash
root@377289074a67:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/gemma-4-31B-it-GGUF/google_gemma-4-31B-it-Q4_K_L.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| gemma4 ?B Q4_K - Medium        |  18.56 GiB |    30.70 B | CUDA       |  99 |  1 |           pp512 |       1203.63 ± 4.71 |
| gemma4 ?B Q4_K - Medium        |  18.56 GiB |    30.70 B | CUDA       |  99 |  1 |           tg128 |         25.10 ± 0.01 |

build: 5803c8d (1)

```
