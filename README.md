# FineTuningLlama
FineTuning Llama to create a versatile chatbot on Colab

- Deploy Llama2 Model based on an OpenAssistant Dataset
- Fine-tune model to construct a versatile chatbot using LangChain

## Requirements 

- Create an environment and import libraries
```python
!pip install -q accelerate==0.21.0 peft==0.4.0 bitsandbytes==0.40.2 transformers==4.31.0 trl==0.4.7
```

```python
import os
import torch
from datasets import load_dataset
from transformers import (AutoModelForCausalLM, AutoTokenizer, BitsAndBytesConfig, HfArgumentParser, TrainingArguments, pipeline, logging)

from peft import LoraConfig, PeftModel
from trl import SFTTrainer
import platform
```

## Model Stored in Hugging face hub

<img src="https://github.com/simran-padam/FineTuningLlama/blob/main/images/huggingface-model.png" width="400" height="400" />

#![image](https://github.com/simran-padam/FineTuningLlama/blob/main/images/huggingface-model.png)



