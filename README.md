# Homework 6: Linear Programs and Shadow Prices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This is the repository for Homework 6 for [BEE 4750](https://envsys.viveks.me/), taught at [Cornell University](https://cornell.edu) in Fall 2026 by [Vivek Srikrishnan](https://viveks.me).

If enrolled in the class, a PDF of the completed notebook, **with all cells evaluated**, should be submitted to Gradescope *no later* than the due date, at 9:00pm. 50% will be deducted for late submissions, which can be accepted up to 24 hours from the original deadline.

## Learning Objectives

After completing this assignment, students will be able to:

* formulate a linear program from a word problem, with decision variables (and their units and bounds), an objective, and constraints, including a blending constraint;
* convert a linear program to standard form;
* solve a two-variable linear program graphically, and explain why its optimum is at a corner;
* identify binding constraints and find and interpret shadow prices, with units;
* decide whether to buy more of a constrained resource using a shadow price, and recognize when a shadow price stops applying;
* use the solution and shadow prices of a linear program with many decision variables, solved in `JuMP`, to explain which options the optimal plan uses.

## Repository Overview

The repository consists of the following files:

- `hw06.ipynb`: Jupyter Notebook for the homework assignment. This is the only file you should need to edit.
- `hw06.pdf`: PDF version of the homework assignment, if you don't want to rely on the Jupyter Notebook.
- `Project.toml`, `Manifest.toml`: Julia environment files. These should just work, but feel free to add other packages as needed using the `Pkg` package manager. This is the only other file that you might end up making changes to, though you should do this using `Pkg`, not directly.
- `hw06.qmd`: Source file for Jupyter notebook generation. You shouldn't need to or want to touch this; everything is in the `.ipynb` file.
- `LICENSE`: This material is licensed using the MIT license. You can ignore this for working on the problem set.
- `README.md`: This file. You shouldn't need to touch this.
- `.gitignore`: This tells `git` what files to ignore. You shouldn't need to touch this.
- `.devcontainer/`: Settings for opening this repository in GitHub Codespaces (see the course website's assignment workflow page). You shouldn't need to touch this.

## Dependencies

This notebook was written using Julia 1.11.5. Problems 1 to 3 are by hand. Problem 4 runs a `JuMP.jl` model, provided in the notebook, with the `HiGHS.jl` solver. `Plots.jl` is included in case you want to draw a feasible region in code.

## Prerequisites

1. [Install Julia](https://julialang.org/downloads/) before beginning this assignment. This notebook was developed with version 1.11.5, but any 1.11.x should work (there could be some issues with other versions, depending on what's changed).
2. If necessary, [install git](https://happygitwithr.com/install-git.html) and [create a GitHub account](https://github.com).
3. [Clone the repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository). I recommend doing this in a dedicated `BEE4750/` folder, which can also house homework assignment repositories and lecture notes. You can clone directly into the `BEE4750/` folder.   For Windows (or from another graphical interface), just create a `BEE4750` folder, then a `hw` folder inside of that, then clone into that folder. Or to clone into a `BEE4750/hw` folder, from a command prompt:
    ```bash
    cd BEE4750/
    mkdir hw
    cd hw/
    git clone https://github.com/bee-envsys-cornell/hw06.git
    ```
