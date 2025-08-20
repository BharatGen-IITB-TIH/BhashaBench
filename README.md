# BhashaBench

[![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview

BhashaBench is a series of India-specific, multi-task benchmarks designed to evaluate Large Language Models (LLMs) across multiple Indic languages, diverse domains, and varied task types. Built from the ground up with authentic Indian contexts, it goes beyond factual knowledge to capture cultural nuances, domain-specific expertise, and rural values. The suite includes datasets spanning agriculture, governance, education, and more offering a mix of question answering, classification, reasoning, translation, and other tasks to ensure robust, multilingual, and context-aware performance assessment.

This repository contains code for evaluating language models on the BBK benchmark using the [lm-eval-harness](https://github.com/EleutherAI/lm-evaluation-harness) framework.

## Domain Specific Benchmark

1) **BhashaBench-Krishi (BBK)**: It is the first large-scale, authentic benchmark designed to rigorously evaluate AI models on Indian agricultural knowledge. Tailored for India’s diverse agro-ecological zones, crops, languages, and farming practices, BBK draws from 55+ official government agricultural exams to assess models' ability to provide precise, region-aware, policy-relevant, and actionable agricultural advice. [![Hugging Face](https://img.shields.io/badge/🤗%20Hugging%20Face-Datasets-yellow)](https://huggingface.co/datasets/bharatgenai/BhashaBench) 



    ### Key Features

    - **Languages**: English and Hindi (with plans for more Indic languages)
    - **Exams**: 55+ unique agricultural government and institutional exams across India
    - **Domains**: 25+ agricultural and allied science domains, spanning over 270 topics
    - **Questions**: 15,405 rigorously validated, exam-based questions
    - **Difficulty Levels**: Easy (6,754), Medium (6,941), Hard (1,710)
    - **Question Types**: Multiple Choice, Assertion-Reasoning, Match the Column, Rearrange the Sequence, Fill in the Blanks
    - **Focus**: Practical, context-rich, region-specific agricultural knowledge essential for Indian farmers


    ### Dataset Structure
    ### Test Set
    The test set consists of the BBK benchmark, which contains approximately 15,000 multiple-choice questions across 2 Indic languages.

    ### Dataset Statistics

    | Metric                   | Count                     |
    | ------------------------ | ------------------------- |
    | Total Questions          | 15,405                    |
    | English Questions        | 12,648                    |
    | Hindi Questions          | 2,757                     |
    | Subject Domains          | 25+                       |
    | Government Exams Covered | 55+                       |


    ### Subjects spanning BBK
    | Subject Domain                     | Count |
    |----------------------------------|-------|
    | Agri-Environmental & Allied Disciplines | 176   |
    | Agricultural Biotechnology       | 524   |
    | Agricultural Chemistry & Biochemistry | 281   |
    | Agricultural Economics & Policy  | 627   |
    | Agricultural Engineering & Technology | 244   |
    | Agricultural Extension Education | 774   |
    | Agricultural Microbiology        | 111   |
    | Agriculture Communication        | 254   |
    | Agriculture Information Technology | 190   |
    | Agronomy                        | 5078  |
    | Animal Sciences                 | 148   |
    | Crop Sciences                  | 549   |
    | Dairy & Poultry Science          | 89    |
    | Entomology                    | 696   |
    | Fisheries and Aquaculture       | 34    |
    | General Knowledge & Reasoning   | 661   |
    | Genetics and Plant Breeding      | 389   |
    | Horticulture                   | 2070  |
    | Natural Resource Management      | 193   |
    | Nematology                   | 184   |
    | Plant Pathology                | 397   |
    | Plant Sciences & Physiology     | 129   |
    | Seed Science and Technology     | 202   |
    | Soil Science                   | 1357  |
    | Veterinary Sciences           | 48    |


2) **BhashaBench-Finance (BBF)**: It is the first comprehensive benchmark designed to evaluate AI models on Indian financial knowledge and practices. Tailored for India's diverse financial ecosystem, regulatory framework, and economic landscape, BBF draws from 25+ official government and institutional financial exams to assess models' ability to provide accurate, policy-compliant, and contextually relevant financial advice and analysis. [![Hugging Face](https://img.shields.io/badge/🤗%20Hugging%20Face-Datasets-yellow)](https://huggingface.co/datasets/bharatgenai/BhashaBench-Finance) 

    ### Key Features
    - **Languages**: English and Hindi (with plans for more Indic languages)
    - **Exams**: 25+ unique financial government and institutional exams across India
    - **Domains**: 30+ financial and allied domains, spanning comprehensive financial knowledge
    - **Questions**: 19,433 rigorously validated, exam-based questions
    - **Difficulty Levels**: Easy (7,111), Medium (9,348), Hard (2,974)
    - **Question Types**: Multiple Choice, Assertion-Reasoning, Match the Column, Rearrange the Sequence, Fill in the Blanks, Reading Comprehension, Essay
    - **Focus**: Practical, regulation-aware, India-specific financial knowledge essential for financial professionals and consumers

    ### Dataset Structure
    ### Test Set
    The test set consists of the BBF benchmark, which contains approximately 19,000 questions across 2 Indic languages.

    ### Dataset Statistics
    | Metric                   | Count                     |
    | ------------------------ | ------------------------- |
    | Total Questions          | 19,433                    |
    | English Questions        | 13,451                    |
    | Hindi Questions          | 5,982                     |
    | Subject Domains          | 30+                       |
    | Government Exams Covered | 25+                       |

    ### Subjects spanning BBF
    | Subject Domain                                | Count |
    |---------------------------------------------|-------|
    | Problem Solving                             | 5,686 |
    | Mathematics for Finance                     | 4,845 |
    | Banking Services                           | 1,171 |
    | Governance & Policy                        | 1,064 |
    | Language & Communication                   | 946   |
    | Corporate Finance & Investment             | 910   |
    | Commerce                                   | 863   |
    | Accounting                                 | 773   |
    | General Knowledge                          | 539   |
    | Information Technology Finance             | 490   |
    | Economics & Development Studies            | 274   |
    | Rural Economics                            | 261   |
    | Environmental Finance                      | 168   |
    | Taxation & Regulatory Compliance           | 155   |
    | Interdisciplinary Finance                  | 153   |
    | Data & Analytics in Finance                | 127   |
    | History, Sociology & Cultural Studies of Finance | 127 |
    | Finance Education                          | 118   |
    | Healthcare Economics                       | 114   |
    | Science and Technology in Finance          | 101   |
    | International Finance & Trade              | 83    |
    | Business Management                        | 83    |
    | Energy, Infrastructure & Finance           | 82    |
    | Behavioral Finance                         | 67    |
    | Financial Markets                          | 47    |
    | Sports, Media & Finance Linkages           | 45    |
    | Marketing Finance                          | 42    |
    | Insurance & Risk Management                | 42    |
    | Legal Finance                              | 34    |
    | Financial Technology                       | 23    |

   
## Usage

##### Prerequisites

- Python 3.7+
- `lm-eval-harness` library
- HuggingFace Transformers
- vLLM (optional, for faster inference)

1. Clone this repository:

```bash
git clone --depth 1 https://github.com/BharatGen-IITB-TIH/BhashaBench.git
cd BhashaBench
pip install -e .
```

2. Request access to the HuggingFace 🤗 dataset [here](https://huggingface.co/datasets/bharatgenai/BhashaBench).

3. Set up your environment variables:

```bash
export HF_HOME=/path/to/HF_CACHE/if/needed
export HF_TOKEN=YOUR_HUGGINGFACE_TOKEN
```

The following languages are supported for BBK and BBF:
- English
- Hindi

### HuggingFace Evaluation

For HuggingFace models, you may use the following sample command:

```bash
lm_eval --model hf \
    --model_args 'pretrained=google/gemma-2-27b-it,temperature=0.0,top_p=1.0,parallelize=True' \
    --tasks bbk,bbf \
    --batch_size auto:40 \  
    --log_samples \
    --output_path $EVAL_OUTPUT_PATH \
    --max_batch_size 64 \
    --apply_chat_template
```

### vLLM Evaluation

For vLLM-compatible models, you may use the following sample command:

```bash
lm_eval --model vllm \
    --model_args 'pretrained=meta-llama/Llama-3.2-3B,tensor_parallel_size=$N_GPUS' \
    --gen_kwargs 'temperature=0.0,top_p=1.0' \
    --tasks bbk,bbf \
    --batch_size auto \
    --log_samples \
    --output_path $EVAL_OUTPUT_PATH
```

### Single Language Evaluation

To evaluate your Model on a specific language, modify the `--tasks` parameter:

```bash
--tasks bbk_English
--tasks bbf_Hindi
```

Replace `English` with the available language (e.g., Hindi, etc.).

### Evaluation Tips & Observations

1. Make sure to use `--apply_chat_template` for Instruction-fine-tuned models, to format the prompt correctly.
2. vLLM generally works better with Llama models, while Gemma models work better with HuggingFace.
3. If vLLM encounters out-of-memory errors, try reducing `max_gpu_utilization` else switch to HuggingFace.
4. For HuggingFace, use `--batch_size=auto:<n_batch_resize_tries>` to re-select the batch size multiple times.
5. When using vLLM, pass generation kwargs in the `--gen_kwargs` flag. For HuggingFace, include them in `model_args`.



## License

This dataset is released under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).


## Links

- [GitHub Repository 💻](https://github.com/BharatGen-IITB-TIH/BhashaBench)
- [Paper 📄](#)
- [Hugging Face Dataset 🤗](https://huggingface.co/datasets/bharatgenai/BhashaBench-Krishi)

