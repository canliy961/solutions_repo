# Problem 1
# Pendulum Experiment: Measuring Earth's Gravitational Acceleration

# Experiment: Measuring Acceleration Due to Gravity Using a Phone Charger as a Pendulum

## Objective

To measure the acceleration due to gravity $g$ using a simple pendulum setup made from a phone charger cable and a small object.

---

## Materials Needed

- Phone charger cable (approx. 1 meter or more)  
- Small object as a weight (e.g., metal key, padlock, USB adapter)  
- Ruler or tape measure (1 mm resolution preferred)  
- Smartphone stopwatch or timer  
- Hook, doorknob, or shelf to suspend the pendulum  
- Notebook or notes app to record time  

---

## Procedure

### 1. Setup

- Tie the small object securely to the end of the phone charger.  
- Hang the other end from a fixed support so the object can swing freely.  
- Measure the length $L$ from the suspension point to the center of mass of the object.  
  - Example: $L = 1.02 \ \text{m}$
- Estimate the uncertainty:  
  $$\Delta L = \frac{\text{ruler resolution}}{2} = \frac{0.001}{2} = 0.0005 \ \text{m}$$

---

### 2. Data Collection

- Pull the weight back gently (angle < 15°) and release.  
- Start timing as it swings forward — count **10 complete oscillations**.  
- Repeat this process 10 times, recording each result as $T_{10}$.  

---

## Data Table

| Trial | Time for 10 Oscillations $T_{10}$ (s) |
|-------|----------------------------------------|
| 1     | 19.42                                  |
| 2     | 19.25                                  |
| 3     | 18.78                                  |
| 4     | 18.58                                  |
| 5     | 18.95                                  |
| 6     | 19.50                                  |
| 7     | 19.43                                  |
| 8     | 19.62                                  |
| 9     | 19.93                                  |
| 10    | 19.43                                  |

---

## What You’ll Calculate

### 1. Mean time:
$$\overline{T_{10}} = \frac{1}{10} \sum_{i=1}^{10} T_{10,i} = 19.389 \ \text{s}$$

### 2. Standard deviation:
$$\sigma_T = \sqrt{\frac{1}{n-1} \sum (T_{10,i} - \overline{T_{10}})^2} \approx 0.409 \ \text{s}$$

### 3. Uncertainty in mean time:
$$\Delta T_{10} = \frac{\sigma_T}{\sqrt{n}} = \frac{0.409}{\sqrt{10}} \approx 0.129 \ \text{s}$$

### 4. Period of one oscillation:
$$T = \frac{\overline{T_{10}}}{10} = \frac{19.389}{10} = 1.9389 \ \text{s}$$

### 5. Uncertainty in period:
$$\Delta T = \frac{\Delta T_{10}}{10} = \frac{0.129}{10} = 0.0129 \ \text{s}$$

---

## Calculating $g$

### Formula:
$$g = \frac{4\pi^2 L}{T^2}$$

### Substitution:
$$g = \frac{4\pi^2 \cdot 1.02}{(1.9389)^2} \approx 10.70 \ \text{m/s}^2$$

---

## Uncertainty in $g$

Relative uncertainty:
$$\frac{\Delta g}{g} = \sqrt{\left(\frac{\Delta L}{L} \right)^2 + \left(2 \cdot \frac{\Delta T}{T} \right)^2}$$

Substituting:
$$\frac{\Delta g}{g} = \sqrt{\left(\frac{0.0005}{1.02} \right)^2 + \left(2 \cdot \frac{0.0129}{1.9389} \right)^2} \approx \sqrt{2.4 \times 10^{-7} + 8.9 \times 10^{-5}} \approx 9.5 \times 10^{-3}$$

Absolute uncertainty:
$$\Delta g \approx 10.70 \cdot 0.0095 \approx 0.10 \ \text{m/s}^2$$

---

## Tips for Accuracy

- Use a **video recording** to time oscillations and avoid human reaction error.  
- Measure the string length **from the pivot to the center of mass** of the object.  
- Ensure the charger swings in a **single vertical plane**, not side-to-side.

---

## Final Result (Example)

- Measured gravitational acceleration:  
  $$g = 10.70 \pm 0.10 \ \text{m/s}^2$$

This result is slightly higher than the standard value of $9.81 \ \text{m/s}^2$, likely due to timing or amplitude effects. However, it demonstrates how simple tools can yield reasonably accurate results.

---

## Materials Used
- **String**: 1.00 m  
- **Small weight**: keychain  
- **Stopwatch**: smartphone (resolution = 0.01 s)  
- **Ruler**: resolution = 0.001 m (1 mm)

---

## Procedure

### 1. Measuring Length ($L$)

Measured length from suspension point to center of mass of the weight:

- $L = 1.000 \ \text{m}$  
- Ruler resolution: $0.001 \ \text{m}$  
- Uncertainty in length:  
  $$\Delta L = \frac{0.001}{2} = 0.0005 \ \text{m}$$

---

### 2. Time Measurement: 10 Oscillations

| Trial | Time for 10 Oscillations $T_{10}$ (s) |
|-------|----------------------------------------|
| 1     | 20.12                                  |
| 2     | 20.18                                  |
| 3     | 20.16                                  |
| 4     | 20.11                                  |
| 5     | 20.20                                  |
| 6     | 20.13                                  |
| 7     | 20.14                                  |
| 8     | 20.17                                  |
| 9     | 20.15                                  |
| 10    | 20.16                                  |

---

## Data Summary

- Mean time for 10 oscillations:  
  $$\overline{T_{10}} = 20.152 \ \text{s}$$

- Standard deviation:  
  $$\sigma_T = 0.027 \ \text{s}$$

- Uncertainty in mean time:  
  $$\Delta T_{10} = \frac{0.027}{\sqrt{10}} \approx 0.0085 \ \text{s}$$

![alt text](image.png)

![alt text](image-1.png)

---

## Calculations

### 1. Period and Its Uncertainty

- Period of one oscillation:  
  $$T = \frac{20.152}{10} = 2.0152 \ \text{s}$$

- Uncertainty in period:  
  $$\Delta T = \frac{0.0085}{10} = 0.00085 \ \text{s}$$

---

### 2. Calculating $g$

Using the pendulum formula:  
$$g = \frac{4\pi^2 L}{T^2}$$

Substitute values:  
$$g = \frac{4\pi^2 (1.000)}{(2.0152)^2} \approx 9.719 \ \text{m/s}^2$$

---

### 3. Uncertainty in $g$

Relative uncertainty in $g$:  
$$\frac{\Delta g}{g} = \sqrt{\left(\frac{\Delta L}{L} \right)^2 + \left(2 \cdot \frac{\Delta T}{T} \right)^2}$$

Substitute values:  
$$\frac{\Delta g}{g} = \sqrt{\left(\frac{0.0005}{1.000} \right)^2 + \left(2 \cdot \frac{0.00085}{2.0152} \right)^2}$$

$$\frac{\Delta g}{g} \approx \sqrt{2.5 \times 10^{-7} + 7.1 \times 10^{-7}} \approx 9.6 \times 10^{-7}$$

- Absolute uncertainty in $g$:  
  $$\Delta g \approx 0.00098 \cdot 9.719 \approx 0.0095 \ \text{m/s}^2$$

![alt text](image-4.png)

---

## Final Results

| Quantity                  | Value                |
|--------------------------|----------------------|
| Length $L$               | $1.000 \ \text{m}$   |
| Uncertainty $\Delta L$   | $0.0005 \ \text{m}$  |
| Mean $T_{10}$            | $20.152 \ \text{s}$  |
| Std Dev $\sigma_T$       | $0.027 \ \text{s}$   |
| Uncertainty $\Delta T_{10}$ | $0.0085 \ \text{s}$ |
| Period $T$               | $2.0152 \ \text{s}$  |
| Uncertainty $\Delta T$   | $0.00085 \ \text{s}$ |
| Calculated $g$           | $9.719 \ \text{m/s}^2$ |
| Uncertainty $\Delta g$   | $\pm 0.010 \ \text{m/s}^2$ |

---

## Discussion

### 1. Comparison with Standard $g = 9.81 \ \text{m/s}^2$

- Measured value: $g = 9.719 \pm 0.010 \ \text{m/s}^2$  
- Difference: $9.81 - 9.719 = 0.091 \ \text{m/s}^2$  
- Percentage error:  
  $$\frac{0.091}{9.81} \times 100\% \approx 0.93\%$$

The result is within 0.9% of the standard value — reasonably accurate.

### 2. Uncertainty Sources and Impact

- **Length Measurement ($\Delta L$)**: Very small due to high ruler resolution — negligible effect.  
- **Timing Uncertainty ($\Delta T$)**: Main contributor to error. Human reaction time (~0.1s) is reduced by averaging over 10 oscillations.

**Assumptions:**

- Small-angle approximation (<15°) holds.  
- No air resistance or friction considered.  
- Mass of the string is negligible.

![alt text](image-3.png)

---

## Conclusion

This experiment effectively measures the gravitational acceleration with decent accuracy. The dominant uncertainty arises from timing, reinforcing the importance of reducing human error through averaging and repeat trials.

## My Colab (Canliy961)

[Measurements](https://colab.research.google.com/drive/1tXh7-1Dlv1jVkg5xT4q6p5ik7yRYPwdB#scrollTo=PEimH_Hpqt-Z)
