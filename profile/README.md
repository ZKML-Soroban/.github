<p align="center">
  <img src="https://raw.githubusercontent.com/ZKML-Soroban/ZKML-Soroban/main/assets/banner-zkml-soroban.svg" alt="ZKML Soroban" width="100%">
</p>

<p align="center"><strong>Verifiable machine learning inference with zero-knowledge proofs on Stellar.</strong></p>

<p align="center">
  <a href="https://github.com/ZKML-Soroban/ZKML-Soroban"><img src="https://img.shields.io/badge/repo-ZKML--Soroban-7D00FF.svg" alt="Repository"></a>
  <a href="https://crates.io/crates/zkml-common"><img src="https://img.shields.io/crates/v/zkml-common.svg?label=zkml-common" alt="zkml-common on crates.io"></a>
  <a href="https://crates.io/crates/zkml-verifier"><img src="https://img.shields.io/crates/v/zkml-verifier.svg?label=zkml-verifier" alt="zkml-verifier on crates.io"></a>
  <a href="https://github.com/ZKML-Soroban/ZKML-Soroban/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-Apache--2.0-blue.svg" alt="Apache 2.0"></a>
</p>

---

### What we build

Credit scores, KYC risk tiers and compliance checks are increasingly decided by machine learning
models, but nobody can check that a claimed result really came from the approved model.

ZKML Soroban runs small ML models off-chain and proves, with zero-knowledge cryptography, that a
specific model produced a specific result on specific inputs. A Soroban smart contract verifies
the proof on Stellar and records the outcome, without revealing the model weights or the input
features. It is built on the Protocol 25 host functions for BN254 (CAP-0074) and Poseidon
(CAP-0075).

### Projects

| Repository | Description |
| ---------- | ----------- |
| [**ZKML-Soroban**](https://github.com/ZKML-Soroban/ZKML-Soroban) | Fixed-point ML inference, ONNX import, RISC Zero zkVM prover and the Soroban Groth16 verifier contract. |

| Crate | Description |
| ----- | ----------- |
| [`zkml-common`](https://crates.io/crates/zkml-common) | Deterministic core: Q16.16 fixed point, models, inference and Poseidon commitments. |
| [`zkml-verifier`](https://crates.io/crates/zkml-verifier) | Soroban contract that verifies Groth16 proofs over BN254 with replay protection. |

### Status

Pre-1.0 and built in the open. Model import, fixed-point inference, Poseidon commitments, zkVM
execution and on-chain Groth16 verification are in place. Wrapping zkVM proofs into Groth16 and
the end-to-end testnet demo are in progress. See the
[roadmap](https://github.com/ZKML-Soroban/ZKML-Soroban/blob/main/docs/project/roadmap.md).

### Where it is going

- **Provable KYC risk scoring:** anchors share a verified risk tier instead of repeating
  compliance work.
- **Credit-gated DeFi:** lending protocols admit borrowers based on a score proven to come from an
  approved model, without seeing the underlying data.
- **Verifiable RWA risk:** buyers of tokenized invoices check a risk assessment without access to
  the model.
- **Post-quantum readiness:** a crypto-agile verifier so attestations stay trustworthy as
  pairing-based cryptography ages. See
  [post-quantum readiness](https://github.com/ZKML-Soroban/ZKML-Soroban/blob/main/docs/security/post-quantum.md).

### Tech stack

`Rust` · `Soroban` · `RISC Zero zkVM` · `Groth16` · `BN254` · `Poseidon` · `ONNX`

### Get involved

- Read the [contributing guide](https://github.com/ZKML-Soroban/ZKML-Soroban/blob/main/CONTRIBUTING.md)
  and the [code of conduct](https://github.com/ZKML-Soroban/ZKML-Soroban/blob/main/CODE_OF_CONDUCT.md).
- Pick an [open issue](https://github.com/ZKML-Soroban/ZKML-Soroban/issues).
- Report security issues privately as described in the
  [security policy](https://github.com/ZKML-Soroban/ZKML-Soroban/blob/main/SECURITY.md).

Licensed under Apache 2.0.
