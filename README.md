# MBSE-CPS-Security-Toolchain

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/你的用户名/mbse-cps-security-toolchain)](https://github.com/Qieqienia/mbse-cps-security-toolchain/issues)

**MBSE-driven predictive security analysis for networked Cyber-Physical Systems: from SysML to attack graphs with cryptographic semantics.**

This toolchain provides an end-to-end workflow:
- Model system architecture in **Eclipse Papyrus (SysML)**
- Automatically transform to **MulVAL** input facts using **Acceleo** MTT
- Generate attack graphs and quantify **attack success probability** of critical assets
- Compare security mechanisms (VPN/TLS/TEE) via **cryptographic semantic control layer**

## 📦 Repository Structure

| Folder | Description |
|--------|-------------|
| `SysML_Extension_for_MulVAL` | SysML profile for security annotations |
| `org.eclipse.aceleo.module.sample` | Acceleo MTT templates |
| `mulval` | Extended MulVAL reasoner |
| `UAV-simple` | UAV case study model |
| `chu-Enhanced` | CHU hospital ventilation model (with VPN/TLS/TEE) |
| `tableau` | Attack graph visualizer |

## 🚀 Quick Start

### Prerequisites
- Java 11+, Eclipse Papyrus 2020-03+, Acceleo 3.x
- Graphviz (`apt install graphviz` or `brew install graphviz`)

### Run the UAV example
1. Import `UAV-simple` into Papyrus.
2. Run Acceleo transformation → generates `facts.P` file.
3. Run MulVAL: `mulval -f facts.P -a > attack_graph.dot`
4. Visualize: `dot -Tpng attack_graph.dot -o attack_graph.png`

See [docs/SETUP.md](docs/SETUP.md) for detailed instructions.

## 📝 Citation

If you use this toolchain, please cite the associated paper:

```bibtex
@article{yourname2026mbse,
  title={MBSE-Driven Predictive Security Analysis for Networked CPS: A Cryptographic Semantic Control Layer and Risk Assessment Approach},
  author={Your Name and Others},
  journal={...},
  year={2026}
}
