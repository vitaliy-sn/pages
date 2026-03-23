# llama.cpp

```bash
root@e63e39a0d495:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/Qwen3-Coder-Next-UD-IQ3_S.gguf,/models/unsloth/Qwen3-Coder-Next-UD-IQ3_XXS.gguf,/models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q2_K_L.gguf
| model                                  |       size |     params | backend    | ngl | fa |            test |                  t/s |
| -------------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B IQ3_S - 3.4375 bpw   |  27.65 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |      1535.26 ± 10.85 |
| qwen3next 80B.A3B IQ3_S - 3.4375 bpw   |  27.65 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         69.89 ± 0.10 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  26.52 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |      1541.30 ± 17.86 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  26.52 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         70.77 ± 0.40 |
| qwen3next 80B.A3B Q2_K - Medium        |  26.51 GiB |    79.67 B | CUDA       |  99 |  1 |           pp512 |      1374.31 ± 10.20 |
| qwen3next 80B.A3B Q2_K - Medium        |  26.51 GiB |    79.67 B | CUDA       |  99 |  1 |           tg128 |         75.68 ± 0.33 |

build: a69d54f (1)

root@b7d7de86a1a8:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_K_L.gguf -ngl 30
| model                           |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  30 |  1 |           pp512 |        397.30 ± 4.48 |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  30 |  1 |           tg128 |         27.23 ± 0.18 |

build: a69d54f (1)
root@b7d7de86a1a8:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_K_L.gguf -ot ".([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU"
| model                           |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU |           pp512 |        446.66 ± 4.90 |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU |           tg128 |         49.06 ± 0.65 |

build: a69d54f (1)
```


```bash
root@9e685f4a4209:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-IQ4_XS.gguf -ngl 34
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------: | -------------------: |
| qwen3next 80B.A3B IQ4_XS - 4.25 bpw |  39.90 GiB |    79.67 B | CUDA       |  34 |  1 |           pp512 |        520.68 ± 6.03 |
| qwen3next 80B.A3B IQ4_XS - 4.25 bpw |  39.90 GiB |    79.67 B | CUDA       |  34 |  1 |           tg128 |         32.96 ± 0.48 |

build: 1e64534 (1)
```

```bash
root@9e685f4a4209:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-IQ4_XS.gguf -ot ".([0-2].ffn_up|[0-2].ffn_down|[0-2].ffn_gate)_exps.=CPU"ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B IQ4_XS - 4.25 bpw |  39.90 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-2].ffn_up|[0-2].ffn_down|[0-2].ffn_gate)_exps.=CPU |           pp512 |        618.79 ± 8.28 |
| qwen3next 80B.A3B IQ4_XS - 4.25 bpw |  39.90 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-2].ffn_up|[0-2].ffn_down|[0-2].ffn_gate)_exps.=CPU |           tg128 |         57.42 ± 0.87 |

build: 1e64534 (1)
```



```bash
root@9e685f4a4209:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q3_K_M.gguf -ot ".([0-1].ffn_up|[0-1].ffn_down|[0-1].ffn_gate)_exps.=CPU"ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B Q3_K - Medium |  34.13 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-1].ffn_up|[0-1].ffn_down|[0-1].ffn_gate)_exps.=CPU |           pp512 |        802.88 ± 8.57 |
| qwen3next 80B.A3B Q3_K - Medium |  34.13 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-1].ffn_up|[0-1].ffn_down|[0-1].ffn_gate)_exps.=CPU |           tg128 |         67.11 ± 1.45 |

build: 1e64534 (1)
```


```bash
root@9e685f4a4209:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-IQ3_XS.gguf -ot ".([0].ffn_up|[0].ffn_down|[0].ffn_gate)_exps.=CPU"ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B IQ3_XS - 3.3 bpw |  30.76 GiB |    79.67 B | CUDA       |  99 |  1 | .([0].ffn_up|[0].ffn_down|[0].ffn_gate)_exps.=CPU |           pp512 |       1170.54 ± 9.47 |
| qwen3next 80B.A3B IQ3_XS - 3.3 bpw |  30.76 GiB |    79.67 B | CUDA       |  99 |  1 | .([0].ffn_up|[0].ffn_down|[0].ffn_gate)_exps.=CPU |           tg128 |         67.20 ± 2.39 |

build: 1e64534 (1)
```


```bash
root@9e685f4a4209:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-IQ3_XXS.gguf -ot ".([0].ffn_up|[0].ffn_down)_exps.=CPU"
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  29.54 GiB |    79.67 B | CUDA       |  99 |  1 | .([0].ffn_up|[0].ffn_down)_exps.=CPU |           pp512 |      1296.08 ± 10.62 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  29.54 GiB |    79.67 B | CUDA       |  99 |  1 | .([0].ffn_up|[0].ffn_down)_exps.=CPU |           tg128 |         75.82 ± 0.90 |

build: 1e64534 (1)
```


```bash
root@9e685f4a4209:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/Qwen3-Coder-Next-MXFP4_MOE.gguf -ot ".([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU"
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B MXFP4 MoE    |  44.73 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU |           pp512 |        488.52 ± 5.07 |
| qwen3next 80B.A3B MXFP4 MoE    |  44.73 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU |           tg128 |         44.76 ± 0.99 |

build: 1e64534 (1)
```


```bash
root@9e685f4a4209:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/Qwen3-Coder-Next-UD-Q4_K_S.gguf -ot ".([0-3].ffn_up|[0-2].ffn_down|[0-3].ffn_gate)_exps.=CPU"
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B Q4_K - Small |  42.91 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-2].ffn_down|[0-3].ffn_gate)_exps.=CPU |           pp512 |        502.70 ± 5.97 |
| qwen3next 80B.A3B Q4_K - Small |  42.91 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-2].ffn_down|[0-3].ffn_gate)_exps.=CPU |           tg128 |         49.73 ± 0.22 |

build: 1e64534 (1)
```


```bash
root@69da3d387c95:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_K_M.gguf -ot ".([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU"ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B Q4_K - Medium |  45.38 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU |           pp512 |        446.51 ± 4.34 |
| qwen3next 80B.A3B Q4_K - Medium |  45.38 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU |           tg128 |         50.31 ± 1.26 |

build: 990e4d9 (1)
```


```bash
root@69da3d387c95:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_K_S.gguf -ot ".([0-3].ffn_up|[0-3].ffn_down|[0-2].ffn_gate)_exps.=CPU"ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B Q4_K - Small |  43.70 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-2].ffn_gate)_exps.=CPU |           pp512 |        496.24 ± 5.37 |
| qwen3next 80B.A3B Q4_K - Small |  43.70 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-2].ffn_gate)_exps.=CPU |           tg128 |         52.80 ± 0.84 |

build: 990e4d9 (1)
```


```bash
root@69da3d387c95:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_0.gguf -ot ".([0-3].ffn_up|[0-3].ffn_down|[0-2].ffn_gate)_exps.=CPU"ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -: | --------------------- | --------------: | -------------------: |
| qwen3next 80B.A3B Q4_0         |  42.93 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-2].ffn_gate)_exps.=CPU |           pp512 |        500.36 ± 4.55 |
| qwen3next 80B.A3B Q4_0         |  42.93 GiB |    79.67 B | CUDA       |  99 |  1 | .([0-3].ffn_up|[0-3].ffn_down|[0-2].ffn_gate)_exps.=CPU |           tg128 |         52.93 ± 0.48 |

build: 990e4d9 (1)
```



# ik_llama.cpp

```bash
root@57ca4b351df4:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/unsloth/Qwen3-Coder-Next-UD-IQ3_S.gguf,/models/unsloth/Qwen3-Coder-Next-UD-IQ3_XXS.gguf,/models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q2_K_L.gguf
| model                                  |       size |     params | backend    | ngl |          test |              t/s |
| -------------------------------------- | ---------: | ---------: | ---------- | --: | ------------: | ---------------: |
| qwen3next 80B.A3B IQ3_S - 3.4375 bpw   |  27.65 GiB |    79.67 B | CUDA       | 999 |         pp512 | 1611.86 ± 128.25 |
| qwen3next 80B.A3B IQ3_S - 3.4375 bpw   |  27.65 GiB |    79.67 B | CUDA       | 999 |         tg128 |    113.99 ± 1.76 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  26.52 GiB |    79.67 B | CUDA       | 999 |         pp512 |  1642.17 ± 37.00 |
| qwen3next 80B.A3B IQ3_XXS - 3.0625 bpw |  26.52 GiB |    79.67 B | CUDA       | 999 |         tg128 |    111.86 ± 1.39 |
| qwen3next 80B.A3B Q2_K - Medium        |  26.51 GiB |    79.67 B | CUDA       | 999 |         pp512 | 1398.67 ± 104.10 |
| qwen3next 80B.A3B Q2_K - Medium        |  26.51 GiB |    79.67 B | CUDA       | 999 |         tg128 |    118.34 ± 1.69 |

build: 9015b6c (1)

root@57ca4b351df4:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_K_L.gguf -ngl 30

| model                           |       size |     params | backend    | ngl |          test |              t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | ------------: | ---------------: |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  30 |         pp512 |   440.56 ± 16.18 |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       |  30 |         tg128 |     26.66 ± 0.22 |

build: 9015b6c (1)

root@57ca4b351df4:/app# ./llama-bench -ctk f16 -ctv f16 -fa 1 -m /models/bartowski/Qwen3-Coder-Next-GGUF/Qwen_Qwen3-Coder-Next-Q4_K_L.gguf -ot ".([0-3].ffn_up|[0-3].ffn_down|[0-3].ffn_gate)_exps.=CPU"
| model                           |       size |     params | backend    | ngl |          test |              t/s |
| ------------------------------- | ---------: | ---------: | ---------- | --: | ------------: | ---------------: |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       | 999 |         pp512 |   433.90 ± 14.16 |
| qwen3next 80B.A3B Q4_K - Medium |  45.59 GiB |    79.67 B | CUDA       | 999 |         tg128 |     54.20 ± 1.00 |

build: 9015b6c (1)
```
