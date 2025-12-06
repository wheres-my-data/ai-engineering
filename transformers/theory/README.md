# Transformers — Theory

This section is for **core concepts and mental models** behind transformer architectures.  
These notes aim for clarity, intuition, and structural understanding — before touching code.

## 📘 Planned Topics

### 1. Tokenization
- Why models operate on tokens, not characters or words
- Byte-Pair Encoding (BPE) and other tokenization methods  
- How text becomes a sequence of integers  

### 2. Embeddings
#### **WTE — Word Token Embedding**
- Mapping token IDs → dense vectors  
- Why embedding space encodes semantic similarity

#### **WPE — Word Position Embedding**
- How transformers learn positional information  
- Absolute vs relative position embeddings  
- Why attention is “order-agnostic” without them  

### 3. Self-Attention (Q, K, V)
- What problem attention solves  
- Intuition for Query / Key / Value  
- Why attention is “soft lookup”  
- Dot-product attention: QKᵀ → softmax → V  
- Masked attention for autoregressive models  

### 4. Multi-Head Attention & Residual Connections
- Why multiple heads capture different patterns  
- How heads are projected and concatenated  
- Why residual/skip connections stabilize training  
- Add → Norm sequence and its importance  

### 5. Transformer Block Structure
- LayerNorm placement (“pre-norm” vs “post-norm”)  
- MLP feed-forward network (two linear layers + nonlinearity)  
- Quick overview of common activation functions (GELU, ReLU)  
- Full block = Attention → MLP → Skip connections → LayerNorm  

### 6. Logits
- What logits actually represent  
- Why they are unnormalized scores  
- Relationship between logits and probability distributions  

### 7. Softmax
- Converting logits into probabilities  
- Temperature scaling  
- Why softmax is used for attention & decoding  
- Numerical stability tricks (subtract max, etc.)  

---

## 🎯 Purpose of This Section
To build a **clean, complete transformer intuition** that makes it easier to:

- understand what models *actually compute*  
- debug / reason about model behavior  
- implement simplified transformer modules from scratch  
- meaningfully use transformers in real tasks (see Practice)  
- build your own tiny attention / tiny block (see Implementation)

This is the *mental map* before touching code.
