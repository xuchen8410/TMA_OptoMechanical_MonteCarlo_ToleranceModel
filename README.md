# Multi-Mirror Opto-Mechanical Monte Carlo Framework

A modular computational framework for system-level modeling and statistical tolerance analysis of multi-mirror reflective optical systems.

---

## Overview

Unlike single-optic models—where perturbations can often be treated locally—multi-mirror optical systems exhibit strong **system-level coupling**. Mechanical, thermal, and alignment variations propagate through successive reflections, producing cumulative wavefront effects that must be evaluated through sequential system propagation.

This project provides a lightweight simulation environment that integrates:

- optical geometry
- opto-mechanical perturbations
- coordinate transformation management
- Monte Carlo tolerance analysis
- wavefront performance evaluation

The framework is designed for rapid research exploration and early-stage **STOP (Structural-Thermal-Optical Performance)** analysis.

---

## Physical Modeling Concept

In multi-mirror architectures, optical behavior is governed by coupled geometry and coordinate transformations rather than isolated surface effects.

Each mirror is represented by:

- **Rigid-body degrees of freedom**  
  (decenter, tilt, piston)
- **Surface deformation modes**  
  describing figure errors or thermo-elastic distortion
- **Local reference frames** defining mirror geometry

Global system behavior emerges from transformations between **local and global coordinate systems** during reflection and propagation.

Perturbations modify:

- surface normals  
- reflection geometry  
- optical path length  

leading to cumulative optical path differences that evolve across the optical chain. Because downstream optics depend on upstream perturbations, performance must be evaluated through **sequential propagation** instead of independent sensitivity analysis.

---

## Architecture

The framework follows a modular system architecture separating physical modeling from numerical evaluation.

### 1. System State Modeling
Stacked opto-mechanical degrees of freedom describing the complete system configuration across multiple mirrors.

### 2. Coordinate Transformation Management
Consistent handling of:

- global ↔ local reference frames
- mirror pose relationships
- inter-optic alignment
- beam coordinate propagation

### 3. Physics Propagation Engine
Sequential reflective propagation updating ray direction and optical path length using:

- local surface sag and gradients
- rigid-body mirror pose
- deformation modes

### 4. Error & Tolerance Modeling
Correlated Monte Carlo sampling representing:

- manufacturing variation
- mounting uncertainty
- alignment errors
- thermo-elastic effects

### 5. Performance Evaluation
Wavefront characterization via:

- Zernike decomposition
- statistical performance metrics
- alignment sensitivity analysis

---

## Monte Carlo STOP Analysis

Monte Carlo simulations capture realistic system variability driven by structural and thermal sources. Wavefront outputs are decomposed into Zernike modes to quantify:

- aberration evolution
- performance stability
- alignment sensitivity
- tolerance robustness

This enables scalable **system-level STOP analysis** applicable to complex reflective imaging systems.

---

## Design Philosophy

The software architecture intentionally separates:

- optical geometry
- coordinate transformations
- perturbation modeling
- propagation physics
- performance evaluation

This modularization enables:

- extension to arbitrary **N-mirror systems**
- rapid experimentation and visualization
- research-oriented prototyping
- scalable tolerance workflows

---

## Project Goals

This project bridges traditionally separated domains:

- Optical design
- Opto-mechanical modeling
- Statistical tolerance engineering

into a unified computational framework suitable for:

- early system feasibility studies
- alignment sensitivity exploration
- tolerance trade analysis
- research and algorithm development

---

## Scope

✔ Reflective multi-mirror systems  
✔ System-level perturbation modeling  
✔ Wavefront-based performance metrics  
✔ Research and prototyping workflows  

---

## Future Extensions

- GPU-accelerated Monte Carlo sampling
- Stray-light integration
- STOP co-simulation interfaces
- Optimization-driven tolerance allocation
- Hybrid ray + wave propagation models

---

## License

[Add license here]

---

## Author

**Xu Chen**  
Optics · Opto-Mechanics · Computational Photonics · STOP Analysis
