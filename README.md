# PSO Algorithm - LaTeX Implementation

This repository contains a **LaTeX implementation** of the **Particle Swarm Optimization (PSO) algorithm visualization** using the `TikZ` package.

## 📜 Description
The figure illustrates how a particle moves in PSO based on:
- Its **current velocity** ($v_i$)
- Its **personal best position** ($p_{best}$)
- The **global best position** ($g_{best}$)

This helps visualize how particles update their positions in search of the optimal solution.

## 🛠️ Requirements
- A LaTeX editor (Overleaf, TeXStudio, or VS Code with LaTeX extension)
- `TikZ` package for drawing the figure
- Optionally, `pdflatex` to compile locally

## 📂 Files
- `main.tex` - The main LaTeX code
- `pso_diagram` - Standalone TikZ figure

```sh
pdflatex main.tex
