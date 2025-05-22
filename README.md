# Qwen 2.5 0.5B PEFT Finetuning for long reasoning  

![Results graph](results_graph.png)

Finetuning (both full finetuning and PEFT (LoRA) finetuning) a small model (Qwen2.5-0.5B-Instruct) with GSM8K for long reasoning capabilities. 

Original notebook (only full-finetuning code) by Will Brown ([X profile](https://x.com/willccbb)). 
PEFT finetuning code and (model) evaluation code by me.

(I could not find the release post of the original notebook)

# Experiments
We had performed full finetuning (as a baseline) and PEFT finetuning using LoRA adapters of Rank 8, 16 and 32 

- Full finetuning :white_check_mark:
- Rank 8 LoRA adapter :white_check_mark: 
- Rank 16 LoRA adapter :white_check_mark: 
- Rank 32 LoRA adapter :white_check_mark: 

# Results

## Performance Gains
- **Baseline Qwen2.5-0.5B-Instruct**: 33.21% (unofficial score)
- **LoRA Rank 8**: 40.41% (+7.2% absolute improvement)
- **LoRA Rank 16**: 42.61% (+9.4% absolute improvement)
- **LoRA Rank 32**: 45.79% (+12.58% absolute improvement)
- **Full Fine-tuning**: 46.17% (+12.96% absolute improvement)

## Key Findings
- All LoRA configurations substantially outperform the baseline model
- Our Rank 32 LoRA adapter achieves 99% of the performance gain of full fine-tuning while updating only a portion of the parameters
