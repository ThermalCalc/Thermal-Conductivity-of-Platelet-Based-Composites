# Thermal-Conductivity-of-Platelet-Based-Composites
Calculation of effective thermal conductivity of platelet-based compositions.
1. Introduction
This program is a web-based computational tool for predicting the effective thermal conductivity (keff) of polymer composites filled with anisotropic platelet-shaped fillers, such as hexagonal boron nitride (hBN), graphene, and related two-dimensional materials.
The calculator integrates the effects of:
	Geometrical characteristics of platelet fillers
	In-plane and through-plane anisotropic thermal conductivities of fillers
	Filler volume fraction
	Filler-matrix interfacial thermal resistance (Ri)
	Filler-filler contact thermal resistance (Rc)
	Filler orientation factor (cos²θ)
It is designed for rapid evaluation and parametric analysis of thermal transport behavior in platelet-based composites under multi-parameter coupling conditions.

2. Model Description
The implemented model is based on unit-cell analysis and equivalent thermal resistance network theory, and distinguishes two filler loading regimes:
	Low filler loading regime: \mathbit{V}_\mathbit{f}\le\frac{\mathbit{d}}{\mathbf{2}\mathbit{a}}
	High filler loading regime: \mathbit{V}_\mathbit{f}>\frac{\mathbit{d}}{\mathbf{2}\mathbit{a}}
Where a is the radius of platelet filler, d is the thickness of platelet filler.
The model independently calculates:
	Through-plane effective thermal conductivity k⊥
	In-plane effective thermal conductivity k∥
The overall effective thermal conductivity is obtained by orientation-weighted averaging:
\mathbit{k}_{\mathbit{eff}}=\mathbit{k}_\bot{\mathbit{cos}}^\mathbf{2}\mathbit{\theta}+\mathbit{k}_\parallel{\mathbit{sin}}^\mathbf{2}\mathbit{\theta}

3. Input Parameters
3.1 Filler Geometry
Parameter	Description	Unit
a	Radius of platelet filler	m
d	Thickness of platelet filler	m
Both manual input and predefined typical dimensions are supported.

3.2 Volume Fraction
Parameter	Description
Vf	Filler volume fraction

3.3 Thermal Conductivity Parameters
Parameter	Description	Unit
km	Thermal conductivity of matrix	W·m⁻¹·K⁻¹
kf⊥	Through-plane thermal conductivity of filler	W·m⁻¹·K⁻¹
kf∥	In-plane thermal conductivity of filler	W·m⁻¹·K⁻¹

3.4 Interfacial and Contact Thermal Resistance
Parameter	Description	Unit
Ri	Filler-matrix interfacial thermal resistance	m²·K·W⁻¹
Rc	Filler-filler contact thermal resistance	m²·K·W⁻¹
Note: The interfacial thermal resistance and the filler-filler contact thermal resistance can be obtained either from experimental measurements or directly calculated using theoretical or numerical models.

3.5 Orientation Factor
Parameter	Description
cos²θ	Orientation factor of platelet fillers
Note: cos²θ = 1: fully through-plane aligned; cos²θ = 0: fully in-plane aligned; cos²θ ≈ 1/3: random orientation approximation.

4. How to Use
	Open index.html directly in any modern web browser
	Enter or select all required parameters
	Click “Calculate the effective thermal conductivity (keff)”
	The calculated result will be displayed at the bottom of the page as: keff: XX.XX W/m·K
⚠ No message will appear if any parameter is missing.

5. Key Features
✅ No backend required — runs entirely on HTML + JavaScript;
✅ Supports both continuous input and engineering-friendly preset values;
✅ Automatically switches between low- and high-filler-loading regimes;
✅ Explicit separation of in-plane and through-plane thermal contributions;
✅ Independent control of interfacial and contact thermal resistances.

6. Notes and Limitations
	The model is applicable to platelet-dominated heat conduction composites;
	In the high-filler-loading regime, results are sensitive to Ri and Rc
	Input parameters should satisfy geometric and physical constraints
	The results are intended for theoretical analysis and trend comparison, not as direct substitutes for experimental measurements
7. Typical Applications
	Design of high-thermal-conductivity polymer composites;
	Optimization of platelet filler size and orientation;
	Analysis of interfacial engineering effects on thermal transport;
	Model-experiment comparison and validation.
