# ARN-2-NOZZLE-COMPRESSIBLE-FLOW-ANALYSIS
2D axisymmetric CFD simulation and aerodynamic validation of the NASA TMR ARN2 convergent nozzle using ANSYS Fluent (k-ω SST), evaluating potential core decay, discharge coefficient (Cd = 0.988), and net thrust.

Project Summary
Geometry: NASA ARN2 Convergent Nozzle (Exit Diameter: 2.0 inches / 0.0508 m)

Operating Conditions: Subsonic Cold Jet (Mach ~ 0.51, NPR = 1.1862)

Turbulence Model: k-omega SST (NASA benchmark data uses Spalart-Allmaras)

Solver: 2D Axisymmetric, Steady-State

Mass Flow Rate: 0.4321 kg/s

Discharge Coefficient (Cd): 0.988 (98.8% aerodynamic efficiency)

Estimated Net Thrust: ~72.8 N to 74.0 N



Simulation Setup
Fluid: Air (Ideal Gas, Sutherland Viscosity)

Nozzle Inlet: Total Pressure = 120.2 kPa, Total Temperature = 294.4 K

Ambient / Farfield: Static Pressure = 101.3 kPa, Temperature = 294.4 K

Walls: Viscous No-Slip (inner wall and outer nozzle lip)


Mesh and Near-Wall Resolution

Mesh Statistics and Quality:

Total Nodes: 67820

Total Elements: 67005

Orthogonal Quality: Min 0.141, Max 1.000, Average 0.937

Skewness: Min 0.000, Max 0.795, Average 0.152

Aspect Ratio: Min 1.000, Max 247.1, Average 7.788


Wall y+ values on the inner and outer walls range between 1 and 12. The boundary layer was generated using an alternative meshing approach, as technical issues arose while enforcing the targeted edge sizing (Number of Divisions and Bias Factor) near the walls, preventing further sub-layer refinement. Nevertheless, because the kw SST model employs automatic wall functions in ANSYS Fluent, the boundary layer velocity profiles are resolved adequately without compromising overall convergence.

<img width="1105" height="441" alt="Ekran görüntüsü 2026-09-02 201540" src="https://github.com/user-attachments/assets/7d526b35-0bb1-4272-aa75-1e5e371bb5f9" />
<img width="1108" height="527" alt="Ekran görüntüsü 2026-09-02 200058" src="https://github.com/user-attachments/assets/33e91878-6635-4eef-8a5a-d38c2a45a304" />
<img width="737" height="410" alt="Ekran görüntüsü 2026-09-02 200211" src="https://github.com/user-attachments/assets/2a027ae8-3039-4c3d-88e3-a99651ded6e1" />
<img width="972" height="382" alt="Ekran görüntüsü 2026-09-02 200231" src="https://github.com/user-attachments/assets/0a845c36-e63e-4a8c-abf0-65301f7a1b70" />


Aerodynamic Results

<img width="1107" height="548" alt="Ekran görüntüsü 2026-09-02 194727" src="https://github.com/user-attachments/assets/8ae8ce47-1cd2-4821-95fc-4259d34bd911" />
<img width="987" height="552" alt="Ekran görüntüsü 2026-09-02 194930" src="https://github.com/user-attachments/assets/5180dd34-c52b-4264-9476-5bf11d4da38a" />
<img width="1002" height="547" alt="Ekran görüntüsü 2026-09-02 194942" src="https://github.com/user-attachments/assets/f9c21a3a-fe72-4cb3-b1e9-78d359057285" />
<img width="1110" height="565" alt="Ekran görüntüsü 2026-09-02 195128" src="https://github.com/user-attachments/assets/bf806bf6-1f66-4836-80bb-07f90c5b85f0" />
<img width="732" height="442" alt="Ekran görüntüsü 2026-09-02 194958" src="https://github.com/user-attachments/assets/39d9962a-b828-4956-a51e-b94ec2588de0" />
<img width="1110" height="565" alt="Ekran görüntüsü 2026-09-02 195128" src="https://github.com/user-attachments/assets/1ad0208d-c354-4b4f-aa91-0925018f7939" />
<img width="1107" height="463" alt="Ekran görüntüsü 2026-09-02 200027" src="https://github.com/user-attachments/assets/8d53464f-8523-4ae5-a91f-8dd3f5db44bc" />


Validation and Performance Dataset (Excel)
This workbook contains the numerical simulation data, benchmark comparisons, and aerodynamic performance calculations for the ARN2 nozzle study:
Experimental NASA: Centerline velocity decay benchmark measurements from NASA experimental data (x/Dj and u/Uj).

MY CFD SST MODEL: Present numerical simulation results obtained with the k-omega SST turbulence model (x/Dj and u/Uj).

NASA CFD SA: Reference CFD dataset from the NASA TMR database utilizing the Spalart-Allmaras turbulence model (x/Dj and u/Uj).

Nozzle Discharge Coefficient: Aerodynamic discharge efficiency calculated by comparing analytical mass flow rate (0.437231 kg/s) to the CFD mass flow rate (0.432083 kg/s), yielding Cd = 0.988226.

Thrust Force: Net nozzle thrust force derived from exit momentum flux, calculated as 74.028 N.

Verification Plot: Comparative chart overlaying the experimental, SST model, and SA model axial velocity distributions along the jet centerline.
[ARN 2 nozzle analysis data.xlsx](https://github.com/user-attachments/files/31749095/ARN.2.nozzle.analysis.data.xlsx)
















