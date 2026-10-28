# PyTorch Basics: Tensors

A hands-on notebook where I work through the fundamentals of PyTorch tensors, the data structure that everything else in deep learning is built on. Every concept is run and checked in code, with my own notes alongside.

**Notebook:** `pytroch_basics_.ipynb`

## What I covered

| Topic | What I practiced |
|---|---|
| Creating tensors | `torch.empty`, `rand`, `randint`, `zeros`, `ones`, and converting a NumPy array with `torch.tensor()` |
| Data types | Checking and setting `dtype`, and why `torch.rand(..., dtype=int)` raises an error |
| In-place operations | `add_()` (modifies the tensor itself) vs `torch.add()` (returns a new tensor) |
| Reshaping | `size()`, `reshape()`, `transpose()` |
| Broadcasting | Rules for element-wise operations on different shapes, tested on `(5,4,3,1)` + `(1,3,5)` |
| Multiplication | Element-wise `torch.mul` vs matrix multiplication `matmul` |
| Indexing & slicing | Multi-dimensional indexing, slicing, `.item()`, and `torch.flip()` for reversing (since `[::-1]` is not supported) |

## Key takeaways

- **Broadcasting rule:** compare shapes from the right; each pair of dimensions must be equal or one of them must be 1.
- **Trailing underscore = in-place.** Methods like `add_()` change the tensor without making a copy.
- **Tensors don't support negative-step slicing.** Use `torch.flip(tensor, dims)` instead.
- `rand` creates floats only; use `randint` for integer tensors.

## Getting started

```bash
pip install torch numpy
jupyter notebook pytroch_basics_.ipynb
```

## Status

This is a learning notebook, part of my daily ML learning journal, and still a work in progress. It covers the basics only. Next up: autograd, building and training simple neural networks, and applying PyTorch to a real dataset.

## About

I'm Tejas, a B.Tech student in Robotics & AI, building up my data science and machine learning skills in public. More notebooks and projects are in this repository.
