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

<img width="600" height="800" alt="f(n)" src="https://github.com/user-attachments/assets/9150dd9b-3100-43b3-a654-13d176d9dddf" />


