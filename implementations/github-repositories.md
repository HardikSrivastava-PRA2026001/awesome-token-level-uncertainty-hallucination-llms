# GitHub Implementations

Verified, actively relevant open-source implementations of token-level uncertainty and hallucination-detection methods.

---

### potsawee/selfcheckgpt
Official implementation of SelfCheckGPT (Manakul, Liusie & Gales, 2023), including all five consistency-checking variants (BERTScore, MQAG, n-gram, NLI, LLM-Prompt) plus demo notebooks and the accompanying WikiBio hallucination dataset loader.
**Why it's relevant:** the standard black-box baseline that most token-level and semantic UQ papers compare against.
🔗 [github.com/potsawee/selfcheckgpt](https://github.com/potsawee/selfcheckgpt)

### IINemo/lm-polygraph
Official LM-Polygraph toolkit implementing token-probability, entropy, semantic-entropy, and ensemble-based uncertainty estimators behind a single, unified interface, with a large-scale benchmark for reproducible comparison.
**Why it's relevant:** the most comprehensive open reference implementation of the token-level UQ methods surveyed in this repository.
🔗 [github.com/IINemo/lm-polygraph](https://github.com/IINemo/lm-polygraph)

### jlko/semantic_uncertainty
Actively maintained codebase reproducing the semantic entropy experiments from the *Nature* paper (Farquhar, Kossen, Kuhn & Gal, 2024), covering both short-phrase/sentence-length and paragraph-length generation.
**Why it's relevant:** the reference implementation of semantic entropy, the key refinement of naive token-level entropy discussed throughout the accompanying paper.
🔗 [github.com/jlko/semantic_uncertainty](https://github.com/jlko/semantic_uncertainty)

### lorenzkuhn/semantic_uncertainty
Original codebase for the ICLR 2023 semantic uncertainty paper (Kuhn, Gal & Farquhar, 2023). Now deprecated in favor of `jlko/semantic_uncertainty`, but useful for understanding the original pipeline (`compute_confidence_measure.py`, `get_semantic_similarities.py`).
**Why it's relevant:** historical/original implementation of the method that introduced semantic entropy.
🔗 [github.com/lorenzkuhn/semantic_uncertainty](https://github.com/lorenzkuhn/semantic_uncertainty)

### RUCAIBox/HaluEval
Data-generation and evaluation code for the HaluEval benchmark (Li et al., 2023), including the sampling-then-filtering pipeline used to generate hallucinated samples and scripts for scoring hallucination-recognition performance.
**Why it's relevant:** provides the benchmark infrastructure used to evaluate detectors — including uncertainty-based ones — built in this space.
🔗 [github.com/RUCAIBox/HaluEval](https://github.com/RUCAIBox/HaluEval)
