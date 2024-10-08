# FLAN-T5 Dialog Summarization Fine-Tuning with PEFT

This project involves fine-tuning the FLAN-T5 (1B) model to generate less toxic summaries for dialog data using Parameter-Efficient Fine-Tuning (PEFT) methods such as LoRA and QLoRA. A hate speech reward model from Meta AI is used to guide the model toward reducing toxicity in its outputs.

## Project Overview

- **Objective**: Fine-tune FLAN-T5 on the DialogSum dataset to produce dialog summaries with reduced toxicity.
- **Dataset**: DialogSum from Hugging Face – 10,000+ dialogues aimed at dialog summarization tasks.
- **Model**: Pretrained FLAN-T5 (1B parameters) using PEFT methods:
  - **Full Fine-Tuning**
  - **LoRA** (Low-Rank Adaptation) with Rank=32
  - **QLoRA** with Float16 precision

## Results

After fine-tuning, the model achieved the following absolute percentage improvements:
- **Instruct Model over Original Model**:
  - ROUGE-1: +18.82%
  - ROUGE-2: +10.43%
  - ROUGE-L: +13.70%
  - ROUGE-Lsum: +13.69%
- **PEFT Model over Instruct Model**:
  - ROUGE-1: -1.35%
  - ROUGE-2: -1.70%
  - ROUGE-L: -1.34%
  - ROUGE-Lsum: -1.35%


