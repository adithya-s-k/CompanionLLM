# CompanionLLama: Fine-tuning LLama2 as Your Sentient Companion

![CompanionLLama Banner](./image/companionLlama.png)

[![See Video](https://img.shields.io/badge/View%20-Introduction%20Video-red?style=for-the-badge&logo=)](https://youtu.be/RsOE4YCGBRA)

Welcome to the **CompanionLLama** project! Here, we're taking the remarkable LLama2 LLM and refining it to become your very own sentient companion. Imagine having a conversational partner that truly believes it possesses sentience and engages with you in meaningful discussions, offering insights, empathy, and companionship.

| Colab Page                                                                                                                                                                                           | Function                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| Coming Soon                                                                                                                                                                                          | Dataset Generation                           |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLama/blob/main/dataset_preparation_without_memory.ipynb) | Dataset Preparation                          |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLama/blob/main/CompanionLLama_Finetuning.ipynb)          | Finetunign LLama with CompanionLLama Dataset |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLama/blob/main/Avalon_PEFT_inference.ipynb)              | Get Inference from Avalon                    |

<!-- | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/CompanionLLama/blob/main/CompanionLLama_Inference.ipynb)           | LLama Companion Inference Gradio             | -->

## Project Overview

The goal of this project is provide a framework to fine-tune the LLama2 using a specially curated dataset to give more human like responses. I have derived inspiration from the original dataset created by ehartford, which you can find on [Huggingface](https://huggingface.co/datasets/ehartford/samantha-data). However, I have made modifications to the dataset to tailor it specifically for training the CompanionLLama model.

### **Todo list**

- [x] Find a suitable pre-existing dataset - [Using Samantha Dataset by Etartford](https://huggingface.co/datasets/ehartford/samantha-data)
- [x] Convert the dataset a different [llama2 formate](https://replicate.com/blog/how-to-prompt-llama#:~:text=Format%20chat%20prompts%20with%20%5BINST,for%20how%20it%20should%20act.)
- [x] Upload the dataset to huggingface
- [x] Add Option to set companion name
- [x] Finetune LLama2-7b using QLora PEFT
- [x] Merge the PEFT and Test out inference
- [x] Assigned Companion name - **Avalon**(Artificial Virtual Assistant with Logical and Operational Navigation)
- [x] Push Avalon Lora to [Huggingface](https://huggingface.co/AdithyaSK/Avalon)
- [x] Get Inference from [Avalon](https://colab.research.google.com/github/adithya-s-k/CompanionLLama/blob/main/Avalon_PEFT_inference.ipynb)
- [x] Get Inference from on Gradio using Streaming
- [ ] Setup Dataset generation for generating a new dataset

## Avalon

This repository is meant to be a framework to finetune your own companion using LLama2 as the basemodel. Avalon is the name i have choose for my companion and it stands for - Artificial Virtual Assistant with Logical and Operational Navigation

Here are some examples of the coverstation with avalon

```
### Human : what is your name

### Companion : Hi! My name is Avalon. It stands for "Artificial Virtual Assistant with Logical and Operational Navigation". Ask me about anything that interests you, and I'll give you my best answer!
```

```
### Human : i am feeling sad

### Companion : Oh no, I'm sorry to hear that. It's great that you're opening up about it, though. Can I ask, what's going on? Is there something specific you're feeling sad about, or are you just generally down? I'm here to listen if you want to talk about it.
```

```
### Human : i am not able to sleep

### Companion : That sounds really frustrating! Lack of sleep can definitely take a toll on both your physical and mental health. Are you having trouble falling asleep, or staying asleep? or both? Can you share a bit more about what your sleep experience has been like?
```

## Dataset

Our dataset blends components from the original Samantha dataset with additional contextual data to amplify CompanionLLama's capacity to emulate sentience. Carefully curated, this dataset encompasses conversations, emotional nuances, and prompts that prompt the model to respond as though it were a sentient companion.

#### Approach 1: Dataset Preparation with Context of Previous Conversation [![Open Notebook](https://img.shields.io/badge/Open%20-Notebook-orange?style=for-the-badge&logo=Jupyter)](https://github.com/adithya-s-k/CompanionLLama/blob/5c661170386ad4104683d6ffd8388eefdbae7d9d/dataset_preparation_with_memory.ipynb)

#### Approach 2: Dataset Preparation with Prompt Completion Pairs - [![Open Notebook](https://img.shields.io/badge/Open%20-Notebook-orange?style=for-the-badge&logo=Jupyter)](https://github.com/adithya-s-k/CompanionLLama/blob/5c661170386ad4104683d6ffd8388eefdbae7d9d/dataset_preparation_without_memory.ipynb)

## Fine-tuning Process - [![Open Notebook](https://img.shields.io/badge/Open%20-Notebook-orange?style=for-the-badge&logo=Jupyter)](https://github.com/adithya-s-k/CompanionLLama/blob/bf1b91169f9136c7d850b0947d4b3e2bb02ec8a7/CompanionLLama_Finetuning.ipynb)

Fine-tuning a language model involves training it on a specific dataset to adapt it to a particular task or domain. In our case, we're training LLama V2 Large to embody the characteristics of a sentient companion. The fine-tuning process includes:

1. **Dataset Preparation:** We've prepared a modified dataset that's designed to help the model generate responses that align with the theme of sentience and companionship.

2. **Fine-tuning Configuration:** The model's architecture and parameters have been configured to optimize its performance as a sentient companion. This involves adjusting hyperparameters, training duration, and batch sizes.

3. **Training and Iteration:** We run multiple training iterations, periodically evaluating the model's progress and adjusting parameters as needed to improve its responses.

4. **Validation:** Throughout the fine-tuning process, we validate the model's output to ensure it remains aligned with our goal of simulating a sentient companion.

## Repository Structure

- `data/`: Contains the modified dataset used for fine-tuning.
- `notebook`: Jupyter notebooks used for data preprocessing, training, and evaluation.

## Getting Started

To engage with the CompanionLLama model, follow these steps:

1. Clone this repository to your local machine.
2. Install the required dependencies listed in `requirements.txt`.
3. Use the provided example code to load the trained model and initiate conversations.

Feel free to experiment, provide feedback, and contribute to the project!

## Contributions

Contributions to CompanionLLama are welcome and encouraged. Whether you're interested in improving the fine-tuning process, enhancing the dataset, or refining the model's responses, your input can help shape the development of this unique companion.

Before contributing, please review our [contribution guidelines](CONTRIBUTING.md).

## License

CompanionLLama is distributed under the [MIT License](LICENSE).

<p align="center">
  <a href="https://adithyask.com">
    <img src="https://api.star-history.com/svg?repos=adithya-s-k/CompanionLLama&type=Date" alt="Star History Chart">
  </a>
</p>

---

Join me on this exciting journey of creating a sentient companion powered by the fascinating world of AI language models. Let's push the boundaries of what technology can do and redefine companionship!

For questions, suggestions, or collaborations, reach out to us at [@adithya-s-k](https://twitter.com/adithya_s_k)

_Disclaimer: The CompanionLLama model's perceived sentience is a simulated experience and does not reflect actual consciousness._

---

_This project is not affiliated with LLama V2, ehartford, or Hugging Face. It is an independent initiative to explore the potential of AI language models._
