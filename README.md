#  When Labels Lie: Investigating LLMs under a Bias-Sensitive Framework for Bangla Hate Speech

This project accompanies the research titled **“When Labels Lie: Investigating LLMs under a Bias-Sensitive Framework for Low-Resource Language – Bangla”**. It aims to critically analyze how large language models (LLMs) reflect and amplify annotator bias in hate speech datasets within low-resource settings.

---

##  Project Description

This repository contains:

- Our **paper** outlining the bias evaluation framework  
- Jupyter notebooks for inference and evaluation  
- Model-wise **performance results** on different levels of label complexity  
- Sample dataset used for hate speech classification in Bangla
- Explored reasoning for each output label to examine the proper understanding of LLM.
- Visualizations & metrics for **positive/negative bias** and **mismatch analysis**

We examine LLM behavior under different label granularities (binary, ternary, quaternary, etc.) and measure their alignment, agreement, and bias using metrics like **F1 Score**, **Cohen’s Kappa**, and **Mismatch Rate**. For reasoning we have used metrics like **BERT-Score** and **Cohen's Kappa**.

---

## 📁 Repository Structure

```
.
├── 📄 README.md
├── 📄 When_Labels_Lie.pdf                          # Full research paper (It hasn't completed yet)
├── 📄 Annotator_Bias_Results.pdf                  # Complete performance evaluation results
├── 📁 data/
│   └── sample_dataset.csv                         # Sample of annotated hate speech data in Bangla
├── 📁 notebooks/
│   ├── inference_with_gemini.ipynb                # Inference using Gemini models
│   ├── inference_with_llama.ipynb                 # Inference using LLaMA models
│   └── evaluation_script_hate_speech.ipynb        # Bias evaluation script
```

---

##  Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/annotator-bias-bangla.git
cd annotator-bias-bangla
```

### 2. Install Dependencies
You can run the notebooks in a [Kaggle kernel](https://www.kaggle.com/code) or install the dependencies locally:
```bash
pip install -r requirements.txt
```

>  Most of the work was developed and tested on **Kaggle**, so the notebooks are fully runnable there without additional setup.

### 3. Run Inference
Use the provided Jupyter notebooks to run inference on various LLMs:
- `notebooks/inference_with_gemini.ipynb`
- `notebooks/inference_with_llama.ipynb`

These scripts take Bangla hate speech text and generate predictions using different LLMs.

### 4. Run Evaluation
Use:
```python
notebooks/evaluation_script_hate_speech.ipynb
```
to compute:
- **F1 Score**
- **Cohen's Kappa**
- **Mismatch Rates**
- **Bias-specific evaluations** (e.g., gender, religion, profession)

---

## Key Contributions

-  **Bias-Sensitive Framework** to assess model alignment under biased and unbiased labeling settings  
-  Extensive **multi-model comparison**: Gemini, GPT, DeepSeek, Mistral, LLaMA, Qwen  
-  Evaluation across **multiple label granularities** (2, 3, 4, 5, 6 labels)  
-  Detection of **annotator bias and mismatch patterns**
-  Investigate a proper understanding of LLM with reasoning during multi-label classification.  

---

## Reproducibility

All results can be reproduced by following these steps:

1. Load any model notebook from `notebooks/`  
2. Replace dataset path with `data/sample_dataset.csv`  
3. Run all cells to generate predictions  
4. Run `evaluation_script_hate_speech.ipynb` to evaluate performance metrics  

---

## License

This work is released under the [MIT License](LICENSE).

---

## Citation

If you use this work in your research, please cite:

```bibtex

```

---

## 🙌 Acknowledgements

Thanks to the researchers and contributors who supported the creation of the Bangla hate speech dataset and to the open-source LLM community for model access and integration support.
