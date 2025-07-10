# 🐱🐶 CNN Cats-vs-Dogs Demo (CPU-only, macOS-safe)

A tiny, self-contained Jupyter notebook that:

1. Organises a mini Kaggle cats & dogs set.  
2. Trains a lightweight CNN **on CPU only** (no Metal GPU).  
3. Shows a convergence plot and saves the model (`.keras`).

Total runtime ≈ 1 min on an M2 MacBook (8 GB).

---

## Folder layout

```
cnn-demo/
├── Untitled.ipynb              # run this notebook live
├── cnn_cats_dogs_cpu.keras     # saved model (~11 MB, optional)
├── data/                       # auto-created (cats/ dogs/ images)
└── kaggle/                     # raw downloaded images (not committed)
```

---

## Quick start

```bash
git clone https://github.com/<your-user>/cnn-demo.git
cd cnn-demo

conda create -n cnn_cpu_env python=3.10 -y
conda activate cnn_cpu_env
python -m pip install tensorflow-macos==2.16.2 notebook matplotlib

jupyter notebook          # Kernel ▸ Restart & Run All
```

## Notebook cells

| Cell | Purpose |
|------|---------|
| 1    | Verify CPU-only TensorFlow devices. |
| 2    | Copy .jpgs into `data/images/cats/` and `data/images/dogs/`. |
| 3    | Build 80/20 train-val datasets (128×128, batch 8). |
| 4    | CNN + data-augmentation (flip/rot/zoom). |
| 5    | Train with EarlyStopping (patience 3). |
| 6    | Plot loss curves; save cnn_cats_dogs_cpu.keras. |

## Demo replay

```bash
conda activate cnn_cpu_env
cd cnn-demo
jupyter notebook   # Kernel ▸ Restart & Run All
```
