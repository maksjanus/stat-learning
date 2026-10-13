# stat-learning

My notes and lab work while working through **An Introduction to Statistical Learning with Applications in Python** (ISLP) by James, Witten, Hastie, Tibshirani & Taylor.

The book is free online at [statlearning.com](https://www.statlearning.com/).

## Progress

| Ch. | Topic | Notes | Lab | Exercises |
|----|-------|:-----:|:---:|:---------:|
| 2 | Statistical Learning | ⬜ | ⬜ | ⬜ |
| 3 | Linear Regression | ⬜ | ⬜ | ⬜ |
| 4 | Classification | ⬜ | ⬜ | ⬜ |
| 5 | Resampling Methods | ⬜ | ⬜ | ⬜ |
| 6 | Linear Model Selection & Regularization | ⬜ | ⬜ | ⬜ |
| 7 | Moving Beyond Linearity | ⬜ | ⬜ | ⬜ |
| 8 | Tree-Based Methods | ⬜ | ⬜ | ⬜ |
| 9 | Support Vector Machines | ⬜ | ⬜ | ⬜ |
| 10 | Deep Learning | ⬜ | ⬜ | ⬜ |
| 11 | Survival Analysis & Censored Data | ⬜ | ⬜ | ⬜ |
| 12 | Unsupervised Learning | ⬜ | ⬜ | ⬜ |
| 13 | Multiple Testing | ⬜ | ⬜ | ⬜ |

⬜ not started · 🟨 in progress · ✅ done

## Repo layout

```
stat-learning/
├── notes/        # chapter notes (markdown)
├── labs/         # the book's labs, worked through in notebooks
└── exercises/    # my answers to end-of-chapter exercises
```

## Running the notebooks

```bash
git clone https://github.com/maksjanus/stat-learning.git
cd stat-learning
python -m venv .venv
# Windows: .venv\Scripts\activate    macOS/Linux: source .venv/bin/activate
pip install ISLP jupyter
jupyter notebook
```

The `ISLP` package includes the datasets used in the book, so no separate downloads are needed.

## Notes

These are my own learning notes, so expect mistakes along the way. Corrections and suggestions are welcome through issues.
