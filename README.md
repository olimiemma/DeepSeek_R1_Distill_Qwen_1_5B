# DeepSeek R1 Distill Qwen 1.5B Model Experiments

This repository contains experiments and examples using the DeepSeek R1 Distill Qwen 1.5B model, a lightweight but capable language model. The notebook demonstrates various capabilities and limitations of the model through different types of prompts and tasks.

## Model Overview

- **Model**: DeepSeek R1 Distill Qwen 1.5B
- **Training**: Group Relative Policy Optimization (GRPO) with Reinforcement Learning
- **Size**: 1.5B parameters
- **Format**: No quantization

## Key Features

### Strengths
- Excellent performance on mathematical reasoning tasks (e.g., GSM8K)
- Strong capability with LaTeX output formatting
- Efficient step-by-step thinking process visible through thinking tags
- Good at formal reasoning and structured problem-solving

### Limitations
- Default 512 token context window (can be expanded but may affect performance)
- Limited performance on creative writing tasks
- Not optimized for agent-based interactions or tool use
- Struggles with structured output and persona adoption

## Examples Included

1. **Mathematical Reasoning**
   - Prime number detection
   - Mathematical word problems
   - Equation solving

2. **Analytical Writing**
   - Complex analogies
   - Step-by-step problem solving
   - Structured analysis

3. **Response Generation**
   - Email composition
   - Weather descriptions
   - General knowledge Q&A

4. **Edge Cases**
   - Creative writing attempts
   - Agent-based interactions
   - Persona adoption scenarios

## Setup Instructions

```python
# Install required packages
!pip -q install accelerate
!pip -q install git+https://github.com/huggingface/transformers
!pip install -q sentencepiece tokenizer

# Import and load model
from transformers import AutoTokenizer, AutoModelForCausalLM
import torch

model = AutoModelForCausalLM.from_pretrained(
    "deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B",
    device_map="cuda",
    torch_dtype="auto",
)

tokenizer = AutoTokenizer.from_pretrained("deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B")
```

## Usage Notes

- The model performs best with explicit reasoning tasks
- Consider increasing token limit for complex reasoning problems
- May need additional prompting for structured outputs
- Works well with mathematical and analytical problems

## Requirements

- Python 3.x
- PyTorch
- Transformers library
- CUDA-capable GPU (recommended)
- 4GB+ GPU memory

## License

This notebook is provided as-is for educational and research purposes. The DeepSeek model has its own license terms that should be consulted for production use.

## Acknowledgments

Model developed by DeepSeek AI. Experiments and documentation compiled based on hands-on testing and model capabilities assessment.



![Distillation DeepSeekR12](https://github.com/user-attachments/assets/888ff802-2db1-4736-9c3e-aed58f633c86)
![Distillation DeepSeekR1](https://github.com/user-attachments/assets/e2f5de6e-6e28-4749-b0d8-f52e9bcb0483)
![Full models DeepSeekR1 ](https://github.com/user-attachments/assets/1b1eba0c-114f-48ee-8117-85079d309af6)
![Distilled model DeepSeekR1 ](https://github.com/user-attachments/assets/0745ede2-4d3e-45d4-9485-e55e14d96582)
