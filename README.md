# 🧠 Tiny Shakespeare GPT

This project implements a **mini GPT language model** trained on the *Tiny Shakespeare* dataset, following Andrej Karpathy’s YouTube tutorial **“Let’s Build GPT: From Scratch, in Code, Spelled Out.”**
The goal is to understand the inner workings of transformers by building a simplified GPT architecture **from the ground up** using PyTorch.

---

## Project Overview

This notebook walks through:

* Loading and preparing the Tiny Shakespeare dataset
* Building a transformer-based GPT model completely from scratch
* Implementing:

  * Self-attention
  * Multi-head attention
  * Feedforward networks
  * Positional encoding
  * Training loop and evaluation
* Generating text using the trained model

---

## Hyperparameters

The default hyperparameters are optimized for **CPU training**, which is slower and requires smaller models.

**CPU-Friendly Settings (Default):**

* `batch_size = 4`
* `block_size = 8`
* Suitable for quick experimentation or learning

If you're using a **GPU**, you can scale up the model size for better performance and lower loss.

**Recommended GPU Settings:**

* `batch_size = 64`
* `block_size = 256`
* `max_iters = 5000`
* `eval_interval = 500`
* `learning_rate = 3e-4`
* `eval_iters = 200`
* `n_embd = 384`
* `n_head = 6`
* `n_layer = 6`
* `dropout = 0.2`

---

## Dataset

The model trains on the **Tiny Shakespeare** dataset (≈1 MB), a collection of Shakespeare’s works in plain text.
The dataset is tokenized at the **character level** to keep the model simple and lightweight.

---

## Training

Run the notebook end-to-end.
Training on CPU will take significantly longer; GPU is recommended for larger hyperparameter settings.

Once trained, the model can generate text like:

```
ROMEO:
What light through yonder window breaks?
It is the east, and Juliet is the sun.
```

(Your output will vary.)

---

## Acknowledgements

This project is inspired by Andrej Karpathy’s tutorial on building GPT models from scratch.

---

## License

This project is open-source and free to use for learning and experimentation.

---

