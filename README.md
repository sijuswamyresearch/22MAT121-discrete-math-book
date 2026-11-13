# 22MAT121: Discrete Mathematics — Quarto Book

Digital course material for **22MAT121: Discrete Mathematics** (B.Tech Artificial Intelligence & Engineering, BTC-AIE, Amrita Vishwa Vidyapeetham).

## Project Structure

```text
22MAT121-discrete-math-book/
├── _quarto.yml                      # Quarto Book master configuration
├── index.qmd                        # Course overview, objectives, COs & CO-PO matrix
├── unit1-logic-counting.qmd         # Unit 1: Logic, Mathematical Reasoning & Counting (20 problems)
├── unit2-relations-recurrences.qmd  # Unit 2: Relations, Recurrences & Advanced Counting (20 problems)
├── unit3-number-theory.qmd          # Unit 3: Number Theory & Cryptography (15 problems)
├── styles.css                       # Custom academic styles & mobile MathJax rules
├── requirements.txt                 # Python dependencies (SymPy, NumPy, Jupyter)
├── docs/.nojekyll                   # Prevents Jekyll from ignoring underscore directories
└── .github/workflows/publish.yml    # Automated GitHub Actions deployment workflow
```

## Quick Start (Local Preview & Build)

1. Install Python packages:
   ```bash
   pip install -r requirements.txt
   ```
2. Live-preview the book in your browser:
   ```bash
   quarto preview
   ```
3. Render the static website (into `docs/`) and PDF book:
   ```bash
   quarto render
   ```

## Publishing to GitHub Pages

### Option A: Publish from `docs/` folder on `main` branch (Simplest)
1. Run `quarto render` locally (which outputs the rendered site into `docs/` and caches Python execution inside `_freeze/`).
2. Commit and push all files (including `docs/` and `_freeze/`) to the `main` branch on GitHub.
3. In your GitHub repository, navigate to **Settings -> Pages -> Build and deployment**, select **Deploy from a branch**, and choose **`main`** with folder **`/docs`**.

### Option B: One-command CLI publish (`gh-pages` branch)
Run directly from your terminal:
```bash
quarto publish gh-pages
```
