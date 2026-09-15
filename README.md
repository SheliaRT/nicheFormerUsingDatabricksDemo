# nicheFormerUsingDatabricksDemo
# Nicheformer on Databricks

Runs [Nicheformer](https://huggingface.co/theislab/Nicheformer), a transformer
foundation model for single-cell and spatial transcriptomics, on Databricks to
generate cell embeddings for a public spatial transcriptomics dataset.

## What it does

1. Loads a subsampled [Xenium Human Lung](https://www.10xgenomics.com/datasets/xenium-human-lung-preview-data-1-standard) dataset (~3,000 cells).
2. Loads Nicheformer's pretrained weights from Hugging Face (`aletlvl/Nicheformer`).
3. Tokenizes the cells and extracts 512-dimensional embeddings.
4. Visualizes the embeddings with UMAP.

Runs on CPU-only compute — no GPU required for inference.

## Usage

Open `nicheformer_xenium_lung_demo.py` in Databricks (Workspace → Import), update
the file paths near the top of the notebook to match your own uploaded data, and
run the cells top to bottom.

## Credit

- Model: [Nicheformer: a foundation model for single-cell and spatial omics](https://www.biorxiv.org/content/10.1101/2024.04.15.589472) (Schaar et al.)
- Code: [github.com/theislab/nicheformer](https://github.com/theislab/nicheformer) (BSD-3-Clause) / [huggingface.co/theislab/Nicheformer](https://huggingface.co/theislab/Nicheformer)
- Data: [Xenium Human Lung Preview Data](https://www.10xgenomics.com/datasets/xenium-human-lung-preview-data-1-standard), 10x Genomics (CC BY 4.0)
