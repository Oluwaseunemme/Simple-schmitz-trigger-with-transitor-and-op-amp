# Schmitt Trigger (NPN Transistor + Op-Amp) — Proteus
What is a Schmitt Trigger?
A Schmitt Trigger is a comparator circuit with hysteresis.
It has two different switching thresholds:

Rising threshold (
𝑉
𝑇
𝐻
+
V 
TH+
​
 ): when input goes LOW → HIGH
Falling threshold (
𝑉
𝑇
𝐻
−
V 
TH−
​
 ): when input goes HIGH → LOW
Because the thresholds are different, the output is less sensitive to noise near the switching point (reduced output “chattering”).

Circuit 1: NPN Transistor Schmitt Trigger (Q1, Q2)
The two NPN transistors are arranged with resistors so that the current conduction state feeds back to the input biasing network.
When Vin starts to rise, one transistor turns on first and shifts the effective switching level.
When Vin falls, the switching happens again only after Vin crosses a different level.
✅ Result: output switches at different Vin values depending on rising vs falling input.

Circuit 2: Op-Amp Schmitt Trigger (LM358 + Resistor Feedback)
The LM358 is used like a comparator (high gain, saturating output).
Resistors provide positive feedback, so the reference level seen by the op-amp input changes with the output state.
Therefore:
Output changes to HIGH at one threshold
Output changes to LOW at another threshold
✅ Result: hysteresis is created by feedback.

How to verify in Proteus
Apply a slow triangle/sine/ramp to Vin.
View Vin and Vout.
Confirm hysteresis: Vout should switch at different Vin values for rising vs falling.
Files
Proteus schematic(s) for:

Transistor-based Schmitt Trigger
LM358-based Schmitt Trigger
