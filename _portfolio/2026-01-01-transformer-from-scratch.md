---
Title: "Transformer from Scratch: Encoder–Decoder Architecture in PyTorch"
excerpt: "A full encoder–decoder Transformer implemented from first principles, verified against PyTorch's reference attention to zero deviation."
collection: portfolio
date: 2026-01-01
---

**Tools:** Python (PyTorch, NumPy, Matplotlib), Jupyter

Implemented the complete encoder–decoder Transformer from *Attention Is All You Need* from first principles: multi-head attention, sinusoidal positional encoding, and causal and padding masks, built using only `nn.Linear` and tensor operations. Verified to 0.00e+00 maximum absolute deviation against `torch.nn.MultiheadAttention` under copied weights.

Trained a 932K-parameter model to 99.8% exact-match accuracy on a sequence-reversal task under free-running greedy decoding, reaching that in 3,000 steps and roughly 4.5 minutes on CPU. Getting there required pre-norm residuals, Noam learning-rate warmup, label smoothing, and weight tying. Cross-attention recovered the correct anti-diagonal alignment with no attention supervision.

[View on GitHub](https://github.com/tayaba02/Building-transformer-model-from-scratch)
