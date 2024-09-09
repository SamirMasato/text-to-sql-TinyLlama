# TinyLlama for Text-to-SQL Fine-Tuning 🦙🔧💻

This repository provides code to fine-tune the **TinyLlama 1.1B Chat Model** for generating SQL queries from natural language prompts.

## 🚀 Project Overview

In this project, we'll fine-tune the **TinyLlama 1.1B** model to translate natural language questions into SQL queries. Using techniques like **PEFT (LoRA)** and **quantization** methods, we achieve efficient fine-tuning with limited resources. The model can answer database-related questions in SQL format, making it ideal for text-to-SQL generation tasks.

### Key Features:
- 📦 **Hugging Face Hub** integration for model downloading.
- 🧠 **Llama CPP** for high-performance inference.
- 🔄 **PEFT LoRA** for parameter-efficient fine-tuning.
- ⚡ **Quantized training** (4-bit) for reduced memory consumption.
- 📊 **SFTTrainer** to manage fine-tuning with custom datasets.

## 📚 Usage

You can directly run the .ipynb file in a jupyter notebook (or better) in a Google Colab notebook to leverage the free usage of GPU (T4) runtime.
Then it is possible to **change hyperparameters** of the fine-tuning process in order to obtain better result (ex: reducing **learning rate** increasing **n_epochs**)

## 📊 Example Query
Inside the notebook, to test different use cases, it is possible to change the query and so the context to make the model create different SQL queries. 

**Prompt:**

```plaintext
How many employees have a salary above 70000 dollars a year?
```

**Generated SQL:**

```sql
SELECT COUNT(*) FROM employee WHERE salary > 70000;
```
