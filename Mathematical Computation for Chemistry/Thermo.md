
# Entropy
$$S = f(U,V)$$
$$dS = \frac{1}{T}dU + \frac{P}{T}dV$$
$$\int dS = S = \frac{U}{T} + \frac{PV}{T}$$
# Internal Energy
$$U = f(S,V)$$
$$dU = TdS - PdV$$
$$\int dU = U = TS - PV$$
# Enthalpy
$$H = f(S,P)$$
$$dH = TdS + VdP$$
$$\int dH = H = TS + PV$$
# Helmholtz Free Energy
$$A = f(T,V)$$
$$dA = -SdT - PdV$$
$$\int dA = A = U - PV$$
# Gibbs Free Energy
$$G = f(T,P)$$
$$dG = -SdT + VdP$$
$$\int dG = G = U + PV - TS$$

# Measurable Quantities
|Name|Variable|Expression|
|-:|:-:|:-:|
|Pressure|P|-|
|Volume|V|-|
|Temperature|T|-|
|Amount|N |-|
|Heat Capacity <br>constant volume|$$C_V$$|$$\left(\frac{\delta S}{\delta T}\right)_V$$|
|Heat Capacity<br>constant pressure|$$C_p$$|$$\left(\frac{\delta H}{\delta T}\right)_P$$|
|Isothermal Compressibility|$$\kappa_t$$|$$-\frac{1}{V}\left(\frac{\delta V}{\delta P}\right)_T$$|
|Thermal Expansivity|$$\alpha_p$$|$$\frac{1}{V}\left(\frac{\delta V}{\delta T}\right)_P$$|

# Calculus Manipulations for Multivariable Functions

## Basic Trickery
### Total Derivative
    restrictions - none, you can do this at anytime
let P be some function of volume, V, and temperature, T,
$$ P = f(V,T) $$
the total derivative of P,
$$ dP = \left(\frac{\delta P}{\delta V}\right)_TdV+\left(\frac{\delta P}{\delta T}\right)_VdT$$

### Holding a Variable Constant
    restrictions - none, you can do this at anytime
When you hold a variable constant, you will force any derivative of that constant in the equation to be reduced to 0, for example,
let P be some function of V and T,
$$ P = f(V,T) $$
the total derivative of P,
$$ dP = \left(\frac{\delta P}{\delta V}\right)_TdV+\left(\frac{\delta P}{\delta T}\right)_VdT$$
holding P constant, results in all instances of dP (the derivative of P) to become 0, i.e. dP = 0
$$ 0 = \left(\frac{\delta P}{\delta V}\right)_TdV+\left(\frac{\delta P}{\delta T}\right)_VdT$$
note that the partial derivatives of P (indicated with a $\delta$ symbol) are not effected by holding the variable constant.

### Inversion
    restrictions - none, you can do this at anytime
let P be some function of V and T,
$$ P = f(V,T) $$
$$\left(\frac{\delta P}{\delta V}\right)_T = \frac{1}{\left(\frac{\delta V}{\delta P}\right)_T}$$

### Triple Product
    restrictions - none, you can do this at anytime
let P be some function of V and T,
$$ P = f(V,T) $$
the triple is defined as,
$$ \left(\frac{\delta P}{\delta V}\right)_T\left(\frac{\delta V}{\delta T}\right)_P\left(\frac{\delta T}{\delta P}\right)_V = -1$$
any algebraic rearrangement of partial derivative expressions is allowed,
$$ \left(\frac{\delta P}{\delta V}\right)_T=-\frac{1}{\left(\frac{\delta V}{\delta T}\right)_P\left(\frac{\delta T}{\delta P}\right)_V}=-\frac{\left(\frac{\delta T}{\delta V}\right)_P}{\left(\frac{\delta T}{\delta P}\right)_V}=-\left(\frac{\delta T}{\delta V}\right)_P\left(\frac{\delta P}{\delta T}\right)_V$$
### Potential Transformation
    when - only when you a working with a potential and need to turn into another potential
    restrictions - the potentials must be related through a common a fundamental definition (see example below)
in general,
$$ \left(\frac{\delta F_1/X}{\delta X}\right)= -\frac{F_2}{X^2}$$
A specific example of transforming the helmholtz energy into internal energy. To do this, start with the fact that 
$$ U = A + TS$$
and we also know (from other calculations)
$$ S =\left(\frac{\delta A}{\delta T}\right)_V $$
substituting S,
$$ U = A + T\left(\frac{\delta A}{\delta T}\right)_V$$
divide both sides by $T^2$,
$$ \frac{U}{T^2} = \frac{A}{T^2} - \frac{1}{T}\left(\frac{\delta A}{\delta T}\right)_V$$
the right hand side of the previous equation is just a derivative using the chain rule:
$$ -\left(\frac{\delta A/T}{\delta T}\right)_V = \frac{A}{T^2} - \frac{1}{T}\left(\frac{\delta A}{\delta T}\right)_V$$
which means we can transform one potential to another as long as they are related by at least one natural variable:
$$ \left(\frac{\delta A/T}{\delta T}\right)_V = -\frac{U}{T^2}$$
### Non-Natural Derivatives
    when - you can do this at anytime
    restrictions - none
What if we know that U is some function of S and V,
$$ U = f(S,V) $$
but we don't know exactly how $f(S,V)$ is defined (for the sake of this example). We want to find out how the internal energy of the system changes with volume while being held at constant pressure,
$$\left(\frac{\delta U}{\delta V}\right)_P =~ ? $$
the total derivative of U,
$$ dU = \left(\frac{\delta U}{\delta S}\right)_VdS+\left(\frac{\delta U}{\delta V}\right)_SdV$$
At first glance, this seems to be an impossible problem to solve for, since internal energy, U, does not depend on pressure. How can you solve for something that isn't even defined in the original function? This process is refereed to as a non-natural derivative (sometimes called unnatural).

First, divide both sides by dV
$$ \frac{dU}{dV} = \left(\frac{\delta U}{\delta S}\right)_V\frac{dS}{dV}+\left(\frac{\delta U}{\delta V}\right)_S$$
then hold P constant, any partial derivative that is already being held constant is not effected by this,
$$ \left(\frac{\delta U}{\delta V}\right)_P = \left(\frac{\delta U}{\delta S}\right)_V\left(\frac{\delta S}{\delta V}\right)_P+\left(\frac{\delta U}{\delta V}\right)_S$$
At this point we have achieved our objective, we have an expression for the change internal energy with respect to volume at constant pressure without knowing the exact nature of $f(S,V)$. 
#### Why Non-Natural Derivatives Are Important
Sometimes the expressions that we derive are not easy to measure (if possible at all) but by careful inspection we discover some unlikely things. Consider internal energy again that $U = f(S,V)$.  We actually do know how $f(S,V)$ is defined (because we can define it however we want).
$$ U = f(S,V) = TS - PV $$
$$ dU = TdS - PdV$$
$$ \frac{dU}{dV} = T\frac{dS}{dV} - P$$
Consider the derivative of internal energy and then hold P constant
$$ \left(\frac{\delta U}{\delta V}\right)_P = T\left(\frac{\delta S}{\delta V}\right)_P- P$$
looking back at our non-natural derivative results of $U = f(S,V)$, 
$$ \left(\frac{\delta U}{\delta V}\right)_P = \left(\frac{\delta U}{\delta S}\right)_V\left(\frac{\delta S}{\delta V}\right)_P+\left(\frac{\delta U}{\delta V}\right)_S$$
it becomes clear (not really but it makes us sound smart) that,
$$ T = \left(\frac{\delta U}{\delta S}\right)_V $$
and
$$ P = -\left(\frac{\delta U}{\delta V}\right)_S $$
substituting them back into the non-natural derivative result,
$$ \left(\frac{\delta U}{\delta V}\right)_P = T\left(\frac{\delta S}{\delta V}\right)_P+P$$
let P become a variable again,
$$ \frac{dU}{dV} = T\frac{dS}{dV}+P$$
multiply both sides by dV,
$$ dU = TdS - PdV$$
and we have come full circle but we now have some fundamental expressions for two very macroscopic quantities, which is very cool and neat.
### Addition/Removal of Variable
    restrictions - you can only combine partial expressions if they are being held to the same constant variable, then normal rules of "unit" cancellations apply. You can also just add variables if you want to, it may be advantageous to do this but is typically avoided as it just introduces new complexities.
$$ \left(\frac{\delta H}{\delta S}\right)_P = \frac{\left(\frac{\delta H}{\delta T}\right)_P }{\left(\frac{\delta S}{\delta T}\right)_P }=T$$

$$\left(\frac{\delta H}{\delta S}\right)_P=\left(\frac{\delta H \delta T}{\delta S \delta T}\right)_P=\left(\frac{\delta H}{\delta T}\right)_P\left(\frac{\delta T}{\delta S}\right)_P $$
### Maxwell's Relations
    restrictions - only for second derivatives
    when - you want thermodynamics problems to be easy
$$ \left(\frac{\delta^2 F}{\delta x \delta y}\right)= \left(\frac{\delta^2 F}{\delta y \delta x}\right)\rightarrow  \left(\frac{\delta A}{\delta x}\right)_y = \left(\frac{\delta B}{\delta y}\right)_x$$
Common Maxwell Relations
$$ \left(\frac{\delta T}{\delta V}\right)_S = -\left(\frac{\delta P}{\delta S}\right)_V =\left(\frac{\delta^2U}{\delta S \delta V}\right) $$
$$ \left(\frac{\delta T}{\delta P}\right)_S = \left(\frac{\delta V}{\delta S}\right)_P =\left(\frac{\delta^2H}{\delta S \delta P}\right) $$
$$ \left(\frac{\delta V}{\delta T}\right)_P = -\left(\frac{\delta S}{\delta P}\right)_T =\left(\frac{\delta^2G}{\delta T \delta P}\right) $$
$$ \left(\frac{\delta P}{\delta T}\right)_V = \left(\frac{\delta S}{\delta V}\right)_T =-\left(\frac{\delta^2A}{\delta T \delta V}\right) $$
There are two other relations but they are not commonly used in introductory thermodynamics.

| Thermodynamic Potential | Symbol | Formula  | Natural Variables | Meaning  |
| ----------------------- | ------ | ------------ | --------- | ------- |
| Internal Energy         | U      | TS - PV | S,V       | capacity to do work plus the capacity to release heat  |
| Enthalpy                | H      | U + PV = TS + PV | S,P  | capacity to do chemical work (i.e. non-mechanical) plus the capacity to release heat |
| Gibbs Free Energy       | G      | U + PV - TS = H -    | T,P | capacity to do chemical work (i.e. non-mechanical)              |
| Helmholtz Free Energy   | A      | U - TS            | T,V       | capacity to do mechanical plus chemical work                   |


