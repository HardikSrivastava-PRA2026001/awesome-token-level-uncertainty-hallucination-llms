# Datasets

Verified datasets relevant to token-level uncertainty and hallucination detection in large language models.

---

### WikiBio GPT-3 Hallucination Dataset
- **Source:** Manakul, Liusie & Gales (2023), released alongside SelfCheckGPT
- **Description:** Sentence-level human annotations marking hallucinated vs. factual content in GPT-3-generated Wikipedia-style biographies. Each sentence is labeled as major-inaccurate, minor-inaccurate, or accurate.
- **Application:** Standard benchmark for evaluating sentence- and token-level hallucination detectors, including uncertainty-based methods.
- **Link:** [huggingface.co/datasets/potsawee/wiki_bio_gpt3_hallucination](https://huggingface.co/datasets/potsawee/wiki_bio_gpt3_hallucination)

### HaluEval
- **Source:** Li, Cheng, Zhao, Nie & Wen (2023), RUCAIBox
- **Description:** 5,000 general user queries with ChatGPT responses plus 30,000 task-specific examples across question answering, knowledge-grounded dialogue, and text summarization, each paired with a hallucinated and a non-hallucinated response.
- **Application:** Evaluating whether LLMs — and downstream uncertainty-based detectors — can recognize hallucinated text; used as a standard benchmark in recent token-level detection papers (e.g., TokenHD).
- **Link:** [github.com/RUCAIBox/HaluEval](https://github.com/RUCAIBox/HaluEval)

### TruthfulQA
- **Source:** Lin, Hilton & Evans (2022)
- **Description:** 817 questions spanning 38 categories (health, law, finance, politics, etc.), specifically written to elicit false answers that imitate common human misconceptions.
- **Application:** Testing whether token-level confidence/uncertainty correlates with factual correctness, particularly for the "confident hallucination" failure mode where models are sharply wrong.
- **Link:** [github.com/sylinrl/TruthfulQA](https://github.com/sylinrl/TruthfulQA)

---

*Note: If additional datasets are added later (e.g., for cross-lingual or long-form evaluation), append them here following the same four-field format (Source, Description, Application, Link).*
