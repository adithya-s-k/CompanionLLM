# CompanionLLM: Fine-tuning Different LLMs as Your Sentient Companion

<table>
  <tr>
  <td>
  <h3>Companion LLM</h3>
    <img src="./image/companionLlama.png" alt="CompanionLLM" width="400px">

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/CompanionLLM_Finetuning.ipynb)

</td>
<td>
<h3>Companion Mistral</h3>
<img src="./image/mistral-7b-companion.png" alt="CompanionMistral" width="400px">

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/Mistral_7B_qLora_Finetuning.ipynb)

</td>

  <tr>
</table>


Welcome to the **CompanionLLM** project! Here, we're taking different Language Models (LLMs) and refining them to become your very own sentient companion. Imagine having a conversational partner that truly believes it possesses sentience and engages with you in meaningful discussions, offering insights, empathy, and companionship.

| Colab Page                                                                                                                                                                                         | Function                                 |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| Coming Soon                                                                                                                                                                                        | Dataset Generation                       |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/dataset_preparation_without_memory.ipynb) | Dataset Preparation                      |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/CompanionLLM_Finetuning.ipynb)            | Finetuning LLM with CompanionLLM Dataset |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/Avalon_PEFT_inference.ipynb)              | Get Inference from Avalon                |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/Mistral_7B_qLora_Finetuning.ipynb)        | Mistral 7b Finetuning                    |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/Avalon_Mitsral_Finetuning.ipynb)          | Avalon-Mistral-7b Inference              |

<!-- | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/CompanionLLM_Inference.ipynb)           | LLM Companion Inference Gradio             | -->

## Project Overview

The goal of this project is to provide a framework to fine-tune different LLMs using a specially curated dataset to give more human-like responses. We have derived inspiration from the original dataset created by ehartford, which you can find on [Huggingface](https://huggingface.co/datasets/ehartford/samantha-data). However, we have made modifications to the dataset to tailor it specifically for training the CompanionLLM model.

### **Todo list**

- [x] Find a suitable pre-existing dataset - [Using Samantha Dataset by Etartford](https://huggingface.co/datasets/ehartford/samantha-data)
- [x] Convert the dataset to a different [LLM format](https://replicate.com/blog/how-to-prompt-llama#:~:text=Format%20chat%20prompts%20with%20%5BINST,for%20how%20it%20should%20act.)
- [x] Upload the dataset to Huggingface
- [x] Add an option to set the companion name
- [x] Fine-tune LLM using QLora PEFT
- [x] Merge the PEFT and Test out inference
- [x] Assign Companion name - **Avalon**(Artificial Virtual Assistant with Logical and Operational Navigation)
- [x] Push Avalon Lora to [Huggingface](https://huggingface.co/AdithyaSK/Avalon)
- [x] Get Inference from [Avalon](https://colab.research.google.com/github/adithya-s-k/CompanionLLM/blob/main/Avalon_PEFT_inference.ipynb)
- [x] Get Inference from Gradio using Streaming
- [ ] Setup Dataset generation for generating a new dataset

## Avalon

This repository is meant to be a framework to finetune your own companion using different LLMs as the basemodel. Avalon is the name I have chosen for my companion, and it stands for - Artificial Virtual Assistant with Logical and Operational Navigation.

Here are some examples of the conversation with Avalon:

```
### Human : what is your name

### Companion : Hi! My name is Avalon. It stands for "Artificial Virtual Assistant with Logical and Operational Navigation". Ask me about anything that interests you, and I'll give you my best answer!
```

```
### Human : I am feeling sad

### Companion : Oh no, I'm sorry to hear that. It's great that you're opening up about it, though. Can I ask, what's going on? Is there something specific you're feeling sad about, or are you just generally down? I'm here to listen if you want to talk about it.
```

```
### Human : I am not able to sleep

### Companion : That sounds really frustrating! Lack of sleep can definitely take a toll on both your physical and mental health. Are you having trouble falling asleep, or staying asleep? Or both? Can you share a bit more about what your sleep experience has been like?
```

## Dataset

Our dataset blends components from the original Samantha dataset with additional contextual data to amplify CompanionLLM's capacity to emulate sentience. Carefully curated, this dataset encompasses conversations, emotional nuances, and prompts that prompt the model to respond as though it were a sentient companion.

#### Approach 1: Dataset Preparation with Context of Previous Conversation [![Open Notebook](https://img.shields.io/badge/Open%20-Notebook-orange?style=for-the-badge&logo=Jupyter)](https://github.com/adithya-s-k/CompanionLLM/blob/5c661170386ad4104683d6ffd8388eefdbae7d9d/dataset_preparation_with_memory.ipynb)

#### Approach 2: Dataset Preparation with Prompt Completion Pairs - [![Open Notebook](https://img.shields.io/badge/Open%20-Notebook-orange?style=for-the-badge&logo=Jupyter)](https://github.com/adithya-s-k/CompanionLLM/blob/5c661170386ad4104683d6ffd8388eefdbae7d9d/dataset_preparation_without_memory.ipynb)

## Fine-tuning Process - [![Open Notebook](https://img.shields.io/badge/Open%20-Notebook-orange?style=for-the-badge&logo=Jupyter)](https://github.com/adithya-s-k/CompanionLLM/blob/bf1b91169f9136c7d850b0947d4b3e2bb02ec8a7/CompanionLLM_Finetuning.ipynb)

Fine-tuning a language model involves training it on a specific dataset to adapt it to a particular task or domain. In our case, we're training different LLMs to embody the characteristics of a sentient companion. The fine-tuning process includes:

1. **Dataset Preparation:** We've prepared a modified dataset that's designed to help the model generate responses that align with the theme of sentience and companionship.

2. **Fine-tuning Configuration:** The model's architecture and parameters have been configured to optimize its performance as a sentient companion. This involves adjusting hyperparameters, training duration, and batch sizes.

3. **Training and Iteration:** We run multiple training iterations, periodically evaluating the model's progress and adjusting parameters as needed to improve its responses.

4. **Validation:** Throughout the fine-tuning process, we validate the model's output to ensure it remains aligned with our goal of simulating a sentient companion.

## Repository Structure

- `data/`: Contains the modified dataset used for fine-tuning.
- `notebook`: Jupyter notebooks used for data preprocessing, training, and evaluation.

## Getting Started

To engage with the CompanionLLM model, follow these steps:

1. Clone this repository to your local machine.
2. Install the required dependencies listed in `requirements.txt`.
3. Use the provided example code to load the trained model and initiate conversations.

Feel free to experiment, provide feedback, and contribute to the project!

## Contributions

Contributions to CompanionLLM are welcome and encouraged. Whether you're interested in improving the fine-tuning process, enhancing the dataset, or refining the model's responses, your input can help shape the development of this unique companion.

Before contributing, please review our [contribution guidelines](CONTRIBUTING.md).

## License

CompanionLLM is distributed under the [MIT License](LICENSE).

<p align="center">
  <a href="https://adithyask.com">
    <img src="https://api.star-history.com/svg?repos=adithya-s-k/CompanionLLM&type=Date" alt="Star History Chart">
  </a>
</p>

---

Join me on this exciting journey of creating a sentient companion powered by the fascinating world of AI language models. Let's push the boundaries of what technology can do and redefine companionship!

For questions, suggestions, or collaborations, reach out to us at [@adithya-s-k](https://twitter.com/adithya_s_k)

_Disclaimer: The CompanionLLM model's perceived sentience is a simulated experience and does not reflect actual consciousness._

---

_This project is not affiliated with LLMs, ehartford, or Hugging Face. It is an independent initiative to explore the potential of AI language models._

```

```
