## Computational_tool_experimental_validation - Reduced Scale

**Figure 1** - **High frequency method**
<img width="2435" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/dca3dd3d-abc3-46c6-b430-6bc2db7ba648">


### Under construction

A common issue in measuring grounding resistance at the specific frequency of 25 kHz is the pronounced coupling effect between the leads connected to auxiliary electrodes for current and voltage. This effect becomes particularly significant when these leads are laid in parallel within the ground. To address this challenge, it is recommended to adopt the configuration outlined in Figure 1. In this setup, the auxiliary electrodes for the current and the voltage probes should be positioned in opposite directions along a line orthogonal to the horizontal electrode direction. This arrangement mitigates the coupling effect, providing a more accurate measurement of grounding resistance at 25 kHz [-1].


[1] S. Visacro, F. H. Silveira and C. H. D. Oliveira, "Measurements for Qualifying the Lightning Response of Tower-Footing Electrodes of Transmission Lines," in IEEE Transactions on Electromagnetic Compatibility, vol. 61, no. 3, pp. 719-726, June 2019, doi: 10.1109/TEMC.2019.2915188.

**Figure 2** - **Clamp-on ground meter method**

<img width="600" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/224314f7-6d26-4264-884d-75a5cc9f7a91">




**Figure 3** - **Proposed method**
<img width="1752" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/2fc2c2cf-371e-4eaf-b3ed-65a3858e3a96">


**Figure 4** - **Low-Frequency Fall-of-Potential Method**
<img width="2130" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/a047e545-e236-4100-bbfe-301e5815f511">

**Figure 5** - **Low-Frequency Fall-of-Potential Method**
<img width="2071" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/93ecf1d2-bf40-417c-87ba-05becf5aef29">


## Results

| Turbine | 1     | 2     | 3     |
|---------|-------|-------|-------|
| Rf      | 40    | 49    | 39.5  |
| Zmed_FoP_LF (MTR-1522) | 6.28  | 6.28  | 6.25  |
| Zmed_FoP_LF (Scope)   | 6.91  | 6.95  | 6.94  |
| Zmed_FoP_HF (Scope)   | 10.33 | 9.61  | 9.86  |
| Zmed_CGM (UT278A)     | 37.8  | 40.5  | 37.5  |
| Zmed @ Proposed Solution | 39.9  | 48.9  | 39.5  |
| Abs. Error (%) (Zmed_FoP_LF MTR-1522) | 5.10% | 0.00% | -0.63% |
| Abs. Error (%) (Zmed_FoP_LF Scope)   | 13.28% | 17.35% | 16.00% |
| Abs. Error (%) (Zmed_FoP_HF Scope)   | 32.39% | 1.14% | 3.64% |
| Abs. Error (%) (Zmed_CGM UT278A)     | 7.41%  | 19.75% | 4.00% |
| Abs. Error (%) (Zmed @ Proposed Solution) | 0.25%  | 1.84%  | 0.00% |





