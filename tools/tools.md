# Tools and Libraries

Verified software and frameworks useful for computing token-level uncertainty and building hallucination detectors.

---

### LM-Polygraph
Open-source Python toolkit consolidating 40+ state-of-the-art uncertainty quantification and calibration methods for LLMs (token probability-based, semantic, ensemble, and internal-state estimators), with a unified benchmark for consistent evaluation.
🔗 [github.com/IINemo/lm-polygraph](https://github.com/IINemo/lm-polygraph)

### SelfCheckGPT (Python package)
Reference implementation of the SelfCheckGPT consistency-checking framework, including BERTScore, QA, n-gram, NLI, and LLM-prompting variants. Commonly used as a black-box baseline against token-level uncertainty methods.
🔗 [github.com/potsawee/selfcheckgpt](https://github.com/potsawee/selfcheckgpt)

### Hugging Face Transformers
Provides `output_scores=True` / `output_logits=True` generation utilities to extract per-token logits and probabilities directly from `model.generate()`, which is the practical starting point for computing any token-level uncertainty metric.
🔗 [github.com/huggingface/transformers](https://github.com/huggingface/transformers)

### vLLM
High-throughput, memory-efficient LLM inference engine that exposes log-probabilities as part of its output API, making it practical to compute token-level uncertainty at scale (batched, production-style inference) rather than only in small research scripts.
🔗 [github.com/vllm-project/vllm](https://github.com/vllm-project/vllm)

### Weights & Biases (wandb)
Experiment-tracking tool used by several uncertainty-quantification research codebases (e.g., the semantic uncertainty / semantic entropy pipeline) to log, visualize, and compare uncertainty-estimation runs across models and datasets.
🔗 [github.com/wandb/wandb](https://github.com/wandb/wandb)
