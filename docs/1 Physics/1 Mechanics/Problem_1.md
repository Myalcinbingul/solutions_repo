# Problem 1
# 📌 Investigating the Range as a Function of the Angle of Projection  

## 🔹 1. Theoretical Foundation  

Projectile motion follows basic kinematic equations. Assuming no air resistance, the equations for motion are:  

### **Equations of Motion**
The horizontal and vertical positions as functions of time:

\[
x(t) = v_0 \cos(\theta) t
\]

\[
y(t) = v_0 \sin(\theta) t - \frac{1}{2} g t^2
\]

where:  
- \( v_0 \) = initial velocity  
- \( \theta \) = launch angle  
- \( g \) = gravitational acceleration  

### **Time of Flight**
The total flight time until the projectile hits the ground:

\[
t_f = \frac{2 v_0 \sin(\theta)}{g}
\]

### **Range Equation**
The range \( R \), or horizontal distance, is given by:

\[
R = \frac{v_0^2 \sin(2\theta)}{g}
\]

## 🔹 2. Analysis of Range  

### **Dependence on Angle**
- The function \( \sin(2\theta) \) dictates that the **maximum range** occurs at **\( \theta = 45^\circ \)**.
- The range is **symmetric** about \( 45^\circ \), meaning \( R(30^\circ) = R(60^\circ) \).

### **Dependence on Initial Velocity**
- Since \( R \propto v_0^2 \), increasing velocity **quadratically increases** range.

### **Dependence on Gravity**
- Higher gravity (\( g \)) **reduces** the range.

## 🔹 3. Practical Applications  

- **Sports**: Optimizing kick angles in football.
- **Engineering**: Calculating projectile paths in robotics.
- **Astronomy**: Estimating trajectories of celestial bodies.

## 🔹 4. Graphical Representation (Without Code)  

To visualize the relationship between \( R \) and \( \theta \), you can plot:

\[
R(\theta) = \frac{v_0^2}{g} \sin(2\theta)
\]

for \( 0^\circ \leq \theta \leq 90^\circ \).  

Using a tool like **Desmos** or **GeoGebra**, you can manually input the equation and see how range varies with angle.

---



