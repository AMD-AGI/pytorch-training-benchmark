# Product Vulnerability Reporting (PVR)

## Status: Not applicable

This repository is **not a product** and is **not intended for production
use**. It contains internal benchmarking and fine-tuning scripts for
PyTorch on AMD Instinct GPUs (Llama 3.1 / Mistral pre-training with FSDP
and Torchtune fine-tuning recipes), used to measure performance and
characterize hardware. The code is meant to be run inside a privileged
docker container on a trusted training node by AMD engineers and
collaborators — it does not ship a network service, an authentication
layer, or any user-data store.

For that reason, AMD's formal **Product Vulnerability Reporting (PVR)**
process **does not apply** to this repository. We do not maintain a PSIRT
case queue, a CVE pipeline, or a coordinated-disclosure SLA for this
codebase.

## Where to report issues anyway

If you still find something that looks security-relevant, please use the
project-level intake instead of the AMD PVR / PSIRT channel:

- **Repository security policy** — [SECURITY.md](./SECURITY.md)
- **GitHub private vulnerability reporting** — the "Report a vulnerability"
  button on the repository's
  [Security tab](https://github.com/AMD-AGI/pytorch-training-benchmark/security)
- **Code owners** — [.github/CODEOWNERS](./.github/CODEOWNERS)

If a finding actually affects an AMD **product** (hardware, firmware,
driver, ROCm, etc.) rather than this benchmarking repo, please redirect
the report to AMD PSIRT directly:
<https://www.amd.com/en/resources/product-security.html>.
