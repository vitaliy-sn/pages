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

```bash
root@7db078a5ec54:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/gemma-4-31B-it-GGUF/google_gemma-4-31B-it-Q4_K_L.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| gemma4 ?B Q4_K - Medium        |  18.56 GiB |    30.70 B | CUDA       |  99 |  1 |           pp512 |       1203.55 ± 4.01 |
| gemma4 ?B Q4_K - Medium        |  18.56 GiB |    30.70 B | CUDA       |  99 |  1 |           tg128 |         25.13 ± 0.06 |

build: ff5ef82 (1)
```


# gemma-4-26B-A4B-it

```bash
root@7db078a5ec54:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/gemma-4-26B-A4B-it-GGUF/google_gemma-4-26B-A4B-it-Q6_K_L.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| gemma4 ?B Q6_K                 |  21.44 GiB |    25.23 B | CUDA       |  99 |  1 |           pp512 |      3655.58 ± 18.64 |
| gemma4 ?B Q6_K                 |  21.44 GiB |    25.23 B | CUDA       |  99 |  1 |           tg128 |        101.11 ± 0.97 |

build: ff5ef82 (1)
```

```bash
root@7db078a5ec54:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/gemma-4-26B-A4B-it-GGUF/google_gemma-4-26B-A4B-it-Q5_K_L.gguf 
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| gemma4 ?B Q5_K - Medium        |  18.14 GiB |    25.23 B | CUDA       |  99 |  1 |           pp512 |      3900.60 ± 24.77 |
| gemma4 ?B Q5_K - Medium        |  18.14 GiB |    25.23 B | CUDA       |  99 |  1 |           tg128 |        110.14 ± 1.15 |

build: ff5ef82 (1)

root@7db078a5ec54:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/gemma-4-26B-A4B-it-GGUF/google_gemma-4-26B-A4B-it-Q5_K_L.gguf -p 16384 -n 4096
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| gemma4 ?B Q5_K - Medium        |  18.14 GiB |    25.23 B | CUDA       |  99 |  1 |         pp16384 |      5832.07 ± 23.05 |
| gemma4 ?B Q5_K - Medium        |  18.14 GiB |    25.23 B | CUDA       |  99 |  1 |          tg4096 |        106.23 ± 0.17 |

build: ff5ef82 (1)
```


