# Numerical Simulation of Aquifers

This was a group project assesed via in person presentation for the module Math of Sust & Environment (ACM41010). The Members of the group were Myslef, Sean White and Nicola Young.

The project aimed to solve nonlinear PDEs modelling aquifer behaviour, compute river fluxes, and fit model parameters to real hydrograph data.

***
## 1-Height of the Aquifer

### Governing equations 

- **Drought:**
  
$$ \hat{h}_{\hat{t}} = (\hat{h}  \hat{h}_{\hat{x}})_{\hat{x}} $$

- **Rainfall:**
  
$$ \hat{h}_{\hat{t}} = (\hat{h}  \hat{h}_{\hat{x}})_{\hat{x}} + 1 $$

These equations were then reduced to ODEs. Separation of variables was used for the drought equation, while similarity solutions were applied to the rainfall equation. We then used the shooting method to solve the resulting ODEs.

<p align="center">
  <img width="45%" height="1196" alt="X(x)" src="https://github.com/user-attachments/assets/349de884-1d22-4520-b408-d81fdfc980d1" />
  <img width="45%" height="1198" alt="f(n)" src="https://github.com/user-attachments/assets/544973fa-c090-4ed9-b40d-912d8c0a9424" />

</p>

## 2-Calculating Flux

### Governing equations 

- **Drought:**
  
$$ \hat{Q}_0 = -\hat{t} f(0) f'(0) = -\frac{C^2 \hat{t}}{2}  $$

- **Rainfall:**
  
$$ \hat{Q}_0 = -\frac{X(0) X'(0)}{ (\hat{t} + A)^2} = -\frac{D^2}{2(\hat{t} + A)^2} $$

The constants C and D are determined from the previously obtained numerical solutions. The parameter A accounts for the transition between drought and rainfall, ensuring continuity in the resulting graph.

<p align="center">
  <img src="https://github.com/user-attachments/assets/17e702c9-4628-4a54-b8f6-03179da9ac85" width="50%" alt="f(n)" />
</p>

## 3-Parameter Fitting to Real Data

Upon re-dimensionalising the flux, two parameters naturally emerged from the equations, denoted P1 and P2. These model parameters were fitted to USGS hydrograph data from four U.S. regions using least-squares minimisation. The resulting models showed strong agreement with observed hydrographs, accurately capturing peak flow and decay across a range of natural conditions.

<p align="center">
  <img src="https://github.com/user-attachments/assets/2e320d67-9b3f-4f92-b671-f244076a5d15" width="45%" alt="p1" />
  <img src="https://github.com/user-attachments/assets/375c3bb0-b829-40e4-a316-fbfc77af3019" width="45%" alt="p2" />
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/11712688-474a-47aa-8a8e-7249835c7c22" width="45%" alt="p3" />
  <img src="https://github.com/user-attachments/assets/603cf468-2e78-460a-a330-e9ade8b4c29b" width="45%" alt="p4" />
</p>



