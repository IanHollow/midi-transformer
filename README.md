# MIDI Transformer

This project explores training a transformer language model to generate MIDI files. It uses the [miditok](https://github.com/NaturalSpeech/miditok) library for tokenizing MIDI data and Hugging Face Transformers for the model implementation.

## Project Goals

- Experiment with applying GPT‑2 style models to symbolic music generation.
- Provide a minimal example using **miditok** to encode MIDI files with the REMI+ format.
- Train a small model that can generate new sequences from a classical music dataset.

## Repository Structure

```
miditok-model.ipynb   # Jupyter notebook with the full training pipeline
requirements.txt      # Python dependencies
```

The notebook walks through downloading the dataset, tokenizing the MIDI files, creating training/validation/test splits, and training a `GPT2LMHeadModel`. At the end it shows how to generate a new MIDI piece from a seed sequence.

## Requirements

Python 3.11+ is recommended. Install dependencies with:

```bash
pip install -r requirements.txt
```

The notebook relies on the [Kaggle](https://www.kaggle.com/) `classical-music-midi` dataset. You will need Kaggle API credentials in a `kaggle.json` file to download it via the `kagglehub` library.

## Using the Notebook

1. Install the requirements.
2. Launch Jupyter and open `miditok-model.ipynb`.
3. Run all cells to download the dataset, train the tokenizer and model, and generate a MIDI file.

Generated MIDI sequences are saved to the working directory.

## Next Steps

This repository is a starting point for experiments. Possible improvements include:

- Converting the notebook code to reusable Python modules or scripts.
- Adding model checkpoints and example generated audio clips.
- Expanding the dataset or experimenting with different tokenization schemes.

Contributions and suggestions are welcome!
