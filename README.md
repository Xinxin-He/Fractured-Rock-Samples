# Fractured-Rock-Samples

This repository contains sample scripts and 3D surface files for simulating fractured rock using **PFC3D**. 
The files include various input parameters, assembly scripts, and auxiliary files that facilitate fracture 
development experiments.

---

## Contents

### Data Folder

This folder contains compressed `.stl` files representing rough surfaces. The `.7z` archives can be 
decompressed and then loaded into PFC3D scripts:

- **len0.1_wdt0.1_rmsh0.0005_wlx0.005_wly0.005.stl.7z**
- **len0.1_wdt0.1_rmsh0.0005_wlx0.015_wly0.015.stl.7z**
- **len0.1_wdt0.1_rmsh0.0015_wlx0.005_wly0.005.stl.7z**

Each archive contains an STL file of a rough rock surface that can be used in the particle flow simulations(PFC3D).

### PFC3D Scripts

- **Initial_parameters.p3dat**  
  Defines the initial model and input parameters for PFC3D.

- **Assemble.p3dat**  
  Assembles two halves of a rock model in PFC3D.

- **Parallel_bonded.p3dat**  
  Inserts parallel bonding between rock particles in the model.

- **Closing_gap.p3dat**  
  Closes the fracture gap before loading (to reduce simulation runtime).

- **Measurements_circles.p3dat**  
  Inserts fiducial measurement spheres for tracking porosity characteristics.

- **Ss_wall.fis**  
  Defines controlled walls for boundary conditions in PFC3D.

- **Fracture_development.p3fis**  
  Tracks fracture development throughout the simulation.

---

## Usage

1. Extract the `.stl` files from the `.7z` archives in the `Data` folder if you wish to visualize or 
   modify the rough surfaces outside of PFC3D.
2. Use the provided `.p3dat` and `.fis` scripts within the PFC3D environment in the order that best fits 
   your workflow:
   - Load **Initial_parameters.p3dat** and **Assemble.p3dat** to create and assemble the rock model.
   - Apply **Parallel_bonded.p3dat** if you need to bond particles.
   - Optionally run **Closing_gap.p3dat** to close the fracture gap and reduce computational time.
   - Insert fiducial measurement spheres with **Measurements_circles.p3dat**.
   - Use **Ss_wall.fis** to set up servo walls for boundary conditions.
   - Run **Fracture_development.p3fis** to track fracture initiation and propagation.
---


## Contact

For any questions or suggestions regarding these scripts and data files, please contact via xkh5114@psu.edu or xinxinheest@gmail.com.
