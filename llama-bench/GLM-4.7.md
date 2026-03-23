# GLM-4.7

```bash
root@aea4539ed481:/app# ./llama-bench -ctk q4_0 -ctv q4_0 -fa 1 -m /models/bartowski/GLM-4.7-GGUF/zai-org_GLM-4.7-IQ2_XXS-00001-of-00003.gguf -ngl 30
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------: | -------------------: |
| glm4moe 355B.A32B IQ2_XXS - 2.0625 bpw |  82.68 GiB |   358.34 B | CUDA       |  30 |   q4_0 |   q4_0 |  1 |           pp512 |         87.66 ± 0.47 |
| glm4moe 355B.A32B IQ2_XXS - 2.0625 bpw |  82.68 GiB |   358.34 B | CUDA       |  30 |   q4_0 |   q4_0 |  1 |           tg128 |          3.63 ± 0.01 |

build: 4efd326 (1)


root@aea4539ed481:/app# ./llama-bench -ctk q4_0 -ctv q4_0 -fa 1 -m /models/bartowski/GLM-4.7-GGUF/zai-org_GLM-4.7-IQ2_XXS-00001-of-00003.gguf -ot ".([0-7].ffn_up|[0-7].ffn_down|[0-7].ffn_gate)_exps.=CPU"
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------------- | --------------: | -------------------: |
| glm4moe 355B.A32B IQ2_XXS - 2.0625 bpw |  82.68 GiB |   358.34 B | CUDA       |  99 |   q4_0 |   q4_0 |  1 | .([0-7].ffn_up|[0-7].ffn_down|[0-7].ffn_gate)_exps.=CPU |           pp512 |         81.06 ± 0.43 |
| glm4moe 355B.A32B IQ2_XXS - 2.0625 bpw |  82.68 GiB |   358.34 B | CUDA       |  99 |   q4_0 |   q4_0 |  1 | .([0-7].ffn_up|[0-7].ffn_down|[0-7].ffn_gate)_exps.=CPU |           tg128 |          5.78 ± 0.00 |

build: 4efd326 (1)


root@aea4539ed481:/app# ./llama-bench -ctk q4_0 -ctv q4_0 -fa 1 -m /models/bartowski/GLM-4.7-GGUF/zai-org_GLM-4.7-IQ2_XXS-00001-of-00003.gguf -ot ".([0-6].ffn_up|[0-6].ffn_down|[0-7].ffn_gate)_exps.=CPU"
ggml_cuda_init: found 2 CUDA devices (Total VRAM: 31658 MiB):
  Device 0: NVIDIA GeForce RTX 5070 Ti, compute capability 12.0, VMM: yes, VRAM: 15808 MiB
  Device 1: NVIDIA GeForce RTX 5060 Ti, compute capability 12.0, VMM: yes, VRAM: 15850 MiB
| model                          |       size |     params | backend    | ngl | type_k | type_v | fa | ot                    |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | --: | -----: | -----: | -: | --------------------- | --------------: | -------------------: |
| glm4moe 355B.A32B IQ2_XXS - 2.0625 bpw |  82.68 GiB |   358.34 B | CUDA       |  99 |   q4_0 |   q4_0 |  1 | .([0-6].ffn_up|[0-6].ffn_down|[0-7].ffn_gate)_exps.=CPU |           pp512 |         85.58 ± 0.46 |
| glm4moe 355B.A32B IQ2_XXS - 2.0625 bpw |  82.68 GiB |   358.34 B | CUDA       |  99 |   q4_0 |   q4_0 |  1 | .([0-6].ffn_up|[0-6].ffn_down|[0-7].ffn_gate)_exps.=CPU |           tg128 |          6.16 ± 0.02 |

build: 4efd326 (1)

```
