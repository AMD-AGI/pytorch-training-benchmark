# Security Policy

This repository (`AMD-AGI/pytorch-training-benchmark`) contains benchmarking
and fine-tuning scripts for PyTorch on AMD Instinct GPUs. We take security
seriously even for benchmark / research code, because the scripts are
frequently copy-pasted into production environments.

## Supported versions

Only the `main` branch is actively maintained. Security fixes will land on
`main`; we do not back-port to historical tags or branches.

| Version | Supported          |
| ------- | ------------------ |
| `main`  | :white_check_mark: |
| other   | :x:                |

## Reporting a vulnerability

**Please do not open a public GitHub issue, discussion, or pull request for
security-sensitive reports.** Public disclosure before a fix is available puts
users at risk.

Use one of the following private channels instead:

1. **GitHub private vulnerability reporting** (preferred): use the
   "Report a vulnerability" button under the
   [Security tab](https://github.com/AMD-AGI/pytorch-training-benchmark/security)
   of this repository. Reports go directly to the maintainers.
2. **AMD Product Security Incident Response Team (PSIRT)**: for
   vulnerabilities that may also affect AMD hardware, drivers, ROCm, or other
   AMD products, follow AMD's product-security disclosure process at
   <https://www.amd.com/en/resources/product-security.html>.

When reporting, please include:

- A clear description of the issue and its impact.
- Affected files / commits / versions (commit SHA on `main` is ideal).
- Steps to reproduce, ideally with a minimal proof-of-concept.
- Your assessment of severity (CVSS vector if you have one).
- Whether you intend to publish a write-up, and your preferred timeline.

## Out of scope

The following are **not** considered security vulnerabilities in this
repository:

- Performance regressions or convergence differences between hardware
  generations or PyTorch / ROCm versions.
- Misconfigurations introduced by users editing the example launch scripts
  (`wikitext_finetune.sh`, `wikitext_lora_finetune.sh`) or YAML recipes.
- Issues that exist solely in upstream dependencies (PyTorch, torchtune,
  Transformer Engine, Hugging Face datasets, etc.). Please report those to
  the corresponding upstream project. We will still help triage if the
  vulnerability is exposed through this repo.
- Findings that require an attacker to already have root / `sudo` access on
  the training node, since the documented setup runs in a privileged docker
  container by design.

## Safe-harbor

We will not pursue legal action against researchers who:

- Make a good-faith effort to follow this policy.
- Avoid privacy violations, data destruction, and service degradation.
- Give us reasonable time to remediate before public disclosure.

Thank you for helping keep AMD's open-source PyTorch tooling secure.
