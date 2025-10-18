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
