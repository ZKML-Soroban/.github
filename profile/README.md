<p align="center">
  <img src="https://raw.githubusercontent.com/ZKML-Soroban/ZKML-Soroban/main/assets/logo.png" alt="ZKML-Soroban" width="180">
</p>

<h1 align="center">ZKML-Soroban</h1>

<p align="center"><strong>Provable machine learning inference for Stellar.</strong></p>

<p align="center">
  Run small ML models off-chain and verify the correctness of their inference
  on-chain with zero-knowledge proofs on Soroban smart contracts.
</p>

---

### What we build

A prover runs an ML model off-chain and produces a Groth16 zero-knowledge proof.
A Soroban smart contract verifies that proof on-chain with a single cheap
cryptographic check, using the BN254 (CAP-0074) and Poseidon (CAP-0075) host
functions introduced in Stellar Protocol 25. This lets anyone prove that a
specific model produced a specific result, without revealing the model weights
or the input data.

### Flagship project

| Repository | Description |
| ---------- | ----------- |
| [**ZKML-Soroban**](https://github.com/ZKML-Soroban/ZKML-Soroban) | The provable ML inference runtime: off-chain prover, shared types, and the on-chain verifier contract. |

### Use cases

- **Provable KYC risk scoring** — anchors share verifiable risk assessments instead of duplicating compliance work.
- **Invoice risk assessment (RWA)** — buyers verify a tokenized invoice's risk score without accessing the model or data.
- **Privacy-preserving credit scoring** — users prove a score clears a threshold without revealing it.

### Tech stack

`Rust` · `Soroban` · `RISC Zero zkVM` · `Groth16` · `BN254` · `Poseidon` · `ONNX`

### Get involved

We build in the open under Apache 2.0. Browse the
[issues](https://github.com/ZKML-Soroban/ZKML-Soroban/issues) (look for `good first issue`)
and the [contributing guide](https://github.com/ZKML-Soroban/ZKML-Soroban/blob/main/CONTRIBUTING.md).
