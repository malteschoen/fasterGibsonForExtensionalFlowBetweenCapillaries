[![DOI](https://zenodo.org/badge/791671677.svg)](https://doi.org/10.5281/zenodo.13999721)

## Chapter 0: Table of contents
- Chapter 1: Mission statement
- Chapter 2: Theory
- Chapter 3.1: Initial simple formula
- Chapter 3.2: Verification/Validation of initial simple formula
- Chapter 4.1: Advanced formula
- Chapter 4.2: Verification/Validation of advanced formula
- Chapter 5.1: Legacy linear formula
- Chapter 5.2: Verification/Validation of legacy linear formula
- Chapter 6: Limitations of the model
- Chapter 7: Some usage examples
- Chapter 8: Citation
- Chapter 9: Contact
- Chapter 10: Literature


## Chapter 1: Mission statement

<details>
<summary>CLICK TO EXPAND AND READ</summary>
This repository is supposed to hold information

1. on the relations between elongational/extensional viscosity AND flow rate AND elongational/extensional pressure drop
2. on the formulae developed by Gibson in the late eighties to depict these relations
3. on our newer formula that gives up some accuracy in order to become a useful tool for everyday engineering work.

</details>

## Chapter 2: Theory

The elongational pressure drop between two cylindrical capillaries according to Gibson [1] is: 
```math
\Delta p_{elong} =I \dot{\gamma}_{app,R1}^{t}\left (\frac{2}{3t}\left (\frac{sin(\alpha)(1+cos(\alpha))}{4} \right )^{t}\left ( 1- \left [ \frac{R_{1}}{R_{0}} \right ]^{3t} \right)+\frac{\phi(t,\alpha)}{4^{t}}\right)
```
With $\phi$ defined as follows 

```math
\phi(t,\alpha) = \int_{0}^{\alpha}\left \{(1+cos(\beta))^{t-1} (sin(\beta))^{t+1} \beta  \right \}  d\beta
```

The highest rate of elongation is achieved at the entrance to the R1 capillary/small capillary:
```math
\dot{\epsilon}_{circumAvg,max}= sin(\alpha)(1+cos(\alpha)) \dot{\gamma}_{app,R1}
```

<details>
<summary>ADDITIONAL NOTES - CLICK TO EXPAND AND READ</summary>
With I and t defining the elongational viscosity and the elongational stress, both following a simple power law:

$\eta_{elong} =I \dot{\epsilon}^{t-1}$

$\sigma_{elong} =I \dot{\epsilon}^{t}$

R1, R0 and alpha define the geometry of the capilliaries
- R0 is the bigger radius
- R1 is the smaller radius
- alpha is the conical half-angle (90 degrees for 'butted' capillaries, 59 degrees for holes drilled with DIN 1897 drill bits)

$\dot{\gamma}_{app,R1}$ is the apparent shear rate in the small capillary. The (circumferentially averaged) elongation rate present in the transition section between the cylindrical bores depends on the local radius R :

$\dot{\epsilon}_{circumAvg}= sin(\alpha)(1+cos(\alpha)) \frac {\dot{Q}}{R^{3}\pi}$
  
</details>



## Chapter 3.1: Initial simple formula

<details>
<summary>CLICK TO EXPAND AND READ</summary>

As seen above, $\phi$ only depends on $\alpha$ and $t$.

Considering only the term in the brackets, the influencing factors are
- Elongational viscosity power law exponent t (expected to fall between 1 and 0.25)
- Half-angle alpha (expected to fall between 30 and 90 degrees)

Hence it is easy to tabulate it and arrive at an approximation formula (in which $\alpha$ in degrees is to be input):

$\phi(t,\alpha) = max(0,\frac{1.2\alpha-33}{100})$

See figure 1 below for the quality of the approximation.

![figure1](https://github.com/malteschoen/fasterGibsonForExtensionalFlowBetweenCapillaries/blob/main/media/figure_1.png)
Figure 1: Approximation of $\phi$

However, this only eliminates the last component of Gibsons unwieldy equation. 
Considering the entire term in the brackets, the influencing factors are
- Ratio of the radii (expected to fall between 1-to-5 and 1-to-30)
- Elongational viscosity power law exponent t (expected to fall between 1 and 0.25)
- Half-angle alpha (expected to fall between 30 and 90 degrees)

We can now tabulate these results at the discrete combinations given above and develop a simpler function to represent the surface (green surface in figure 2) and plot both visually:

The function of the surface is given by:

$\frac{4}{25}\cdot t ^ \frac{5}{-3} +\frac{\alpha}{200}$

It becomes clear that the influence of the ratio of the radii is small for all t > 0.25.

![figure2](https://github.com/malteschoen/fasterGibsonForExtensionalFlowBetweenCapillaries/blob/main/media/figure_2.png)
Figure 2: Approximation of 'bracketed term' with the initial simple formula

</details>
In conclusion, for the elongational entrance pressure drop using the inital simple formula we get:

$\Delta p_{elong} =I \dot{\gamma}_{app,R1}^{t} \left ( \frac{4}{25}\cdot t ^ \frac{5}{-3} +\frac{\alpha}{200}  \right )$


## Chapter 3.2: Verification/Validation of initial simple formula

<details>
<summary>CLICK TO EXPAND AND READ</summary>

If we use the data on injection capillary rheometer entrance pressure drops given by [1] in their figure 7, we can compare our mathematical model to real-world data.
Please note that we use the power-law parameters of elongational viscosity given by [1] in their table 1.

![figure3](https://github.com/malteschoen/fasterGibsonForExtensionalFlowBetweenCapillaries/blob/main/media/figure_3.png)

Figure 3: Comparison between injection moulding dataset and the initial simple formula

Expressed in mathematical terms, our initial simple formula results in an average error of 0.5 bar or 12 % (i.e. our model usually predicts higher values) for the injection moulding data set (t = 0.77). 

However, performance for other elongational flow exponents t is unknown. Hence we compare our initial simple formula to the dataset for the bracketed term. 

![figure4](https://github.com/malteschoen/fasterGibsonForExtensionalFlowBetweenCapillaries/blob/main/media/figure_4.png)

Figure 4: Comparison between bracketed term dataset and the initial simple formula. Square symbols indicate dataset, circles our initial simple formula.

Again, it becomes clear that the influence of the ratio of the radii is notable only for t < 0.25. Performance of our initial simple formula is fair. The data for t = 1 is not matched well. Expressed in mathematical terms, our initial simple formula results in an average error of 28 %, primarily driven by the poor fit for t = 1. The single greatest error is 92 %.


</details>

## Chapter 4.1: Advanced formula

<details>
<summary>CLICK TO EXPAND AND READ</summary>
Seeing that the effect of t is non-linear we can improve the model by adding an exponent to alpha.
</details>
For the elongational entrance pressure drop using the advanced formula we get:

$\Delta p_{elong} =I \dot{\gamma}_{app,R1}^{t}  \frac{4}{5} \left ( t ^ \frac{-4}{5} +\frac{1}{53} \alpha ^ \frac{3}{4}  -1\right)$




## Chapter 4.2: Verification/Validation of advanced formula

<details>
<summary>CLICK TO EXPAND AND READ</summary>

![figure5](https://github.com/malteschoen/fasterGibsonForExtensionalFlowBetweenCapillaries/blob/main/media/figure_5.png)

Figure 5: Comparison between bracketed term dataset and the advanced formula. Square symbols indicate dataset, circles our initial simple formula.

Again, it becomes clear that the influence of the ratio of the radii is notable only for t < 0.25. Performance of our advanced formula is good. The data for t = 1 is now matched well. Expressed in mathematical terms, our initial simple formula results in an average error of 12 %, primarily driven by the poor fit for low alpha. The single greatest error is 38 %.


</details>

## Chapter 5.1: Legacy linear formula

<details>
<summary>CLICK TO EXPAND AND READ</summary>

If we are only interested in the results for intermediate values (0.5; 0.75) of t usually encountered in plastics compounds and the higher (> 50°) angles usually encountered in dies, we can create a simplified linear model.

</details>

For the elongational entrance pressure drop using the legacy linear formula we get:

$\Delta p_{elong} =I \dot{\gamma}_{app,R1}^{t} \left ( \left [ \frac{4}{3}(1-t) \right ]-\frac{\alpha}{250} \right )$

## Chapter 5.2: Verification/Validation of legacy linear formula

<details>
<summary>CLICK TO EXPAND AND READ</summary>

![figure6](https://github.com/malteschoen/fasterGibsonForExtensionalFlowBetweenCapillaries/blob/main/media/figure_6.png)

Figure 6: Comparison between bracketed term dataset and the advanced formula. Square symbols indicate dataset, circles our legacy linear formula.

Again, it becomes clear that the influence of the ratio of the radii is notable only for t < 0.25. Performance of our legacy linear formula varies. The data for alpha = 30° is not matched well. The data for t = 0.25 it not matched at all. Expressed in mathematical terms, our legacy linear formula results in an average error of 22 %. The single greatest error is 50 %.


</details>



## Chapter 6: Limitations of the model

<details>
<summary>CLICK TO EXPAND AND READ</summary>

Like every other model, this model is wrong in the sense that it does not capture the entirety of the physical processes involved. Consequently it can only serve an an useful approximation provided a specific set of conditions is met. I hope that the model - like many other engineering model - is useful still.

The model assumes:
- isothermal flow
- no shear contribution to entrance pressure loss
- isotropic material (consequently, applicability to filled materials cannot be presumed)
- no relaxation phenomena (no thixotropy, infinitely short relaxation times)

</details>

## Chapter 7: Some usage examples

<details>
<summary>CLICK TO EXPAND AND READ</summary>

WIP

</details>


## Chapter 8: Citation

You can (and should) cite this work using the DOI:

[![DOI](https://zenodo.org/badge/791671677.svg)](https://doi.org/10.5281/zenodo.13999721)

## Chapter 9: Contact

To get in touch, drop an e-mail to malte.schoen@rwth-aachen.de.


## Chapter 10: Literature
[1]  Gibson, A. G.: Die entry flow of reinforced polymers. In: Composites 20 (1989) 1, p. 57–64 - DOI: [https://doi.org/10.1016/0010-4361(89)90683-6](https://doi.org/10.1016/0010-4361(89)90683-6)


