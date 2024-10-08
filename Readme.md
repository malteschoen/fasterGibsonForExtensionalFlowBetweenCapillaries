## Chapter 0: Table of contents

## Chapter 1: Mission statement

<details>
<summary>CLICK TO EXPAND AND READ</summary>
This repository is supposed to hold information

1. on the relations between elongational/extensional viscosity AND flow rate AND elongational/extensional pressure drop
2. on the formulae developed by Gibson in the late eighties to depict these relations
3. on our newer formula that gives up some accuracy to have better 

and also materials for other researchers to reproduce our findings and improve on them.

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
<details>
<summary>ADDITIONAL NOTES - CLICK TO EXPAND AND READ</summary>
With I and t defining the elongational viscosity

$\eta_{elong} =I \dot{\epsilon}^{t-1}$

R1, R0 and alpha define the geometry of the capilliaries
- R0 is the bigger radius
- R1 is the smaller radius
- alpha is the conical half-angle (90 degrees for 'butted' capillaries , 59 degrees for holes drilled with DIN 1897 drill bits)

gamma_dot is the shear rate. The average (!) elongation rate is:

TBA
  
</details>

## Chapter 3: Simplifications

<details>
<summary>CLICK TO EXPAND AND READ</summary>

As seen above, $\phi$ only depends on $\alpha$ and $t$.

Hence it is easy to tabulate it and arrive at an approximation formula (in which $\alpha$ in degrees is to be input):

$\phi(t,\alpha) = max(0,\frac{1.2\alpha-33}{100})$

See figure 1 below for the quality of the approximation.

However, this only eliminates the last component of Gibsons unwieldy equation. Considering only the term in the brackets, the influencing factors are
- Ratio of the radii (expected to fall between 1-to-5 and 1-to-30)
- Elongational viscosity power law exponent t (expected to fall between 1 and 0.25)
- Half-angle alpha (expected to fall between 30 and 90 degrees)

We can now tabulate these results and plot them visually (figure 2).



</details>


## Chapter 4: Limitations of the model, guidance on pratical usage

<details>
<summary>CLICK TO EXPAND AND READ</summary>

Like every other model, this model is wrong in the sense that it does not capture the entirety of the physical processes involved. Consequently it can only serve an an useful approximation provided a specific set of conditions is met. I hope that the model - like many other engineering model - is useful still.

The model assumes:
- isothermal flow
- 
</details>

## Chapter 5: Some usage examples

<details>
<summary>CLICK TO EXPAND AND READ</summary>

TBD

</details>

## Literature
[1]  Gibson, A. G.: Die entry flow of reinforced polymers. In: Composites 20 (1989) 1, p. 57–64 - DOI: [https://doi.org/10.1016/0010-4361(89)90683-6](https://doi.org/10.1016/0010-4361(89)90683-6)


