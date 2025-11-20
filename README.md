# Electromagnetic Green's Function & Quantum Emitter Dynamics

This repository contains numerical simulations for calculating the electromagnetic Green's function of a multi-layer structure and analyzing the dynamics of a quantum emitter coupled to a surface plasmon. The codes were developed as part of coursework. Check the full reports for context [here](https://gehadibany.github.io/files/report_p1.pdf) and [here](https://gehadibany.github.io/files/report_p2.pdf)

## Physics Parameters

* **Metallic slab:** modeled with a simple Drude model with zero hydrodynamic parameter.
* **Media:** standard dielectric constants were used.
* **Constants:** standard constants was used for speed of light and conversions.


### Files

#### 1. `p1_green_function.ipynb`
**Green's Tensor Calculation**
This notebook focuses on the fundamental electromagnetic properties of the system.
* **Physics Model:** Implements Fresnel reflection coefficients (`rij`) and total reflection coefficients (`rT`) for a thin metallic slab sandwiched between vacuum and a substrate (e.g., silica).
* **Calculations:** Computes the Real and Imaginary parts of the Green's function components ($G_{xx}$ and $G_{zz}$) via numerical integration over the wavevector $k_\rho$.
* **Visualization:** Plots the variation of Green's function components against intervals of:
    * Frequency ($\omega$)
    * Slab Thickness ($t$)
    * Dipole-Surface Distance ($z$)

#### 2. `p2_emitter_dynamics.ipynb`
**Quantum Emitter Time Evolution**
**NOTE**: This section was a numerical reproduction of the course instructor, A. González-Tudela et al's paper ["Reversible dynamics of single quantum emitters near metal-dielectric interfaces"](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.89.041402)])
This notebook uses the Green's function results obtained from the first notebook to simulate the quantum dynamics.
* **Spectral Density:** Calculates the spectral density $J(\omega)$ based on the imaginary part of the Green's function.
* **Dynamics:** Solves the integro-differential equation governing the probability amplitude $c(t)$ of the emitter's excited state.
* **Visualization:** Plots the spectral density and the population decay $|c(t)|^2$ over intervals of:
    * Wavelength (positions normalized to wavelength)
    * Time (to study the time evolution)

## Dependencies

* Python 3.x
* `numpy`
* `scipy`
* `matplotlib`

