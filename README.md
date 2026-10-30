# Awesome LLM-generated Text Detection

<div align="center" style="border-radius:50%;">
  <img src="log.png" alt="Logo" width="200" class="avatar">
</div>

<p align="center">
  <img src="https://awesome.re/badge.svg" alt="Awesome">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License-MIT">
  <img src="https://img.shields.io/badge/PRs-Welcome-red" alt="PRs-Welcome">
  <img src="https://img.shields.io/github/last-commit/junchaoIU/LLM-generated-Text-Detection/main?logo=github&color=blue" alt="last-commit">
</p>

The powerful ability of large language models (LLMs) to understand, follow, and generate complex languages has enabled LLM-generated texts to flood many areas of our daily lives at an incredible rate, with potentially negative impacts and risks on society and academia. As LLMs continue to expand, *how can we detect LLM-generated texts to help minimize the threat posed by the misuse of LLMs?*

<div align="center">
  <img src="cover.png" alt="cover" width="750">
</div>
<br>
<!-- **Authors:** -->

**_¹ [Junchao Wu](https://github.com/junchaoIU), ¹ [Shu Yang](https://twitter.com/shuyhere), ¹ [Runzhe Zhan](https://runzhe.me/), ¹ ² [Yulin Yuan](https://fah.um.edu.mo/yulin-yuan/), ¹ [Derek Fai Wong](https://www.fst.um.edu.mo/personal/derek-wong/), ¹ [Lidia Sam Chao]()_**


<!-- **Affiliations:** -->

¹ University of Macau, ² Peking University

## 📢 News
* [2026.05] ✨ Our paper is accepted by ACL 2026. We released DetectRL-X, a comprehensive multilingual benchmark for LLM-generated text detection, covering 8 languages, 6 domains, 4 commercial LLMs, and 8 evaluation dimensions. Please refer to arXiv: *[DetectRL-X: Towards Reliable Multilingual and Real-World LLM-Generated Text Detection](https://arxiv.org/abs/2605.15518)* and Github Repo *[DetectRL-X](https://github.com/AIDC-AI/Marco-LLM/tree/main/DetectRL-X)* for details.
* [2025.12] ✨ Our paper is published in TACL. We released RepreGuard, an efficient statistics-based detection method that leverages hidden representation patterns of LLMs to distinguish between LLM-generated and human-written texts. Please refer to arXiv: *[RepreGuard: Detecting LLM-Generated Text by Revealing Hidden Representation Patterns](https://arxiv.org/abs/2508.13152)* and Github Repo *[RepreGuard](https://github.com/NLP2CT/RepreGuard)* for details.
* [2025.03] ✨ Our survey paper is accepted by *Computational Linguistics* (Volume 51, Issue 1). Please refer to *[A Survey on LLM-Generated Text Detection: Necessity, Methods, and Future Directions](https://aclanthology.org/2025.cl-1.8/)* for details.
* [2024.11.28] ✨ Our paper is accepted by COLING 2025. We released GECScore, a simple yet effective black-box zero-shot detection approach based on the observation that human-written texts typically contain more grammatical errors than LLM-generated texts. Please refer to arXiv: *[Who Wrote This? The Key to Zero-Shot LLM-Generated Text Detection Is GECScore](https://arxiv.org/abs/2405.04286)* and Github Repo *[GECScore](https://github.com/NLP2CT/GECScore)* for details.
* [2024.09.26] ✨ Our benchmark paper is accepted by NeurIPS 2024 D&B track. We released DetectRL, a benchmark for real-world LLM-generated text detection, provide real utility to researchers on the topic and practitioners looking for consistent evaluation methods. Please refer to arXiv: *[DetectRL: Benchmarking LLM-Generated Text Detection in Real-World Scenarios](https://arxiv.org/abs/2410.23746)* and Github Repo *[DetectRL](https://github.com/NLP2CT/DetectRL)* for details.
* [2023.10.24] Our survey paper is now available on arXiv: *[A Survey on LLM-generated Text Detection: Necessity, Methods, and Future Directions](https://arxiv.org/abs/2310.14724)*.
* [2023.05.01] : We began to explore the topic of LLM-generated Text Detection.

## 🔍 Table of Contents
- [Awesome LLM-generated Text Detection](#awesome-llm-generated-text-detection)
  - [📢 News](#-news)
  - [� Table of Contents](#-table-of-contents)
  - [📃 Papers](#-papers)
    - [Overview](#overview)
    - [Datasets](#datasets)
      - [Benchmarks](#benchmarks)
      - [Potential Datasets](#potential-datasets)
    - [Detector](#detector)
      - [Watermarking Technology](#watermarking-technology)
      - [Statistics-based Detectors](#statistics-based-detectors)
      - [Neural-based Detectors](#neural-based-detectors)
      - [Human-assisted Methods](#human-assisted-methods)
      - [Detector Attack](#detector-attack)
      - [Shared Task](#shared-task)
    - [Related Works](#related-works)
      - [Other Surveys](#other-surveys)
  - [🚩 Citation](#-citation)
  - [Contributing](#contributing)

## 📃 Papers
### Overview
A survey and reflection on the latest research breakthroughs in LLM-generated Text detection, including data, detectors, metrics, current issues and future directions. 
Please refer to our article/paper for more details.


### Datasets
#### Benchmarks

| Benchmarks / Datasets | Venue | Date | Use | Human | LLMs |
|---|---|---|---|---|---|
| [HC3](https://arxiv.org/abs/2301.07597) | arXiv | 2023-01 | train | 58k | 26k |
| [HC3-Chinese](https://arxiv.org/abs/2301.07597) | arXiv | 2023-01 | train | 22k | 17k |
| [CHEAT](https://arxiv.org/abs/2304.12008) | arXiv | 2023-04 | train | 15k | 35k |
| [GROVER Dataset](https://arxiv.org/abs/1905.12616) | NeurIPS 2019 | 2019-05 | train valid test | 5k 2k 8k | 5k 1k 4k |
| [TweepFake](https://arxiv.org/abs/2008.00036) | PLoS ONE | 2020-07 | train | 12k | 12k |
| [GPT-2 Output Dataset](https://github.com/openai/gpt-2-output-dataset) | GitHub | - | train | 250k | 250k |
| [TuringBench](https://aclanthology.org/2021.findings-emnlp.172/) | EMNLP 2021 Findings | 2021 | train | 10k | 190k |
| [MGTBench](https://arxiv.org/abs/2303.14822) | arXiv | 2023-03 | train test | 2k 563 | 13k 3k |
| [ArguGPT](https://arxiv.org/pdf/2304.07666.pdf) | arXiv | 2023-04 | train valid test | 3k 350 350 | 3k 350 350 |
| [DeepfakeText-Dataset](https://arxiv.org/abs/2305.13242) | ACL 2024 | 2023-05 | train valid test | 95k 29k 29k | 236k 29k 28k |
| [M4](https://arxiv.org/abs/2305.14902) | arXiv | 2023-05 | train valid test | 122k 500 500 | 122k 500 500 |
| [GPABenchmark](https://arxiv.org/abs/2306.05524) | arXiv | 2023-06 | train | 600k | 600k |
| [Scientific-articles Benchmark](https://aclanthology.org/2023.trustnlp-1.17/) | TrustNLP 2023 | 2023 | train test | 8k 4k | 8k 4k |
| [DetectRL](https://arxiv.org/abs/2410.23746) | NeurIPS 2024 D&B | 2024-10 | train test | 101k | 134k (4 LLMs, 4 domains, 4 attacks) |
| [DetectRL-X](https://arxiv.org/abs/2605.15518) | ACL 2026 | 2026-05 | test | 3.46M (8 langs, 6 domains, 4 LLMs, 8 attacks) | |
| [MULTITuDE](https://arxiv.org/abs/2310.13606) | EMNLP 2023 | 2023-10 | test | - | 56k (7 langs, 8 LLMs) |
| [RAID](https://arxiv.org/abs/2405.07940) | ACL 2024 | 2024-05 | test | - | 6M (11 models) |
| [M4GT-Bench](https://arxiv.org/abs/2402.11175) | ACL 2024 | 2024-02 | test | - | - (4 domains, multi-lingual) |
| [MultiSocial](https://arxiv.org/abs/2406.12549) | ACL 2025 | 2025-07 | test | 58k | 414k (22 langs, 5 platforms, 7 LLMs) |
| [Detecting the Machine](https://arxiv.org/abs/2603.17522) | arXiv | 2026-03 | test | 23k | 15k (HC3 + ELI5, multiple LLMs) |

#### Potential Datasets
| Tasks                              | Datasets                                                                    |
|------------------------------------|-----------------------------------------------------------------------------|
| Questions Answering                | PubMedQA, Children book corpus (CBT), ELI5, TruthfulQA, NarrativeQA         |
| Scientific writing                 | Peer Read, arXiv, TOEFL11                                                   | 
| Story generation                   | WritingPrompts                                                              | 
| News Article writing               | XSum                                                                        | 
| Web Text                           | Wiki40b, WebText, Avax tweets dataset, Climate Change Tweets Ids            | 
| Opinion statements                 | r/ChangeMyView (CMV) Reddit subcommunity, Yelp , IMDB Dataset               | 
| Comprehension and Reasoning        | SciGen, ROCStories Corpora, HellaSwag, SQuAD                                | 

### Detectors
<!-- <div align="left">
  <img src="image.png" alt="Detector" width="800">
</div> -->

#### Watermarking Technology

| Paper | Venue | Date | Link |
|---|---|---|---|
| A watermark for large language models. | ICML 2023 | 2023-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2301.10226) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/jwkirchenbauer/lm-watermarking) |
| On the Reliability of Watermarks for Large Language Models | ICLR 2024 | 2023-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2306.04634) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/jwkirchenbauer/lm-watermarking) |
| A Private Watermark for Large Language Models | ICLR 2024 | 2023-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2307.16230) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/THU-BPM/private_watermark) |
| Distillation-Resistant Watermarking for Model Protection in NLP | arXiv | 2022-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2210.03312) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/xuandongzhao/drw) |
| Watermarking Pre-trained Language Models with Backdooring | arXiv | 2022-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2210.07543) |
| CATER: Intellectual Property Protection on Text Generation APIs via Conditional Watermarks | NeurIPS 2022 | 2022-09 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2209.08773) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/xlhex/cater_neurips) |
| An Adaptive Watermark for Large Language Models | ICML 2024 | 2024-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2401.13927) |
| WaterBench: A Benchmark for LLM Watermarking | ACL 2024 | 2023-11 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2311.07138) |
| Watermarking Makes Language Models Radioactive | arXiv | 2024-02 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2402.14904) |
| SynthID-Text: Identifying AI-Generated Text Content | Nature 2024 | 2024-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://www.nature.com/articles/s41586-024-08025-4) |
#### Statistics-based Detectors

| Paper | Venue | Date | Link |
|---|---|---|---|
| DetectGPT: Zero-Shot Machine-Generated Text Detection using Probability Curvature | ICML 2023 | 2023-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2301.11305) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/eric-mitchell/detect-gpt) |
| Fast-DetectGPT: Efficient Zero-Shot Detection of Machine-Generated Text via Conditional Probability Curvature | ICLR 2024 | 2023-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2310.05130) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/baoguangsheng/fast-detect-gpt) |
| Efficient Detection of LLM-generated Texts with a Bayesian Surrogate Model | arXiv | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.16617) |
| DetectLLM: Leveraging Log Rank Information for Zero-Shot Detection of Machine-Generated Text | arXiv | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2306.05540) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/mbzuai-nlp/detectllm) |
| GLTR: Statistical Detection and Visualization of Generated Text | ACL 2019 Demo | 2019-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/1906.04043) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/HendrikStrobelt/detecting-fake-text) |
| HowkGPT: Investigating the Detection of ChatGPT-generated University Student Homework through Context-Aware Perplexity Analysis | arXiv | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.18226) |
| Intrinsic Dimension Estimation for Robust Detection of AI-Generated Texts | arXiv | 2023-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2306.04723) |
| Who Wrote This? The Key to Zero-Shot LLM-Generated Text Detection Is GECScore | COLING 2025 | 2024-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2405.04286) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/NLP2CT/GECScore) |
| RepreGuard: Detecting LLM-Generated Text by Revealing Hidden Representation Patterns | TACL 2025 | 2025-08 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2508.13152) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/NLP2CT/RepreGuard) |
| Is ChatGPT Involved in Texts? Measure the Polish Ratio to Detect ChatGPT-Generated Text | arXiv | 2023-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2307.11380) |
| DNA-GPT: Divergent N-Gram Analysis for Training-Free Detection of GPT-Generated Text | ICLR 2024 | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.17359) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/Xianjun-Yang/DNA-GPT) |
| Binoculars: Zero-Shot Detection of Machine-Generated Text | ICML 2024 | 2024-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2401.12070) |
| LLMDet: A Third Party Large Language Models Generated Text Detection Tool | EMNLP 2023 Findings | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.15004) |
| Ghostbuster: Detecting Text Ghostwritten by Large Language Models | arXiv | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.15047) |
| GPT-who: An Information Density-based Machine-Generated Text Detector | arXiv | 2023-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2310.06202) |
| BiScope: AI-generated Text Detection by Checking Memorization of Preceding Tokens | NeurIPS 2024 | 2024-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2406.05988) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/MarkGHX/BiScope) |
| Ten Words Only Still Help: Improving Black-Box AI-Generated Text Detection via Proxy-Guided Efficient Re-Sampling (POGER) | IJCAI 2024 | 2024-02 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2402.09199) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/ICTMCG/POGER) |
| AdaDetectGPT: Adaptive Detection of LLM-Generated Text with Statistical Guarantees | NeurIPS 2025 | 2025-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2510.01268) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/Mamba413/AdaDetectGPT) |
| Exons-Detect: Identifying and Amplifying Exonic Tokens via Hidden-State Discrepancy for Robust AI-Generated Text Detection | ACL 2026 | 2026-03 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2603.24981) |
| Segmenting Human–LLM Co-authored Text via Change Point Detection | arXiv | 2026-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2605.03723) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/Mamba413/DetectLLMSegmentation) |
| Triospect: A Three-Dimensional Framework for Robust Statistical AI-Generated Text Detection Against Diverse Attacks | TACL 2026 | 2026-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2606.31074) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/baoguangsheng/triospect) |
| Detecting LLM-Generated Tokens in Human–LLM Coauthored Text | arXiv | 2026-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2607.21458) |
| Detecting LLM-Generated Text with Performance Guarantees | arXiv | 2026-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2601.06586) |
#### Neural-based Detectors

| Paper | Venue | Date | Link |
|---|---|---|---|
| How Close is ChatGPT to Human Experts? Comparison Corpus, Evaluation, and Detection | arXiv | 2023-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2301.07597) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/hello-simpleai/chatgpt-comparison-detection) |
| Multiscale Positive-Unlabeled Detection of AI-Generated Texts | ICLR 2024 (Spotlight) | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.18149) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/yuchuantian/aigc_text_detector) |
| Real or fake? Learning to discriminate machine from human generated text | arXiv | 2019-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/1906.03351) |
| Automatic Detection of Generated Text is Easiest when Humans are Fooled | ACL 2020 | 2019-11 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/1911.00650) |
| Stylometric Detection of AI-Generated Text in Twitter Timelines | arXiv | 2023-03 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2303.03697) |
| TweepFake: about Detecting Deepfake Tweets | PLoS ONE | 2020-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2008.00036) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/tizfa/tweepfake_deepfake_text_detection) |
| Towards a Robust Detection of Language Model Generated Text: Is ChatGPT that Easy to Detect? | TALN 2023 | 2023-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2306.05871) |
| Deepfake Text Detection in the Wild | ACL 2024 | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.13242) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/yafuly/deepfaketextdetect) |
| ArguGPT: evaluating, understanding and identifying argumentative essays generated by GPT models | arXiv | 2023-04 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2304.07666) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/huhailinguist/ArguGPT) |
| Check Me If You Can: Detecting ChatGPT-Generated Academic Writing using CheckGPT | arXiv | 2023-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2306.05524) |
| GPT-Sentinel: Distinguishing Human and ChatGPT Generated Content | arXiv | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.07969) |
| Neural Deepfake Detection with Factual Structure of Text | EMNLP 2020 | 2020-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2010.07475) |
| ConDA: Contrastive Domain Adaptation for AI-generated Text Detection | IJCNLP-AACL 2023 | 2023-09 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2309.03992) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/AmritaBh/ConDA-gen-text-detection) |
| RADAR: Robust AI-Text Detection via Adversarial Learning | NeurIPS 2023 | 2023-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2307.03838) |
| OUTFOX: LLM-generated Essay Detection through In-context Learning with Adversarially Generated Examples | AAAI 2024 | 2023-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2307.11729) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/ryuryukke/OUTFOX) |
| Fighting fire with fire: Can chatgpt detect ai-generated text? | SIGKDD Explorations | 2023-08 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2308.01284) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/amritabh/chatgpt-as-detector) |
| GPT Paternity Test: GPT Generated Text Detection with GPT Genetic Inheritance | arXiv | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.12519) |
| Raidar: geneRative AI Detection viA Rewriting | ICLR 2024 | 2024-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2401.12970) |
| Beat LLMs at Their Own Game: Zero-Shot LLM-Generated Text Detection via Querying ChatGPT | EMNLP 2023 | 2023-12 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://aclanthology.org/2023.emnlp-main.463/) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/thunlp/LLM-generated-text-detection) |
| Defending Against Neural Fake News by Removing LLMs' Greatest Weakness | NeurIPS 2019 | 2019-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/1905.12616) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/rowanz/grover) |
| CoCo: Coherence-Enhanced Machine-Generated Text Detection | EMNLP 2023 | 2022-12 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2212.10341) |
| SeqXGPT: Sentence-Level AI-Generated Text Detection | EMNLP 2023 | 2023-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2310.08903) |
| J-Guard: Robust Guardrails against Unreliable Text Generation by LLMs | IJCNLP-AACL 2023 | 2023-09 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2309.03164) |
| DEMASQ: Unmasking the ChatGPT Wordsmith | NDSS 2024 | 2023-11 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2311.05019) |
| Smaller Language Models are Better Black-box Detectors | EACL 2024 | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.09859) |
| DeTeCtive: Detecting AI-generated Text via Multi-Level Contrastive Learning | NeurIPS 2024 | 2024-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2410.20964) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/heyongxin233/DeTeCtive) |
| A Ship of Theseus: Paraphrasing Capabilities for Detecting LLM-Generated Text | ACL 2024 | 2023-11 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2311.08374) |
| ReMoDetect: Reward Modified Detection of LLM-Generated Text | arXiv | 2024-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2405.17382) |
| Origin Tracing and Detecting of Large Language Models | arXiv | 2023-04 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2304.14072) |
| Text Fluoroscopy: Detecting LLM-Generated Text through Intrinsic Features | EMNLP 2024 | 2024-11 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://aclanthology.org/2024.emnlp-main.885/) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/Fish-and-Sheep/Text-Fluoroscopy) |
| Human Texts Are Outliers: Detecting LLM-generated Texts via Out-of-distribution Detection | NeurIPS 2025 | 2025-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2510.08602) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/cong-zeng/ood-llm-detect) |
| DAMAGE: Detecting Adversarially Modified AI Generated Text | arXiv | 2025-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2501.03437) |
| NOTAI.AI: Explainable Detection of Machine-Generated Text via Curvature and Feature Attribution | arXiv | 2026-03 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2603.05617) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/TenderChasm/Notai.ai) |
| Breaking the Generator Barrier: Disentangled Representation for Generalizable AI-Text Detection (DRGD) | arXiv | 2026-04 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2604.13692) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/PuXiao06/DRGD) |
| GigaCheck: Detecting LLM-generated Content via Object-Centric Span Localization | ACL 2026 Findings | 2026-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://aclanthology.org/2026.findings-acl.213/) |
| Linda Assay 1.3.2 and Linda Loupe: two local detectors of AI-generated text in English, Polish and Russian | Zenodo (technical report) | 2026-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://doi.org/10.5281/zenodo.23261670) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/Lendarixon/Linda) |
#### Human-assisted Methods

| Paper | Venue | Date | Link |
|---|---|---|---|
| RoFT: A Tool for Real vs Fake Text Detection | EMNLP 2020 Demo | 2020-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://aclanthology.org/2020.emnlp-demos.25/) |
| Human Heuristics for AI-Generated Language Are Flawed | arXiv | 2022-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2206.07271) |
| Real or Fake Text? Investigating the Abilities of Language Models to Detect AI-Generated Text | AAAI 2023 | 2022-12 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2212.12672) |
| Does Human Collaboration Enhance the Accuracy and Reliability of AI-Generated Text Detection? | HCOMP 2023 | 2023-04 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2304.01002) |
| People cannot distinguish GPT-4 from a human in a Turing test | arXiv | 2024-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2405.08007) |

#### Detector Attack

| Paper | Venue | Date | Link |
|---|---|---|---|
| Paraphrasing evades detectors of AI-generated text, but retrieval is an effective defense | NeurIPS 2023 | 2023-03 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2303.13408) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/martiansideofthemoon/ai-detection-paraphrases) |
| Can AI-Generated Text be Reliably Detected? | arXiv | 2023-03 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2303.11156) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/vinusankars/Reliability-of-AI-text-detectors) |
| Red Teaming Language Model Detectors with Language Models | TACL 2023 | 2023-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2305.19713) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/shizhouxing/LLM-Detector-Robustness) |
| Humanizing Machine-Generated Content: Evading AI-Text Detection through Adversarial Attack | LREC-COLING 2024 | 2024-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://aclanthology.org/2024.lrec-main.739/) |
| RAFT: Realistic Attacks to Fool Text Detectors | EMNLP 2024 | 2024-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2410.03658) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/JamesLWang/RAFT) |
| Adversarial Paraphrasing: A Universal Attack for Humanizing AI-Generated Text | NeurIPS 2025 | 2025-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2506.07001) |
| CoPA: Contrastive Paraphrase Attacks on LLM-Generated Text Detectors | EMNLP 2025 | 2025-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2505.15337) |
| Attacks on Machine-Text Detectors Retain Stylistic Fingerprints | arXiv | 2025-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2505.14608) |
| Revealing Weaknesses in Text Watermarking Through Self-Information Rewrite Attacks (SIRA) | ICML 2025 | 2025-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2505.05190) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/YixinCheng/SIRA) |
| DE-MARK: Watermark Removal in Large Language Models | ICML 2025 | 2024-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2410.13808) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/RayRuiboChen/De-mark) |
| MASH: Evading Black-Box AI-Generated Text Detectors via Style Humanization | ACL 2026 Findings | 2026-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2601.08564) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/githigher/MASH) |
| Vaporizer: Breaking Watermarking Schemes for Large Language Model Outputs | arXiv | 2026-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2605.07481) |
| AI Watermark Evidence Fails Forensic Readiness: An Empirical Evaluation | arXiv | 2026-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2607.16010) |

#### Shared Task

| Paper | Venue | Date | Link |
|---|---|---|---|
| Findings of the RuATD Shared Task 2022 on Artificial Text Detection in Russian | Dialogue 2022 | 2022-06 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2206.01583) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/dialogue-evaluation/RuATD) |
| SemEval-2024 Task 8: Multigenerator, Multidomain, and Multilingual Black-Box Machine-Generated Text Detection | SemEval 2024 | 2024-04 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2404.14183) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/mbzuai-nlp/SemEval2024-task8) |
| GenAI Content Detection Task 1: English and Multilingual Machine-Generated Text Detection | COLING 2025 | 2025-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2501.11012) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/mbzuai-nlp/COLING-2025-Workshop-on-MGT-Detection-Task1) |
| Overview of the NLPCC 2025 Shared Task 1: LLM-Generated Text Detection | NLPCC 2025 | 2025-08 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://doi.org/10.1007/978-981-95-3352-7_21) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/NLP2CT/NLPCC-2025-Task1) |
| Findings of the Counter Turing Test (CT2): AI-Generated Text Detection | DeFactify 2025 | 2026-05 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2605.20761) |
| The Second Shared Task on LLM-Generated Text Detection (NLPCC 2026 Task 6) | NLPCC 2026 | 2026-11 | [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/NLP2CT/NLPCC-2026-Task6-Detection) |

### Related Works
#### Other Surveys
| Paper | Venue | Date | Link |
|---|---|---|---|
| Automatic Detection of Machine Generated Text: A Critical Survey | COLING 2020 | 2020-11 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2011.01314) |
| The Science of Detecting LLM-Generated Texts | arXiv | 2023-02 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2303.07205) |
| Machine Generated Text: A Comprehensive Survey of Threat Models and Detection Methods | ACM Trustworthy AI | 2022-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2210.07321) |
| Computer-Generated Text Detection Using Machine Learning: A Systematic Review | Springer | - | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://link.springer.com/chapter/10.1007/978-3-319-41754-7_43) |
| Attribution and Obfuscation of Neural Text Authorship: A Data Mining Perspective | ACM SIGKDD Explorations | 2022-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2210.10488) |
| Deepfake Text Detection: Limitations and Opportunities | S&P 2023 | 2022-10 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2210.09421) |
| A Survey of AI-generated Text Forensic Systems | arXiv | 2024-03 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2403.01152) |
| SoK: Watermarking for AI-Generated Content | arXiv | 2024-11 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2411.18479) |
| The Imitation Game Revisited: A Comprehensive Survey on Recent Advances in AI-generated Text Detection | ESWA 2025 | 2025-01 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://doi.org/10.1016/j.eswa.2025.126694) [![Static Badge](https://img.shields.io/badge/code-black?logo=github)](https://github.com/Nicozwy/AIGTD-Survey) |
| Watermarking for AI Content Detection: A Review | ICLR 2025 Workshop | 2025-04 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2504.03765) |
| A Survey on LLM Watermarking: Theory and Deployment | arXiv | 2026-07 | [![Static Badge](https://img.shields.io/badge/paper-%23B31B1B?logo=arxiv&labelColor=grey)](https://arxiv.org/abs/2607.10103) |


## 🚩 Citation

If our research helps you, please kindly cite our paper.

```bibtex
@article{wu2025survey,
      title={A Survey on LLM-Generated Text Detection: Necessity, Methods, and Future Directions}, 
      author={Junchao Wu and Shu Yang and Runzhe Zhan and Yulin Yuan and Lidia Sam Chao and Derek Fai Wong},
      journal      = {Computational Linguistics},
      volume       = {51},
      number       = {1},
      year         = {2025},
      pages        = {275--338},
      url          = {https://aclanthology.org/2025.cl-1.8/},
}

@inproceedings{wu2025GECScore,
      title={Who Wrote This? The Key to Zero-Shot LLM-Generated Text Detection Is GECScore}, 
      author={Junchao Wu and Runzhe Zhan and Derek F. Wong and Shu Yang and Xuebo Liu and Lidia S. Chao and Min Zhang},
      booktitle    = {Proceedings of the 31st International Conference on Computational Linguistics},
      year         = {2025},
      pages        = {10275--10292},
      url          = {https://aclanthology.org/2025.coling-main.684/},
}

@article{chen2025RepreGuard,
      title={RepreGuard: Detecting LLM-Generated Text by Revealing Hidden Representation Patterns}, 
      author={Xin Chen and Junchao Wu and Shu Yang and Runzhe Zhan and Zeyu Wu and Ziyang Luo and Di Wang and Min Yang and Lidia S. Chao and Derek F. Wong},
      journal      = {Transactions of the Association for Computational Linguistics},
      volume       = {13},
      year         = {2025},
      pages        = {1812--1831},
      url          = {https://aclanthology.org/2025.tacl-1.81/},
}

@inproceedings{wu2026DetectRLX,
      title={DetectRL-X: Towards Reliable Multilingual and Real-World LLM-Generated Text Detection}, 
      author={Junchao Wu and Yefeng Liu and Chenyu Zhu and Hao Zhang and Zeyu Wu and Tianqi Shi and Yichao Du and Longyue Wang and Weihua Luo and Jinsong Su and Derek F. Wong},
      booktitle    = {Proceedings of the 64th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)},
      year         = {2026},
      pages        = {38247--38294},
      url          = {https://aclanthology.org/2026.acl-long.1773/},
}

@inproceedings{wu2024DetectRL,
      title={DetectRL: Benchmarking LLM-Generated Text Detection in Real-World Scenarios}, 
      author={Junchao Wu and Runzhe Zhan and Derek F. Wong and Shu Yang and Xinyi Yang and Yulin Yuan and Lidia S. Chao},
      booktitle    = {Advances in Neural Information Processing Systems 37 (NeurIPS 2024) Datasets and Benchmarks Track},
      year         = {2024},
      url          = {https://proceedings.neurips.cc/paper_files/paper/2024/hash/b61bdf7e9f64c04ec75a26e781e2ad51-Abstract-Datasets_and_Benchmarks_Track.html},
}
```


## Contributing
Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request. We appreciate your contributions to making LLM-generated Text Detection work even better.




