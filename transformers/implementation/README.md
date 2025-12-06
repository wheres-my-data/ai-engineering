# Transformers — Implementation

This section is for **building transformer components from scratch**.

Planned components:
- A tiny self-attention module (QKᵀ → softmax → V)
- Multi-head attention (minimal version)
- A tiny transformer block (attention + MLP + residual + layer norm)
- Simple decoding functions (greedy, top-k, top-p)

The goal is not to reproduce a full production model, but to:
- Understand each piece by re-implementing it
- Be able to reason about performance, limitations, and design tradeoffs
