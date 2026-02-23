## Experiment No: 4
INTEGRATOR USING OP-AMP (μA741)
## Aim
To design and simulate an Integrator circuit using μA741 in Proteus Design Suite and verify that the output is proportional to the integral of the input voltage.
## Apparatus Required
•	μA741 Op-Amp
•	Resistor R = 10 kΩ
•	Capacitor Cf = 0.01 µF
•	Signal Generator
•	Dual Power Supply (±15V)
•	CRO / Oscilloscope
•	Connecting wires
## Circuit Diagram

<img width="1308" height="645" alt="image" src="https://github.com/user-attachments/assets/d8ef2714-42f5-407e-9b7d-4cade4bc1d96" />

## Connection Details:
•	Input signal → Resistor (R) → Inverting terminal (Pin 2)
•	Feedback capacitor (Cf) → Between Output (Pin 6) and Pin 2
•	Non-inverting terminal (Pin 3) → Ground
•	Pin 7 → +15V
•	Pin 4 → −15V
## Theory
An Integrator circuit produces an output voltage proportional to the integral of the input voltage.
## Working Principle:
•	When input is constant → output is ramp signal
•	Output is inverted
•	Output depends on time
For Sine Wave Input:
•	Output lags input by 90°
•	Output amplitude decreases with frequency
## Procedure
1.	Open Proteus software.
2.	Select μA741, resistor, capacitor, signal generator, and CRO.
3.	Connect circuit in integrator configuration.
4.	Apply ±15V power supply.
5.	Set input waveform (1V, 1kHz).
6.	Run simulation.
7.	Observe input and output waveforms on CRO.
## Tabulation
```

S.No	Input Signal	        Frequency	   Expected Output	                                     Practical Observation

1	    Sine wave (2 Vpp)	  500 Hz        Cosine wave (lags input by 90°), higher amplitude	     Cosine waveform observed, noticeable phase lag
2	    Sine wave (2 Vpp)	  1 kHz	        Cosine wave, reduced amplitude compared to 500 Hz	     Lower amplitude, clear 90° lag
3       Square wave (2 Vpp)	1 kHz         Triangular wave	                                       Triangular waveform observed
4	    Constant DC input	  -----	        Ramp (linearly increasing/decreasing) output	         Linear ramp observed until saturation
``` 

## Waveforms


<img width="1376" height="1099" alt="image" src="https://github.com/user-attachments/assets/9ea61d4a-6eae-4ff4-923b-59a3c21ef8ec" />
<img width="1376" height="1100" alt="image" src="https://github.com/user-attachments/assets/e43099f5-e528-40ca-a286-6fbe6008d7cc" />
<img width="1370" height="1097" alt="image" src="https://github.com/user-attachments/assets/4f79a182-9076-4dcb-9bf6-e287e91173a7" />

## Result
The Integrator circuit using μA741 Op-Amp was successfully designed and simulated in Proteus.
The output waveform is proportional to the integral of the input signal.
The circuit behaves as an integrator.
## Conclusion
•	Output lags input by 90° (for sine input).
•	Output amplitude decreases with increase in frequency.
•	Used in waveform generation and analog computation.
## Viva Questions
```

1.	What is an integrator circuit?
An Integrator is an op-amp circuit in which the output voltage is proportional to the integral (accumulation) of the input voltage over time.
It uses:
Resistor at the input
Capacitor in the feedback path

2.	Write the output equation of integrator.
Vout​=−(1/RC) (∫Vin​dt)
Where:
𝑅 = Input resistor
𝐶 = Feedback capacitor
∫𝑉𝑖𝑛𝑑𝑡 = Integral of input voltage
The negative sign indicates phase inversion.

3.	Why does output lag input?
For a sinusoidal input:
∫sin⁡(𝜔𝑡)𝑑𝑡 = −(1/𝜔) cos⁡(𝜔𝑡)
Since cosine lags sine by 90°, the output waveform lags the input by 90°.

4.	What happens at very low frequency?
At very low frequency:
Capacitive reactance becomes very high
Gain increases
Output may become very large
Circuit may saturate due to DC components
So, ideal integrator becomes unstable at low frequencies.

5.	What is practical integrator?
A Practical Integrator is a modified integrator circuit that includes a resistor in parallel with the feedback capacitor.
This:
Prevents excessive gain at low frequencies
Avoids output saturation
Improves stability
```
