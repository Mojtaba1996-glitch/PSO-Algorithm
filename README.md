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
- ![pso_diagram](figures/pso-latex.PNG)

```sh

\begin{figure}[h]
    \centering
    \begin{tikzpicture}
        % Define positions of points
        \coordinate (pi) at (0,0);
        \coordinate (vi) at (3,-3);
        \coordinate (pbest) at (2,1.25);
        \coordinate (gbest) at (5,-1);
        \coordinate (newpos) at (4,-1.3);
        \coordinate (pp) at (2,-.85);
        \coordinate (vv) at (1.20,-1.25);
        
        % Draw circles indicating the zones
        \draw[dashed, blue] (2,1.25) circle (1);
        \draw[dashed, blue] (5,-1) circle (2);

        % Draw velocity vector
        \draw[->, thick] (pi) -- ++(vi) node[midway, left] {$v_i$};

        % Draw directional arrows to pbest and gbest
        \draw[->, thick,dotted] (pi) -- (pbest);
        \draw[->, thick,dotted] (pi) -- (gbest);
        
        % Arrows towards new position
        \draw[->, thick, blue] (pi)  -- (vv);
        \draw[->, thick, blue] (1.20,-1.25) -- (pp);
        \draw[->, thick, blue] (2,-.85) -- (newpos);
        
        % Nodes for points
        \fill (pi) circle (3pt) node[below] {$p_i$};
        \fill (pbest) circle (3pt) node[below] {$p_{i,\text{best}}$};
        \fill (gbest) circle (3pt) node[below] {$\mathbf{g}_{\text{best}}$};
        \fill[orange] (newpos) circle (3pt) node[below] {\textcolor{orange}{The new position}};
        
        % Labels
        \node[above] at (pi) {Current position};
        \node[above] at (pbest) {The best experience position};
        \node[above] at (gbest) {The best particle position};

    \end{tikzpicture}
    \caption{Illustration of particle movement in PSO algorithm.}
    \label{fig:pso_movement}
\end{figure}
