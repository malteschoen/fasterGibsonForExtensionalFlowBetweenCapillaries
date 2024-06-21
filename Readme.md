# fasterGibsonForExtensionalFlowBetweenCapillaries

## What is this?

This repository is supposed to hold information

1. on the relations between elongational/extensional viscosity AND flow rate AND elongational/extensional pressure drop
2. on the formulae developed by Gibson in the late eighties to depict these relations
3. on our newer formula that gives up some accuracy to have better 

and also materials for other researchers to reproduce our findings and improve on them.

## How can I use this?

WIP

## The theory behind it
The elongational pressure drop according to Gibson [1] is: 

```math
\Delta p_{elong} =I \dot{\gamma}_{app,R0}^{t}
\left (\frac{2}{3t}
\left (\frac{sin(\alpha)(1+cos(\alpha))}{4} 
\right )^{t}
\left ( 1- \left [ \frac{R_{1}}{R_{0}} \right ]^{3t} \right)
+\frac{\phi(t,\alpha)}{4^{t}}
\right )
```
With I and t defining the elongational viscosity

```math
\eta_{elong} =I \dot{\epsilon}^{t-1}
```

R1, R0 and alpha define the geometry of the capilliaries
- R0 is the bigger radius
- R1 is the smaller radius
- alpha is the conical half-angle (90 degrees for 'butted' capillaries , 59 degrees for holes drilled with DIN 1897 drill bits)

Finally, phi defined as follows 

```math
\Phi(t,\alpha) = \int_{0}^{\alpha}\left \{(1+cos(\beta))^{t-1} (sin(\beta))^{t+1} \beta  \right \}  d\beta
```

## Literature
[1]  Gibson, A. G.: Die entry flow of reinforced polymers. In: Composites 20 (1989) 1, p. 57–64 - DOI: [https://doi.org/10.1016/0010-4361(89)90683-6](https://doi.org/10.1016/0010-4361(89)90683-6)


## What else should I know about?
(c) Malte Schön, 2022-2024
