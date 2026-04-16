## build: 463b6a9

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

root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q3_K_S.gguf
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      1490.63 ± 35.59 |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |         45.59 ± 0.02 |

root@c5cf8d322703:/app# ./llama-bench -dev CUDA1 -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q3_K_S.gguf
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA1        |           pp512 |        849.76 ± 8.98 |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA1        |           tg128 |         26.21 ± 0.03 |

root@c5cf8d322703:/app# ./llama-bench -dev CUDA0 -ctk f16 -ctv f16 -fa 1 -m /models/Jackrong/Qwen3.5-27B-Claude-4.6-Opus-Reasoning-Distilled-GGUF/Qwen3.5-27B.Q3_K_M.gguf
| model                          |       size |     params | backend    | ngl | fa | dev          |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | ------------ | --------------: | -------------------: |
| qwen35 27B Q3_K - Medium       |  12.37 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           pp512 |      1562.24 ± 33.71 |
| qwen35 27B Q3_K - Medium       |  12.37 GiB |    26.90 B | CUDA       |  99 |  1 | CUDA0        |           tg128 |         45.21 ± 0.04 |
```


## build: 990e4d9

```bash
root@94f1374dc896:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q5_K_S.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Small        |  17.79 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1249.66 ± 0.61 |
| qwen35 27B Q5_K - Small        |  17.79 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         24.14 ± 0.03 |

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


## build: ff5ef82 (b8763)

```
root@d28752cfae71:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q3_K_S.gguf
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31692 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15842 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1105.55 ± 9.38 |
| qwen35 27B Q3_K - Small        |  11.76 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         33.16 ± 0.07 |

root@d28752cfae71:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q4_K_M.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q4_K - Medium       |  15.94 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |      1269.32 ± 12.86 |
| qwen35 27B Q4_K - Medium       |  15.94 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         28.47 ± 0.04 |

root@d28752cfae71:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q5_K_S.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Small        |  17.79 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |      1270.67 ± 13.07 |
| qwen35 27B Q5_K - Small        |  17.79 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         26.14 ± 0.05 |

root@d28752cfae71:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q5_K_M.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Medium       |  18.57 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |      1219.94 ± 11.83 |
| qwen35 27B Q5_K - Medium       |  18.57 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         25.04 ± 0.07 |

root@d28752cfae71:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q5_K_L.gguf
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q5_K - Medium       |  19.30 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |      1219.06 ± 12.62 |
| qwen35 27B Q5_K - Medium       |  19.30 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         24.63 ± 0.00 |

root@d28752cfae71:/# llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3.5-27B-GGUF/Qwen_Qwen3.5-27B-Q6_K.gguf  
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen35 27B Q6_K                |  21.49 GiB |    26.90 B | CUDA       |  99 |  1 |           pp512 |       1102.83 ± 8.17 |
| qwen35 27B Q6_K                |  21.49 GiB |    26.90 B | CUDA       |  99 |  1 |           tg128 |         22.10 ± 0.01 |

```
