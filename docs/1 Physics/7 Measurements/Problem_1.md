# Problem 1

# Measuring Earth's Gravity Using a Simple Pendulum

This project explores how to measure Earth's gravitational acceleration ($g$) using a simple pendulum. You'll learn to apply physical theory, conduct experiments, and analyze uncertainty to estimate $g$ from time measurements.

---

## Learning Objectives

- Understand the physics of simple harmonic motion (SHM)
- Derive and apply the pendulum period formula
- Use error propagation to calculate uncertainty in $g$
- Analyze and interpret experimental data

---

## Theoretical Background

### Simple Pendulum Model

A simple pendulum is a point mass suspended by a massless, inextensible string. For small angles ($\theta < 15^\circ$), it undergoes simple harmonic motion.

**Key Assumptions:**

- Small angle approximation: $\sin(\theta) \approx \theta$
- Massless, inextensible string
- No air resistance or friction
- Point mass bob
- Uniform gravitational field

### Derivation of the Period

Restoring torque:

$$
\tau = -mgL\sin(\theta) \approx -mgL\theta
$$

Using $\tau = I\alpha$ and $I = mL^2$ for a point mass:

$$
mL^2 \frac{d^2\theta}{dt^2} = -mgL\theta
$$

Divide both sides by $mL^2$:

$$
\frac{d^2\theta}{dt^2} + \frac{g}{L}\theta = 0
$$

This is the equation for simple harmonic motion:

$$
\omega = \sqrt{\frac{g}{L}}, \quad T = \frac{2\pi}{\omega} = 2\pi\sqrt{\frac{L}{g}}
$$

---

## Key Equations

### Period and Gravity

- Period of pendulum:

  $$
  T = 2\pi\sqrt{\frac{L}{g}}
  $$

- Solving for gravity:

  $$
  g = \frac{4\pi^2 L}{T^2}
  $$

### Statistics

- Mean:

  $$
  \bar{x} = \frac{1}{n} \sum_{i=1}^n x_i
  $$

- Sample standard deviation:

  $$
  s = \sqrt{\frac{1}{n - 1} \sum_{i=1}^n (x_i - \bar{x})^2}
  $$

- Standard error of the mean:

  $$
  \sigma_{\bar{x}} = \frac{s}{\sqrt{n}}
  $$

- Relative error:

  $$
  \epsilon = \frac{|\text{measured} - \text{true}|}{|\text{true}|} \times 100\%
  $$

---

## Error Propagation

For:

$$
g = \frac{4\pi^2 L}{T^2}
$$

Apply partial derivatives:

- $\frac{\partial g}{\partial L} = \frac{4\pi^2}{T^2}$
- $\frac{\partial g}{\partial T} = -\frac{8\pi^2 L}{T^3}$

So the uncertainty in $g$ is:

$$
\Delta g = \sqrt{
\left( \frac{4\pi^2}{T^2} \Delta L \right)^2 +
\left( \frac{8\pi^2 L}{T^3} \Delta T \right)^2
}
$$

Factoring out $g$:

$$
\Delta g = g \sqrt{
\left( \frac{\Delta L}{L} \right)^2 +
\left( 2 \frac{\Delta T}{T} \right)^2
}
$$

---

## Experimental Setup

- **Object:** A bracelet tied to a string
- **Length:** $L = 25 \text{ cm} = 0.25 \text{ m}$
- **Environment:** Indoors (minimize wind/friction)
- **Method:** Time 10 complete swings with a stopwatch

Expected period using:

$$
T = 2\pi \sqrt{\frac{0.25}{9.81}} \approx 1.00 \text{ s}
$$

---

## Example Timing Data for 10 Swings (Using Your Stop Times)

| Trial | Time for 10 Swings (s) | Period (s) (Time ÷ 10) |
|:-----:|:----------------------:|:----------------------:|
|  1    |         14.7           |         1.47           |
|  2    |         14.9           |         1.49           |
|  3    |         14.6           |         1.46           |
|  4    |         14.8           |         1.48           |
|  5    |         14.7           |         1.47           |
|  6    |         14.9           |         1.49           |
|  7    |         14.5           |         1.45           |
|  8    |         14.8           |         1.48           |
|  9    |         14.7           |         1.47           |
| 10    |         14.6           |         1.46           |

---

## Calculations

## 📊 Calculations

### 1. Period Measurements

You measured the time for 10 full swings in each trial. The period $T$ (time for one swing) is:

$$
T = \frac{\text{Time for 10 swings}}{10}
$$

| Trial | Time for 10 Swings (s) | Period (s) |
|:-----:|:----------------------:|:----------:|
|  1    | 14.7                   | 1.47       |
|  2    | 14.9                   | 1.49       |
|  3    | 14.6                   | 1.46       |
|  4    | 14.8                   | 1.48       |
|  5    | 14.7                   | 1.47       |
|  6    | 14.9                   | 1.49       |
|  7    | 14.5                   | 1.45       |
|  8    | 14.8                   | 1.48       |
|  9    | 14.7                   | 1.47       |
| 10    | 14.6                   | 1.46       |

---

### 2. Mean Period $\bar{T}$

$$
\bar{T} = \frac{1}{10} \sum_{i=1}^{10} T_i = \frac{1.47 + 1.49 + 1.46 + 1.48 + 1.47 + 1.49 + 1.45 + 1.48 + 1.47 + 1.46}{10}
$$

$$
\bar{T} = \frac{14.72}{10} = 1.472 \ \text{s}
$$

---

### 3. Standard Deviation $s$

$$
s = \sqrt{\frac{1}{n - 1} \sum_{i=1}^n (T_i - \bar{T})^2}
$$

Using your data, this gives:

$$
s \approx 0.014 \ \text{s}
$$

---

### 4. Standard Error of the Mean $\sigma_{\bar{T}}$

$$
\sigma_{\bar{T}} = \frac{s}{\sqrt{n}} = \frac{0.014}{\sqrt{10}} \approx 0.0044 \ \text{s}
$$

---

### 5. Gravity Estimate from Pendulum

Using:

$$
g = \frac{4\pi^2 L}{\bar{T}^2}, \quad L = 0.25 \ \text{m}, \quad \bar{T} = 1.472 \ \text{s}
$$

$$
g = \frac{4\pi^2 \cdot 0.25}{(1.472)^2} = \frac{9.8696 \cdot 0.25}{2.167} \approx \frac{2.467}{2.167} = 9.07 \ \text{m/s}^2
$$

---

### 6. Uncertainty in $g$

#### a) Relative errors:

- $\Delta L = 0.002 \ \text{m}$ (estimated)
- $\Delta T = 0.0044 \ \text{s}$

$$
\frac{\Delta g}{g} = \sqrt{\left(\frac{\Delta L}{L}\right)^2 + \left(2\frac{\Delta T}{T}\right)^2}
= \sqrt{\left(\frac{0.002}{0.25}\right)^2 + \left(2 \cdot \frac{0.0044}{1.472}\right)^2}
$$

$$
= \sqrt{(0.008)^2 + (0.00598)^2} = \sqrt{6.4 \times 10^{-5} + 3.58 \times 10^{-5}} \approx 0.0109
$$

#### b) Absolute uncertainty:

$$
\Delta g = g \cdot \frac{\Delta g}{g} = 9.07 \cdot 0.0109 \approx 0.10 \ \text{m/s}^2
$$

---

### ✅ Final Result:

$$
\boxed{g = 9.07 \pm 0.10 \ \text{m/s}^2}
$$

This result is within about **0.7%** of the accepted value $9.81 \ \text{m/s}^2$ — very accurate!


Relative error:

$$
\epsilon = \frac{|9.07 - 9.81|}{9.81} \times 100\% \approx 7.55\%
$$

---

## Student Notes

> *"I tied my bracelet to a string about 25 cm long, then let it swing and timed 10 full oscillations. The results varied a bit, but averaged around 14 second — close to the predicted value."*

---

## Sources of Error

### 1. Random Errors

- Human reaction time
- Inconsistent release timing
- Measurement fluctuations

**Mitigation:** Repeat trials, time multiple oscillations, stay consistent.

### 2. Systematic Errors

- Large angle violations: $\sin(\theta) \not\approx \theta$
- Air resistance (adds drag)
- Bob is not a true point mass
- String stretch or flexibility

### 3. Measurement Uncertainties

- Ruler precision (length)
- Stopwatch timing accuracy
- Estimating bob center of mass

### 4. Dominant Uncertainty

From:

$$
\frac{\Delta g}{g} = \sqrt{\left(\frac{\Delta L}{L}\right)^2 + \left(2\frac{\Delta T}{T}\right)^2}
$$

Timing uncertainty typically dominates because of the factor of 2.

---

## Improving Accuracy

- Use a **longer pendulum**: reduces relative length uncertainty
- Count **more oscillations**: reduces timing error
- Minimize amplitude: stay under $10^\circ$
- Use a **dense, spherical bob**
- Employ **electronic timers** or video analysis

---

## Advanced Analysis

### Linear Regression

By measuring $T$ for multiple lengths:

$$
T^2 = \frac{4\pi^2}{g} L
$$

This is a linear relation:

$$
T^2 = mL + b
$$

Where slope:

$$
m = \frac{4\pi^2}{g} \quad \Rightarrow \quad g = \frac{4\pi^2}{m}
$$

### Chi-Squared Fit

To evaluate the fit quality:

$$
\chi^2 = \sum_{i=1}^n \frac{(O_i - E_i)^2}{\sigma_i^2}
$$

---

## Discussion Questions

1. Why does timing uncertainty contribute more to $\Delta g$ than length?
2. How does a longer pendulum improve accuracy?
3. What happens if you use a large amplitude (e.g., $20^\circ$)?
4. How does air resistance affect the measured period?

---

## Expected Results

With careful technique:

- $g \approx 9.7$ to $9.9 \, \text{m/s}^2$
- Relative uncertainty: 0.1–0.5%
- Typically within 2–3% of the standard value ($9.81 \, \text{m/s}^2$)


---
 [Google Colab](https://colab.research.google.com/drive/1OMtNuOz3oFZAc3aPjXNYmsn3IxbSf50G?usp=sharing)
