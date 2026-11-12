<p align="center">
  <img src="./assets/hero.svg" alt="Zhiqiang Wang — LLM Inference and GPU Systems" width="100%" />
</p>

<p align="center">
  <strong>GPU Programming · LLM Inference Systems · Reproducible Experiments</strong>
</p>

I am learning GPU programming and LLM inference systems, with a focus on CUDA kernel implementation, correctness checks, and performance analysis. This page highlights projects with inspectable code, measurement methods, and results.

## Selected Projects

| [LLM Inference Lab](https://github.com/Thymos2027/llm-inference-lab) | [Periodical Archiver](https://github.com/Thymos2027/periodical-archiver) |
| :--- | :--- |
| Implemented FP32 CUDA matrix multiplication kernels from a naive baseline through shared memory and register tiling; analyzed performance with CUDA Events, Nsight, and SASS. | Built a Playwright workflow for archiving periodicals available through an authorized account. It produces EPUB, PDF, TXT, covers, and issue summaries, with failure tracking and resumable fetching. |
| `CUDA` `C++` `GPU Profiling` | `JavaScript` `Playwright` `Automation` |

### A Reproducible Benchmark

On an RTX 5060 Ti, the register tiling kernel reached a median time of **0.402 ms** for `1024³` matrix multiplication, a **2.68×** speedup over the tiled baseline measured in the same program. For the `M=1` shape, the same kernel was slower. [See the measurement conditions, correctness checks, and full results →](https://github.com/Thymos2027/llm-inference-lab/blob/main/01-cuda-matmul/BENCHMARKS.md)

> These are FP32 matrix multiplication kernel timings, not end-to-end model inference throughput.
