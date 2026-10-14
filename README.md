README --- ANSYS Mechanical Structural Analysis Report
Project overview
This project contains an ANSYS Mechanical 2026 R1 Static Structural
analysis report for a concrete-and-rebar beam/structural model. The
report includes imported geometry, material definitions, symmetry,
contact connections, meshing, boundary conditions, solver information,
and post-processing results.
The uploaded report filename refers to an MWCNT project, but the
material data shown in the report lists Concrete, Bearing, and
Rebar. The report does not clearly document a separate MWCNT
material assignment, so do not assume that the numerical results
independently prove an MWCNT enhancement effect.
Model and analysis setup
- Software version: ANSYS Mechanical 2026 R1
- Analysis type: Static Structural
- Solver target: Mechanical APDL
- Unit system: Metric (m, kg, N, s); temperature in °C
- Environment temperature: 22 °C
- Geometry: Imported 3-D geometry; reported bounding box
  approximately 0.5 m × 1.1 m × 2.0 m
- Bodies: 7 active bodies
- Mesh: Coarse, linear elements; 940 nodes and 568 elements
- Connections: 2 active contact connections; listed contact
  regions are bonded
- Symmetry: 2 symmetry regions are defined
- Analysis steps: 1 step, ending at 1 s, with 25 substeps
- Large deflection: Off
- Solution status: Solved
Boundary conditions
The report lists a fixed support scoped to one face and a displacement
boundary condition with the Y component set to 1 m (ramped) while
the X and Z components are free. Confirm that this is the intended
loading condition before interpreting the results as representative of a
real service load.
Reported result highlights
At the final reported time of 1 s, the results table reports:
  Result                         Reported minimum   Reported maximum
  X-directional deformation             −1.3449 m            1.345 m
  Equivalent total strain       1.3571 × 10⁻⁶ m/m         14.301 m/m
  Normal stress X                −7.8862 × 10⁸ Pa    8.5695 × 10⁸ Pa
  Normal stress Z                −4.2581 × 10⁸ Pa    8.4095 × 10⁸ Pa
  Total reaction force                        ---     8.4816 × 10⁶ N
The report gives an average X-directional deformation of 1.4108 × 10⁻⁵ m
and an average equivalent total strain of 0.3738 m/m. These values are
reproduced from the report and have not been independently validated.
Important interpretation and validation notes
The reported deformation (about ±1.345 m), equivalent strain (maximum
14.301), and stresses (up to approximately 857 MPa in X and 841 MPa in
Z) are very large for many ordinary reinforced-concrete service-load
cases. They may indicate an overly large imposed displacement,
unsuitable or inconsistent material properties, unit/geometry issues,
contact or constraint problems, or a model that is not intended to
represent service conditions.
Before using these results in a design or research conclusion:
1. Verify the loading: Confirm whether the 1 m Y-direction
   displacement is intentional. Replace it with the intended
   displacement or applied service load if appropriate.
2. Check material properties and units: Review the reported
   concrete Young's modulus of 9.5 × 10¹¹ Pa and the listed strengths,
   as these values appear unusually high for conventional concrete.
   Confirm the units and intended material model.
3. Review the geometry and mesh: Inspect the imported geometry,
   element quality, and mesh convergence. The report identifies the
   mesh as coarse.
4. Check constraints and contacts: Confirm that supports, symmetry
   regions, and bonded contact pairs correctly represent the physical
   structure.
5. Assess convergence and plausibility: The report marks the
   solution as solved and lists zero Newton--Raphson residuals and zero
   identified element violations. This alone does not establish that
   the model is physically valid; inspect solver logs, reaction
   balance, and deformation/stress contours.
6. Evaluate cracking carefully: The report includes strain and
   stress results but does not show a clearly identified
   crack-propagation or damage-evolution result. Do not claim that
   crack propagation has been simulated unless an appropriate concrete
   damage/cracking model and corresponding outputs are present.
7. Do not infer tensile/compressive capacity directly from contour
   extrema: Compare stresses with verified material strengths using
   the correct failure criteria and a validated material model.
Material data listed in the report
- Concrete: Isotropic elasticity and nonlinear/dilatancy-related
  properties are listed.
- Bearing: Isotropic elasticity is listed.
- Rebar: Isotropic elasticity and bilinear isotropic hardening are
  listed; the reported yield strength is 1.204 × 10⁹ Pa.
Check all material definitions in the original ANSYS project before
reuse, particularly values, units, and which bodies each material is
assigned to.
Suggested workflow to reproduce the analysis
1. Open the source project in ANSYS Workbench/Mechanical 2026 R1 or a
   compatible version.
2. Confirm that the imported geometry and all seven bodies are present.
3. Review material assignments, coordinate systems, symmetry, contacts,
   and support/displacement conditions.
4. Generate the mesh and inspect mesh quality.
5. Solve the Static Structural analysis.
6. Add or review directional deformation, equivalent strain, normal
   stress X, normal stress Z, and force reaction results.
7. Compare results with material strengths and appropriate
   serviceability limits only after validating the model and load case.
8. Save the project and export an updated report with the confirmed
   settings and results.
Files and scope
This README describes the uploaded 24-page ANSYS Mechanical report. The
report references a source geometry path on the original author's
computer; that local path may not exist on another computer. The report
document alone may not contain the full editable Workbench project,
geometry, solver database, or all supporting files.
Disclaimer
This is a summary of the report, not a certification of structural
safety or a substitute for engineering verification. The model setup and
reported extreme values should be checked before drawing design,
durability, service-load, or material-performance conclusions.
