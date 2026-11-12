# Zhiqiang Wang

我正在学习 GPU 编程与大模型推理系统，重点做 CUDA kernel、正确性验证和性能分析。这里记录可复现的实验与独立完成的工具项目。

## 代表项目

- **[LLM 推理系统练习](https://github.com/Thymos2027/llm-inference-lab)**：从 naive 到 shared memory、register tiling 逐步实现 FP32 CUDA 矩阵乘法，并用 CUDA Event、Nsight 和 SASS 分析结果。在 RTX 5060 Ti 上，`1024³` 的 register tiling kernel 相对同程序 tiled 基线为 `2.68×`；[测量条件、正确性检查和不适用的形状](https://github.com/Thymos2027/llm-inference-lab/blob/main/01-cuda-matmul/BENCHMARKS.md)均有记录。该结果仅针对矩阵乘法 kernel，不代表完整模型推理吞吐。
- **[期刊个人归档工具](https://github.com/Thymos2027/periodical-archiver)**：用 Playwright 采集已获授权阅读的期刊内容，生成 EPUB、PDF、TXT、封面和摘要，支持失败记录与断点续抓。

当前的推理系统实验持续更新中，代码、构建方式和性能记录以项目仓库为准。
