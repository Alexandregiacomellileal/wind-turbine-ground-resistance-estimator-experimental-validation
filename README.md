# Experimental Validation of the Wind Turbine Grounding Resistance Estimator (WTGRE)

![https://github.com/Alexandregiacomellileal/Wind-Turbine-Grounding-Resistance-Estimator-Experimental-Validation](https://github.com/Alexandregiacomellileal/Wind-Turbine-Grounding-Resistance-Estimator-Experimental-Validation/blob/main/GIF-ezgif.com-video-to-gif-converter.gif)

## Associated research paper
Integrated approach for wind turbine grounding resistance estimation: Bridging clamp-on ground meter, computational simulations, and machine learning

## Overview
This repository offers comprehensive details on the experimental validation conducted for the [[computational tool](https://github.com/Alexandregiacomellileal/Update-computacional-tool)] proposed in the associated research paper. The primary objective of this tool is to precisely estimate the individual grounding resistance of wind turbines when interconnected with the wind farm's grounding system through horizontal electrodes. It serves as an ally in identifying processes of deterioration that may occur in the surrounding soil or in the electrodes within the individual grounding system of the turbine throughout the lifespan of the wind farm.

Validation experiments were conducted using a scaled-down multi-grounded system, as described below. The study involved measurements using four methods: (i) Fall-of-Potential at low frequency, (ii) Fall-of-Potential at high frequency (25 kHz), (iii) Clamp-on ground meter, and (iv) Proposed. The specific objective of this study was to compare the measurements results of these methods with the individual actual turbine grounding resistance ($Rf$, measured in Ω) obtained through Fall-of-Potential method at low frequency before the installation of horizontal electrodes.

## Experimental Setup

The computational tool proposed in the associated research paper underwent experimental validation using a reduced-scale model of the grounding system detailed in paper's Section 2.2. The grounding system was constructed with three 4 mm thick steel cylinders spaced 7.5 m apart, interconnected to a 15 m horizontal electrode. Each steel cylinder, symbolizing a turbine grounding, boasted a radius of 19.7 cm and a height of 43 cm, while the copper horizontal electrode had a cross-sectional area of 35 $mm^2$. The horizontal electrode was buried 12 cm below the ground. Each cylinder electrode was positioned on the same side at a distance of 28.5 cm from the horizontal electrode. The radial connection between the cylinder and horizontal electrodes was established using an insulated wire with a cross-sectional area of 10 $mm^2$, with a length of $s$ + 0.1 $(m)$. The soil had an average low-frequency resistivity of 86.8 Ω·m.  In Figure 1, the schematic of the grounding system is presented, capturing key moments during both its construction and the measurement process.

**Figure 1**
![experiment_git_hub (003)](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/assets/96079504/9a3bbea2-8b20-4a73-ab05-3252bbfae3fe)

## Grounding Impedance Measurement Methods

This section provides details of the measurements conducted in the case study grounding using four methods: (i) Fall-of-Potential at low frequency, (ii) Fall-of-Potential at high frequency (25 kHz), (iii) Clamp-on ground meter, and (iv) the Proposed method. The specific objective of this study was to compare the measurements results of these methods with the individual actual turbine grounding resistance (Rf, measured in Ω) obtained through Fall-of-Potential method at low frequency before the installation of horizontal electrodes.

### (i) Low-Frequency Fall-of-Potential Method using Flat-slope-rule

In Figure 2, we illustrate the application of the Fall-of-Potential (FoP) method to measure the low-frequency grounding resistance in our case study grounding system. The measuring leads have been laid along a line orthogonal to the horizontal electrode's length. A voltage $Vp$ (V) was applied by a low-frequency instrument between the electrode of interest (EE) and the auxiliary current-return electrode (CE), inducing a current $Ic$ (A) to circulate. To minimize mutual resistances, the CE was strategically placed at a substantial distance XC (m) 45 meters from EE.

Next, a Potential Electrode (PE) was positioned at a distance XP (m) from the current injection point in EE. The precise placement of the PE termed the compensation point, is crucial. It must be free from the influences of both the EE and CE. To ensure this, we systematically moved the PE in 0.1XC increments between EE and CE, capturing resistance reading at each step calculated as $( \frac{V_p}{I_c} )$. The detection of three consecutive, evenly spaced, and constant resistance readings (differences lower than 3%) was indicative of true EE grounding resistance, a principle known as the Flat-slope-rule [^4]. 

For comparison with other methods aimed at estimating the individual grounding resistances of turbines within the case study's grounding system, low-frequency Fall-of-Potential (\gls{fop}) measurements were sequentially taken at three different current injection points (turbine bonding bars 1, 2, and 3). Initially, measurements $Zmed_{FoP}^{con.}$ ($\Omega$) were conducted with the system fully connected, implying that all turbines electrodes were linked to the horizontal electrode, as depicted in Figure \ref{fig:val2}. Subsequently, measurements $Zmed_{FoP}^{disc.}$ ($\Omega$) were acquired by disconnecting the horizontal electrode from the turbine under test.

The Minipa MTR-1522 instrument was chosen to perform the FoP Low-frequency Method. The meter operates at a test frequency of 820 Hz, and the test current has a magnitude of approximately 3.2 mA. The selection of this meter was deliberate, aiming to avoid interference from the prevailing spectrum at the measurement location. This careful choice ensures accurate and reliable measurements by mitigating potential disruptions caused by the surrounding frequency range. The results obtained in this section were verified by substituting the meter MTR-1522 with a setup of equipment, including an oscilloscope, a current probe, and a function generator.

[^4]: IEEE guide for measuring earth resistivity, ground impedance, and earth surface potentials of a grounding system, IEEE Std 81-2012 (Revision of IEEE Std 81-1983) (2012) 1–86.


**Figure 2**
<img width="2076" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/0e2ae89d-a060-4546-9149-f108f7bcc970">


### (ii) High-Frequency Fall-of-Potential Method

Ground resistance meters typically operate at low frequencies, carefully chosen to avoid interference from the power system frequency and its lower harmonics. Exceptions to this general rule exist, particularly in the case of instruments operating at 25 kHz. These instruments have gained popularity due to their presumed ability to measure grounding impedance without the need to disconnect shielded wires. Originally designed for evaluating the grounding impedance of transmission line towers, these high-frequency meters have found practical applications beyond their initial scope.

One notable application is in wind farms, where these 25 kHz instruments have been repurposed to estimate the impedance of the grounding resistances of individual turbines. This adaptation involves leveraging the frequency decoupling of grounding adjacent to the measurement point.

Figure 3 shows an illustration of the High-frequency method (HFM) in the case study's grounding system. The high-frequency method consists of an adaption of the Fop method using a sinusoidal high-frequency current injection of approximately 25 mA between the electrode of interest (EE) and the current electrode (CE). The fundamental concept behind the high-frequency method is to inject a current $Ic$ (A) at a higher frequency, allowing it to predominantly circulate through the grounding turbine of interest, canceling the impact of the surrounding ground circuit. Thus, the ratio of the voltage potential $Vp$ (V) to the injected current $Ic$ provides the grounding impedance of the turbine at 25 kHz. 

**Figure 3**
<img width="2436" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/874cbb0d-c3c0-48d3-9f7f-d570b1b35d16">

To minimize mutual impedances, the CE was strategically placed at a substantial distance XC (m) 45 meters from EE. Next, a Potential Electrode (PE) was positioned at a distance XP (m) from the current injection point in EE. A common issue in measuring grounding impedance at the specific frequency of 25 kHz is the pronounced coupling effect between the leads connected to auxiliary electrodes for current and potential. This effect becomes particularly significant when these leads are laid in parallel within the ground. To address this challenge, it was adopted the configuration outlined in Figure 3. In this setup, the auxiliary electrodes for the current and the potential probes should be positioned in opposite directions along a line orthogonal to the horizontal electrode direction. This arrangement mitigates the coupling effect, providing a more accurate measurement of grounding resistance at 25 kHz [^1]. 

We systematically moved the PE in 0.1XC increments in the opposite direction away from CE, capturing resistance reading at each step calculated as $( \frac{Vp^{peak}}{Ic^{peak}} )$. The detection of three consecutive, evenly spaced, and constant resistance readings (differences lower than 3%) was indicative of the turbine of interest grounding impedance at 25 kHz.

For comparison purposes with other approaches aiming to estimate just the individual grounding resistances of turbines in the case study's grounding system, the FoP high-frequency measurements $Zmed_{HF}$ ($\Omega$) were taken at three different current injection points in EE, identified as 1, 2, and 3. It's noteworthy that the assessment of grounding impedance at high frequencies is conventionally used for understanding the behavior of the grounding circuit under the influence of direct atmospheric discharge-related currents. 

It is important to note that some 25 kHz ground meters come equipped with a built-in circuit designed to nullify the inductive component of the measured impedance, employing a technique known as 'inductive compensation'. In such instances, the meter indicates the real part of the measured impedance. However, as indicated in Table 1, with inductive compensation, the readings $R_{HF}$ (Ω) provided by the 25 kHz meter deviate even further from the low-frequency impedance value of the turbine ground. In fact, they align much more closely with the true grounding resistance of the entire system in the test $R_{system}$ ($\Omega$). Thus, for this study, we will not consider inductive compensation. This decision is made to optimize the high-frequency method, aiming to estimate the grounding resistance of the turbine under the most favorable conditions.

### Table 1 - HF Measurement Data      
| Turbine | $Zmed_{HF}$ ($\Omega$) | $θmed_{HF}$ (°) | $Rmed_{HF}$ (Ω) | $Xmed_{HF}$ (Ω) |
|---------|----------|-------|-------|-------|
| 1       | 7.58     | 31.50 | 6.46  | 3.96  |
| 2       | 7.41     | 30.96 | 6.35  | 3.81  |
| 3       | 7.50     | 30.24 | 6.48  | 3.78  |

In Table 1, the following parameters are recorded for each turbine:

- **$Zmed_{HF}$ ($\Omega$):** The measured impedance magnitude, calculated as peak voltage-to-current ratio $( \frac{Vp^{peak}}{Ic^{peak}} )$, representing the total opposition to the flow of alternating current.
- **$θmed_{HF}$ (°):** The delay angle between the voltage wave ($V_p$) and current wave ($I_c$), calculated as $(\frac{t_d \cdot 360}{T})$, represents the time delay in the waveform with a period of $T (s)$.
- **$Rmed_{HF}$ (Ω):** The real part of the measured impedance, representing resistance. Calculated as $Zmed_{HF} \cdot \cos(\theta med_{HF})$.
- **$Xmed_{HF}$ (Ω):** The imaginary part of the measured impedance, representing reactance. Calculated as $Zmed_{HF} \cdot \sin(\theta med_{HF})$.

Figure 4 displays an image captured from the oscilloscope during the field measurement of turbine 3. The channel of the blue waveform ($I_c$) is set to 10.0 mV per division, representing 20 mA per division.

**Figure 4**    
<img width="600" alt="image" src="https://github.com/Alexandregiacomellileal/Wind-Turbine-Grounding-Resistance-Estimator-Experimental-Validation/assets/96079504/281154d3-53ea-4528-bafe-1c7607c47d24">


The instruments used to apply the HFM method were: (i) Tektronix A6302 50 MHz AC Current Probe, (ii) Tektronix AM503 Current Probe Amplifier, (iii) Hantek DSO5102P 2 Channel Digital Storage Oscilloscope 100 Mhz, and
(iv) FeelTech FY3200S Function Signal Generator. 

[^1]: S. Visacro, F. H. Silveira and C. H. D. Oliveira, "Measurements for Qualifying the Lightning Response of Tower-Footing Electrodes of Transmission Lines," in IEEE Transactions on Electromagnetic Compatibility, vol. 61, no. 3, pp. 719-726, June 2019, doi: 10.1109/TEMC.2019.2915188.

### (iii) Clamp-on Ground Meter Method

Measurements Zmed <sub>CGM</sub> were conducted using the UT-278A clamp-on meter attached to the interconnection cable linking each cylinder (representing the turbine grounding) to the horizontal electrode - Figure 5.

**Figure 5**

<img width="600" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/cf96775b-1295-4e97-9a22-e15773305cf4">

### (iv) Proposed Method

The proposed solution, depicted in Figure 6, involves a systematic sequence of tasks. Initially, the process begins by accessing the technical documentation of the wind farm’s grounding system. Following this, a comprehensive survey of the parameters necessary for calculating the components of the equivalent electrical circuit is conducted. Next, an appropriate electrical circuit model is chosen for the wind farm’s grounding system. To account for variations and uncertainties, a sensitivity study is performed on parameters influencing the grounding resistance and capacitance of turbines and horizontal electrodes. Tolerance ranges are defined, considering factors such as construction non-conformities or soil and electrode deterioration. A sample vector $\textbf{P}$ is generated, with each element representing a specific grounding resistance or capacitance of a turbine or horizontal electrode. An element representing the parameter $k$ is also included to replicate the mutual coupling effect between the turbine and horizontal electrodes during clamp-on ground meter measurements. Uniform distributions are used to generate vector elements within their corresponding tolerance ranges set by the sensitivity study. The equivalent circuit of the grounding system is then loaded based on the values from the sample vector $\textbf{P}$. Subsequently, a computational simulation of the clamp-on method is performed in the equivalent electrical circuit. Instrument reading values are obtained in each turbine, resulting in an output sample vector **Z**<sub>med</sub>. This process is repeated $m$ times to generate input-output pairs [**Z**<sub>med</sub> ; **R**<sub>f</sub>] stored in a database $\mathbb{D}_{m\times2n}$ , being $n$ the numbers of turbines of the wind farm. The database is then utilized to train a machine-learning model. The trained model undergoes validation and testing to ensure accuracy and reliability. Finally, the trained model is used to predict the values of the resistances **R**<sub>f est</sub> for the n turbines based on the readings obtained via the clamp-on method during wind farm periodic inspections **Z**<sub>med </sub> . This systematic approach ensures a logical progression from data collection and circuit modeling to machine learning application, facilitating accurate predictions of turbine grounding resistances.


**Figure 6**
<img width="1752" alt="image" src="https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/assets/96079504/2fc2c2cf-371e-4eaf-b3ed-65a3858e3a96">

To assist readers who wish to replicate the experiment, we have attached two files python to the repository. The algorithm [[final_160124.py](https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/blob/main/final_160124.py)] generate the P vectors, involves performing the ATP simulation in mass, obtaining the input-output pairs [**Z**<sub>med</sub> ; **R**<sub>f</sub>], and storaging them in a database $\mathbb{D}_{1000\times6}$. Additionally, for creating the machine learning model to predict the target variables, we utilized [[final_varios_algoritmos.py](https://github.com/Alexandregiacomellileal/Computational_tool_experimental_validation/blob/main/final_varios_algoritmos.py)]. The use of 1000 input-output pairs [**Z**<sub>med</sub> ; **R**<sub>f</sub>] was sufficient to accurate results. The data was splited into two groups, with 70% of the pairs allocated for training and 30% for testing. The Mean Absolute Percentage Error obtained was 4.328 \%, and the percentage of predictions with an absolute error greater than 10\% was 5.111\%.

## Measurement Data and Percentage Error

### Table 2 - Measurement Data

| Turbine | $Rf$ ($\Omega$) | $Zmed_{FoP}^{con.}$ ($\Omega$) | $Zmed_{FoP}^{disc.}$ ($\Omega$)| $Zmed_{HF}$ ($\Omega$) | $Zmed_{CGM}$ ($\Omega$)| $Zmed_{Proposed}$ ($\Omega$)|
|-------------|--------------|------------|----------|-------------|------------|-------------|
| 1          | 40.0      | 6.28     | 34.0              | 7.58       | 37.8            | 40.0            |
| 2          | 49.0      | 6.28     | 42.3              | 7.41       | 40.5            | 48.3            |
| 3          | 39.5      | 6.25     | 30.0              | 7.50       | 37.5            | 39.5            |

In Table 2, taken as benchmarked $Rf$ ($\Omega$) represents the actual turbine grounding resistance measured by the Low-Frequency Fall-of-Potential Method using Flat-slope-rule, and $Zmed_{method}$ represents the estimated turbine grounding impedance by other measurement method evaluated in this research. The "Evaluated Measurement Method Percentage Error" in Table 3 is then calculated as $Error_{method}$ = $\frac{Zmed_{method} - Rf} {Rf} * 100$ (%). It is essential to note that the grounding resistance $Rf$ was obtained prior to the installation of horizontal electrodes.

### Table 3 - Percentage error in estimated the turbine grounding resistance Rf

| Turbine  | $Error_{FoP}^{con.}$ (%) | $Error_{FoP}^{disc.}$ (%) | $Error_{HFM}$ (%)| $Error_{CGM}$ (%)| $Error_{Proposed}$ (%)|
|------------------------------|----------------|----------------|------------------|------------------|------------------|
| 1        | -84.3        | -15.0           | -81.1         | -5.5            | -0.1            |
| 2         | -87.2       | -13.7            | -84.9         | -17.4           | -1.5            |
| 3          | -84.2      | -24.1         | -81.0         | -5.1            | 0.1             |


## Results discussions

The analysis of the presented data from Table 2 and Table 3 provides valuable insights into the performance of different grounding measurement methods of wind turbines. In an initial examination of Table 2, for the Fall-of-Potential at low frequency in the case study fully connected, it becomes evident that irrespective of the test current injection point (1,2 or 3) within the grounding system, the impedance value at low frequency $Zmed_{FoP}^{con.}$ remains constant and reflects the actual grounding resistance of the entire grounding system $R_{system}$ ($\Omega$). 


Subsequently, the FOP method  was implemented by disconnecting the horizontal electrode from the turbine's grounding under test, resulting in readings $Zmed_{FoP}^{disc.}$. Upon analysis of the data in Table 2, it was observed that these values tended to approximate the actual resistance of the turbine. However, considerable errors were still evident in Table 3, potentially attributed to the horizontal electrode remaining installed in the soil (MAPE of 17.5\%). It is worth noting that safety protocols would require the disconnection of electrical installations during such testing procedures in a real electrical environment.

For the case of the high-frequency method, due to the decoupling effect provided by the reactance of the horizontal electrodes along the measurement circuit, the impedance readings obtained for each of the current injection points presented divergent and experienced increases. However, due to the shortened length of the horizontal electrodes, these reactances were not significant enough for the method to achieve good performance in estimating the individual grounding resistances of the turbines presenting a MAPE of 82.3 % in Table 3.

On the other hand, looking at Table 3 we can see that the clamp-on-ground meter method exhibited a moderate MAPE of 9.4 %. What contributed to the CGM method's performance was a combination of the compact dimensions of the grounding system and the effect of mutual impedances among the grounding elements. Nonetheless, the limitations of \gls{cgm} in large-scale systems are acknowledged.

The proposed method surpassed all others, achieving outstanding accuracy in predicting individual grounding resistances for wind turbine systems, as evidenced by an impressive MAPE of 0.6% in Table 3. The success of our proposed method highlights its efficacy, making it a promising approach for assessments of the wind turbines' groundings. Overall, this study underscores the importance of careful method selection in grounding measurements, particularly in the context of wind energy systems, where accurate assessments are crucial for ensuring optimal performance.

________________________________________________________________________________________________________________________

### Contact us:
Please send an email to: alexgiacomelli@yahoo.com

________________________________________________________________________________________________________________________

### Contributors:
Federal University of Technology – Parana (UTFPR) and Institute of Technology for Development (LACTEC)

________________________________________________________________________________________________________________________

<p align="center">
  <img src="https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FAlexandregiacomellileal%2FWind-Turbine-Grounding-Resistance-Estimator-Experimental-Validation&label=Visitors&labelColor=%23697689&countColor=%23ff8a65" alt="Visitors Badge">
</p>

