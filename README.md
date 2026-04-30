> **Fork notice (kicrazom/ddtree)**
>
> This is a personal fork maintained by Łukasz Minarowski (UMB Białystok)
> for evaluation of a possible ROCm / AMD RDNA 4 (gfx1201) port. The fork
> exists to preserve a stable snapshot of the upstream codebase as of the
> fork date and to host any future port-related branches in isolation.
>
> **Status:** evaluation only — no port work has been performed yet.
> The `master` branch tracks upstream (liranringel/ddtree) unmodified.
> Any ROCm-specific work, if pursued, will live on a separate branch
> (e.g. `rocm-gfx1201`) and will not be merged back upstream without
> coordination with the original authors.
>
> **Why this fork exists:** the [NaviMed-UMB](https://github.com/kicrazom/navimed-umb)
> project benchmarks LLM inference on dual AMD Radeon AI PRO R9700 GPUs.
> Speculative decoding via DDTree is a candidate technique for a future
> follow-up study, but porting and validation on ROCm have not yet been
> performed.
>
> **All credit and authorship for DDTree belong to Liran Ringel and Yaniv Romano.**
> This fork makes no claim of contribution to the original method. Please
> cite the original paper (see Citation section below) and direct any
> questions about DDTree itself to the upstream repository.
>
> ---

<h1 align="center">DDTree</h1>

<p align="center">
  Official implementation of <strong>DDTree (Diffusion Draft Tree)</strong> from
  <em>Accelerating Speculative Decoding with Block Diffusion Draft Trees</em>.
</p>

<p align="center">
  Liran Ringel, Yaniv Romano
</p>

<p align="center">
  <a href="https://liranringel.github.io/ddtree/">🌐 Project Page</a>
  &nbsp;|&nbsp;
  <a href="https://arxiv.org/abs/2604.12989">📄 Paper</a>
</p>

## Setup

This codebase is intended for a CUDA-enabled PyTorch environment.

```bash
pip install -r requirements.txt
```

## Run Experiments

```bash
bash run_benchmark.sh
```

This produces benchmark outputs in `runs/` and logs in `logs/`.

## Reproduce Paper Artifacts

Generate the plots:

```bash
python3 plot_results.py
```

Generate the LaTeX table:

```bash
python3 make_latex_table.py
```

## Citation

```bibtex
@article{ringel2026ddtree,
  title={Accelerating Speculative Decoding with Block Diffusion Draft Trees},
  author={Ringel, Liran and Romano, Yaniv},
  journal={arXiv preprint arXiv:2604.12989},
  year={2026}
}
```
