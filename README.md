# 🌊 Rogue Wave Solutions with a Physics-Informed Neural Network

Research for the **D.N.S. at the Claremont Colleges**.

Rogue waves can be modeled using ODEs — and thanks to physics, we know the analytical solutions to this family of equations. This project uses a series of **custom loss functions** to select a target solution and enforce ODE satisfaction, alongside standard **MSE loss** to train against ground truth.

The goal is to document the changes and (hopefully) improvements made over the course of this research.

---

## How It Works

1. **ODE loss** — enforces that the network's output satisfies the governing equation
2. **Custom Loss Functions** — steers the network toward a specific solution in the ODE family set by setting custom loss to specfic values we want to optmize for. (eg. the height, width etc..)
3. **MSE loss** — trains against analytically-derived ground truths

---

## Goals

- Document all iterations and improvements to the network
- Experiment with custom loss function configurations
- Improve solution selectivity through loss engineering

---

*Questions or suggestions? Feel free to reach out.*
