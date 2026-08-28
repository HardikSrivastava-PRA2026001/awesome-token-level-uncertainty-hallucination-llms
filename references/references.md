# References

A curated, human-verified list of scholarly papers on token-level uncertainty and hallucination detection in large language models. Every entry was checked against a publisher page, DOI/Crossref record, arXiv listing, or ACL Anthology entry before inclusion (see [Citation Integrity Audit](../citation-audit/Citation_Integrity_Audit.pdf)).

## Contents

- [Survey and Review Papers](#survey-and-review-papers)
- [Foundational Papers](#foundational-papers)
- [Methods and Algorithms](#methods-and-algorithms)
- [Recent Research (2024–2026)](#recent-research-20242026)
- [Evaluation Methods and Benchmarks](#evaluation-methods-and-benchmarks)

---

## Survey and Review Papers

- **Survey of Hallucination in Natural Language Generation**
  Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii, Ye Jin Bang, Andrea Madotto, Pascale Fung — 2023, *ACM Computing Surveys*, 55(12), 1–38
  [DOI: 10.1145/3571730](https://doi.org/10.1145/3571730) · [arXiv:2202.03629](https://arxiv.org/abs/2202.03629)
  Foundational taxonomy of hallucination types (intrinsic/extrinsic) and detection/mitigation approaches; establishes the vocabulary used across this field.

- **Siren's Song in the AI Ocean: A Survey on Hallucination in Large Language Models**
  Yue Zhang, Yafu Li, Leyang Cui, Deng Cai, Lemao Liu, Tingchen Fu, Xinting Huang, Enbo Zhao, Yu Zhang, Yulong Chen, et al. — 2023, arXiv preprint
  [arXiv:2309.01219](https://arxiv.org/abs/2309.01219)
  LLM-specific survey distinguishing factuality and faithfulness hallucination, with a dedicated taxonomy of uncertainty-based detection methods.

## Foundational Papers

- **Uncertainty Estimation in Autoregressive Structured Prediction**
  Andrey Malinin, Mark Gales — 2021, *International Conference on Learning Representations (ICLR 2021)*
  [arXiv:2002.07650](https://arxiv.org/abs/2002.07650)
  Formalizes token-level and sequence-level predictive uncertainty for autoregressive generation, underpinning most later token-level UQ metrics.

- **On Calibration of Modern Neural Networks**
  Chuan Guo, Geoff Pleiss, Yu Sun, Kilian Q. Weinberger — 2017, *Proceedings of the 34th International Conference on Machine Learning (ICML 2017)*, PMLR 70, 1321–1330
  [arXiv:1706.04599](https://arxiv.org/abs/1706.04599)
  Establishes the calibration framework (expected calibration error) that later work applies to diagnose confident hallucination in LLMs.

- **Simple and Scalable Predictive Uncertainty Estimation Using Deep Ensembles**
  Balaji Lakshminarayanan, Alexander Pritzel, Charles Blundell — 2017, *Advances in Neural Information Processing Systems (NeurIPS 2017)*, Vol. 30
  [Paper (NeurIPS Proceedings)](https://papers.nips.cc/paper_files/paper/2017)
  Classic deep-ensemble uncertainty estimation method that motivated later adaptations of predictive uncertainty to language generation.

- **Language Models (Mostly) Know What They Know**
  Saurav Kadavath, Tom Conerly, Amanda Askell, Tom Henighan, Dawn Drain, Ethan Perez, Nicholas Schiefer, Zac Hatfield-Dodds, Nova DasSarma, Eli Tran-Johnson, et al. — 2022, arXiv preprint
  [arXiv:2207.05221](https://arxiv.org/abs/2207.05221)
  Empirical evidence that LLM output probabilities carry meaningful self-knowledge about answer correctness, motivating uncertainty-based detection.

- **Semantic Uncertainty: Linguistic Invariances for Uncertainty Estimation in Natural Language Generation**
  Lorenz Kuhn, Yarin Gal, Sebastian Farquhar — 2023, *International Conference on Learning Representations (ICLR 2023)*
  [arXiv:2302.09664](https://arxiv.org/abs/2302.09664)
  Introduces semantic entropy, disentangling uncertainty over meaning from uncertainty over wording — a pivotal refinement of naive token-level entropy.

- **Calibrated Language Models Must Hallucinate**
  Adam Tauman Kalai, Santosh S. Vempala — 2023, arXiv preprint
  [arXiv:2311.14648](https://arxiv.org/abs/2311.14648)
  Theoretical result showing calibrated LLMs are statistically compelled to hallucinate on training-data "singleton" facts, bounding what uncertainty thresholds can achieve.

## Methods and Algorithms

- **Detecting Hallucinations in Large Language Models Using Semantic Entropy**
  Sebastian Farquhar, Jannik Kossen, Lorenz Kuhn, Yarin Gal — 2024, *Nature*, 630(8017), 625–630
  [DOI: 10.1038/s41586-024-07421-0](https://doi.org/10.1038/s41586-024-07421-0)
  Scales semantic entropy to a general-purpose hallucination ("confabulation") detector, validated across model families and domains.

- **SelfCheckGPT: Zero-Resource Black-Box Hallucination Detection for Generative Large Language Models**
  Potsawee Manakul, Adian Liusie, Mark J. F. Gales — 2023, *Proceedings of EMNLP 2023*, 9004–9017
  [DOI: 10.18653/v1/2023.emnlp-main.557](https://doi.org/10.18653/v1/2023.emnlp-main.557) · [arXiv:2303.08896](https://arxiv.org/abs/2303.08896)
  Sampling-based consistency detector used throughout the literature as a black-box baseline against token-level UQ methods.

- **Fact-Checking the Output of Large Language Models via Token-Level Uncertainty Quantification**
  Ekaterina Fadeeva, Aleksandr Rubashevskii, Artem Shelmanov, Sergey Petrakov, Haonan Li, Hamdy Mubarak, Evgenii Tsymbalov, Gleb Kuzmin, Alexander Panchenko, Timothy Baldwin, Preslav Nakov, Maxim Panov — 2024, *Findings of ACL 2024*, 9367–9385
  [DOI: 10.18653/v1/2024.findings-acl.558](https://doi.org/10.18653/v1/2024.findings-acl.558) · [arXiv:2403.04696](https://arxiv.org/abs/2403.04696)
  Introduces Claim Conditioned Probability (CCP), a token-level uncertainty measure that removes claim-irrelevant lexical variance.

- **Enhancing Uncertainty-Based Hallucination Detection with Stronger Focus**
  Tianhang Zhang, Lin Qiu, Qipeng Guo, Cheng Deng, Yue Zhang, Zheng Zhang, Chenghu Zhou, Xinbing Wang, Luoyi Fu — 2023, *Proceedings of EMNLP 2023*
  [arXiv:2311.13230](https://arxiv.org/abs/2311.13230)
  Reweights token-level uncertainty by keyword informativeness, historical reliability, and token properties (POS, frequency).

- **Generating with Confidence: Uncertainty Quantification for Black-Box Large Language Models**
  Zhen Lin, Shubhendu Trivedi, Jimeng Sun — 2023, arXiv preprint (later *Transactions on Machine Learning Research*, 2024)
  [arXiv:2305.19187](https://arxiv.org/abs/2305.19187)
  Extends confidence/uncertainty estimation to settings without direct access to token probabilities.

- **Detecting Hallucinations in Large Language Model Generation: A Token Probability Approach**
  Ernesto Quevedo, Jorge Yero, Rachel Koerner, Pablo Rivas, Tomas Cerny — 2024, arXiv preprint
  [arXiv:2405.19648](https://arxiv.org/abs/2405.19648)
  Applies token-probability-based features directly to hallucination classification in generated text.

- **INSIDE: LLMs' Internal States Retain the Power of Hallucination Detection**
  Chao Chen, Kai Liu, Ze Chen, Yi Gu, Yue Wu, Mingyuan Tao, Zhihang Fu, Jieping Ye — 2024, *International Conference on Learning Representations (ICLR 2024)*
  [arXiv:2402.03744](https://arxiv.org/abs/2402.03744)
  Proposes EigenScore, using the eigenvalues of a response covariance matrix over internal states to capture semantic consistency beyond token-level probability.

## Recent Research (2024–2026)

- **Efficient Hallucination Detection for LLMs Using Uncertainty-Aware Attention Heads**
  Artem Vazhentsev, Lyudmila Rvanova, Gleb Kuzmin, Ekaterina Fadeeva, Ivan Lazichny, Alexander Panchenko, Maxim Panov, Mrinmaya Sachan, Preslav Nakov, Timothy Baldwin, Artem Shelmanov — 2026, *Proceedings of the 43rd International Conference on Machine Learning (ICML 2026)*, PMLR 306
  [arXiv:2505.20045](https://arxiv.org/abs/2505.20045)
  Introduces RAUQ, identifying "uncertainty-aware" attention heads and fusing their signal with token confidence in a single forward pass.

- **Learning Uncertainty from Sequential Internal Dispersion in Large Language Models**
  Ponhvoan Srey, Xiaobao Wu, Cong-Duy Nguyen, Anh Tuan Luu — 2026, arXiv preprint
  [arXiv:2604.15741](https://arxiv.org/abs/2604.15741)
  Proposes SIVR, aggregating token-wise, layer-wise hidden-state variance across the full generated sequence.

- **Scalable Token-Level Hallucination Detection in Large Language Models**
  Rui Min, Tianyu Pang, Chao Du, Minhao Cheng, Yi R. Fung — 2026, arXiv preprint
  [arXiv:2605.12384](https://arxiv.org/abs/2605.12384)
  Introduces TokenHD, a supervised token-level detector trained on synthetically labeled hallucination data, scalable from 0.6B to 8B parameters.

- **DynHD: Hallucination Detection for Diffusion Large Language Models via Denoising Dynamics Deviation Learning**
  Yanyu Qian, Yue Tan, Yixin Liu, Wang Yu, Shirui Pan — 2026, arXiv preprint
  [arXiv:2603.16459](https://arxiv.org/abs/2603.16459)
  Extends token-level uncertainty to non-autoregressive diffusion LLMs by modeling uncertainty evolution across the denoising trajectory.

- **Semantic Entropy Probes: Robust and Cheap Hallucination Detection in LLMs**
  Jannik Kossen, Jiatong Han, Muhammed Razzak, Lisa Schut, Shreshth Malik, Yarin Gal — 2024, arXiv preprint
  [arXiv:2406.15927](https://arxiv.org/abs/2406.15927)
  Shows semantic entropy can be approximated by a lightweight linear probe on a single hidden state, avoiding costly multi-sample computation.

## Evaluation Methods and Benchmarks

- **HaluEval: A Large-Scale Hallucination Evaluation Benchmark for Large Language Models**
  Junyi Li, Xiaoxue Cheng, Wayne Xin Zhao, Jian-Yun Nie, Ji-Rong Wen — 2023, *Proceedings of EMNLP 2023*, 6449–6464
  [arXiv:2305.11747](https://arxiv.org/abs/2305.11747)
  Large-scale benchmark of human- and ChatGPT-generated hallucinated samples across QA, dialogue, and summarization; widely used to validate uncertainty-based detectors.

- **TruthfulQA: Measuring How Models Mimic Human Falsehoods**
  Stephanie Lin, Jacob Hilton, Owain Evans — 2022, *Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (ACL 2022)*, Volume 1, 3214–3252
  [ACL Anthology: 2022.acl-long.229](https://aclanthology.org/2022.acl-long.229/)
  Benchmark of questions designed to elicit imitative falsehoods, commonly used to evaluate whether uncertainty correlates with factual correctness.
