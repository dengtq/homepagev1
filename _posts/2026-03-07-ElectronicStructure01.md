---
layout: post
title: Electronic structure I. Hamiltonian and atomic orbitals
date: 2026-03-07 15:00:00
description: Hamiltonian and orbitals
tags: Electronic
categories: Fundamentals
---

# Preface

This is a series to introduce some basics of electronic structure theory and
calculation for students. I wrote this very casually and I hope it would be
concise and understandable. Any mistake/typo is possible and feedbacks are welcomed.

# Schrödinger equation

Let's start from the original time-dependent Schrödinger equation in position-space representation,

$$\hat{H} \Psi(\mathbf{r}, t) = i\hbar \frac{\partial}{\partial t}\Psi(\mathbf{r}, t).$$

which means that the evolution of wavefunction $$\Psi$$ over time $$t$$ depends on the Hamiltonian $$\hat{H}$$.
When $$\hat{H}$$ is not explicitly varying over time, we also have a time-independent version

$$\hat{H}\psi(\mathbf{r}) = E \psi(\mathbf{r}).$$

The $$n$$-th solution $$\psi_n$$ is an eigenstate of $$\hat{H}$$.
Here $$\psi_n(\mathbf{r})$$ is the eigenstate wave function and $$E_n$$ the corresponding eigenvalue.
The eigenstate is special in the sense that if we assume

$$\Psi(\mathbf{r}, t)=\psi_n(\mathbf{r})\tau_n(t),$$

the time-dependent equation leads to

$$\tau_n(t) = c_n e^{-iE_n t/\hbar}$$

This means that when a system is in an eigenstate, only the overall phase evolves over time and its probability amplitude (electron density)

$$\rho(\mathbf{r},t)=|\Psi(\mathbf{r},t)|^2 = |\psi_n(\mathbf{r})|^2$$

is time-independent. And it will stay in that state without perturbation.

# Hamiltonian and atomic orbitals

For a single electron in a potential field $$V(\mathbf{r})$$, the Hamiltonian $$\hat{H}$$ is

$$\hat{H} = \hat{T} + \hat{V}= -\frac{\hbar^2}{2m_e}\nabla^2 + V(\mathbf{r}).$$

The first term is the kinetic energy term, and the second the potential energy term.

One of the simplest systems is the hydrogen atom. After making several approximations, its Hamiltonian is as simple as

$$\hat{H} = -\frac{\hbar^2}{2m_e}\nabla^2 + \frac{e^2}{4\pi\varepsilon_0}\frac{1}{|\mathbf{r}|}.$$

Its solution is the Bohr (hydrogenic) model, where the eigenvalues are

$$E_n = -\frac{1}{n^2} \text{Ry},$$

and the eigenstate wavefunctions (atomic orbitals) are writen in spherical coordinates

$$\psi_{nlm}(\rho, \theta, \varphi) = c_{nlm} L_{n-l-1}^{2l+1}\left(\frac{2}{na_0}r\right)Y_{l}^{m}(\theta,\varphi).$$

Here $$n$$ is the principal quantum number which corresponds to the electron shell.

$$l$$ is the azimuthal quantum number that corresponds to the $$s, p, d, \cdots$$ orbitals.

$$m$$ is the magnetic quantum number that corresponds to the orbital orientation
$$p_x, d_{xy}, \cdots$$ if one uses the real form of spherical harmonics $$Y_{l}^{m}$$.

For atoms beyond hydrogen, $$V(\mathbf{r})$$ becomes $$\frac{Z^2e^2}{4\pi\varepsilon_0}\frac{1}{|\mathbf{r}|}$$.
On top of that, there are many more electrons that interact with each other.
And the spin-orbit interaction also kicks in.
Therefore, the effective potential felt by an electron is more complex.
However, the atomic orbitals can still be roughly classified according to $$nlm$$.
These atomic orbitals for different atoms form a basis called atomic basis.
