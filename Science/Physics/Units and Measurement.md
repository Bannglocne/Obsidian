# The Scope and Scale of Physics
The **order of magnitude** of a number is the power of 10 that most closely approximates it. Thus, the order of magnitude refers to the scale (or size) of a value. An equivalent but quicker way to find the order of magnitude of a number is first to write it in scientific notation and then check to see whether the first factor is greater than or less than $\sqrt{10}$ ≈3

==Building Models==: 
- A **model** is a representation of something that is often too difficult (or impossible) to display directly
- A **theory** is a testable explanation for patterns in nature supported by scientific evidence and verified multiple times by various groups of researchers.
- A **law** uses concise language to describe a generalized pattern in nature supported by scientific evidence and repeated experiments.

---
# Units and Standards
- A **physical quantity** either by specifying how it is measured or by stating how it is calculated from other measurements.

> [!NOTE] **Units** are standardized values. (SI units, English units, SAE units)
> In any system of units, the units for some physical quantities must be defined through a measurement process. These are called the **base quantities** for that system and their units are the **system’s base units**. All other physical quantities can then be expressed as algebraic combinations of the base quantities. Each of these physical quantities is then known as a **derived quantity** and each unit is called a **derived unit**.

| ISQ Base Quantity         | SI Base Unit  |
| ------------------------- | ------------- |
| Length                    | meter (m)     |
| Mass                      | kilogram (kg) |
| Time                      | second (s)    |
| Electrical current        | ampere (A)    |
| Thermodynamic temperature | kelvin (K)    |
| Amount of substance       | mole (mol)    |
| Luminous intensity       | candela (cd)  | 

| Prefix | Symbol | Meaning |
| ------ | ------ | ------- |
| yotta- | Y      | 10^24   |
| zetta- | Z      | 10^21   |
| exa-   | E      | 10^18   |
| peta-  | P      | 10^15   |
| tera-  | T      | 10^12   |
| giga-  | G      | 10^9    |
| mega-  | M      | 10^6    |
| kilo-  | k      | 10^3    |
| hecto- | h      | 10^2    |
| deka-  | da     | 10^1    |
| deci-  | d      | 10^-1   |
| centi- | c      | 10^-2   |
| milli- | m      | 10^-3   |
| micro- | µ      | 10^-6   |
| nano-  | n      | 10^-9   |
| pico-  | p      | 10^-12  |
| femto- | f      | 10^-15  |
| atto-  | a      | 10^-18  |
| zepto- | z      | 10^-21  |
| yocto- | y      | 10^-24  | 

The only rule when using metric prefixes is that you can not “double them up.”

---
# Dimensional Analysis
The **dimension** of any physical quantity expresses its dependence on the base quantities as a product of symbols (or powers of symbols) representing the base quantities: $L^a M^b T^c I^d \Theta^e N^f J^g$

| Symbol for Dimension | Base Quantity       |     
| -------------------- | ------------------- | 
| L                    | Length              |     
| M                    | Mass                |     
| T                    | Time                |     
| I                    | Electric current    |     
| $\Theta$             | Temperature         |     
| N                    | Amount of substance |     
| J                    | Luminous intensity  |     

Equation must obey the following rules:
1. Every term in an expression must have the same dimensions
2. The arguments of any of the standard mathematical functions such as trigonometric functions (such as sine and cosine), logarithms, or exponential functions that appear in the equation must be dimension less. These functions require pure numbers as inputs and give pure numbers as outputs.


> [!NOTE] Physicists often use square brackets around the symbol for a physical quantity to represent the dimensions of that quantity
> [r] = L; [h] = L; [A] = $L^2$; [V] = $L^3$; [m] = M; [$\rho$] = M$L^3$

---
# Significant Figures
**Accuracy** is how close a measurement is to the accepted reference value for that measurement.

The **precision** of measurements refers to how close the agreement is between repeated independent measurements (which are repeated under the same conditions).

The precision of a measuring system is related to the **uncertainty** in the measurements whereas the accuracy is related to the **discrepancy** from the accepted reference value.

=> $\text{Percent uncertainty} = \frac{\delta A}{A} \times 100\%$

1. **Method of adding percents**: The percent uncertainty in a quantity calculated by multiplication or division is the sum of the percent uncertainties in the items used to make the calculation
2. **Method of significant figures**: The last digit written down in a measurement is the first digit with some uncertainty.
3. When combining measurements with different degrees of precision, the number of significant digits in the final answer can be no greater than the number of significant digits in the least-precise measured value.
	- For multiplication and division, the result should have the same number of significant figures as the quantity with the least number of significant figures entering into the calculation.
	- For addition and subtraction, the answer can contain no more decimal places than the least-precise measurement