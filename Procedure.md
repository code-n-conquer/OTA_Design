# OTA Design Procedure

## Step 1: DC Analysis

DC analysis is carried out with appropriate voltage and current parameters to determine the threshold voltage (Vth) and the current gain (β) of the PMOS and NMOS transistors used in the circuit.

## Step 2: Parameter Approximation

The parameters are approximated to values that simplify the calculation process:
- **μpCox**: 165 µA/V²
- **μnCox**: 330 µA/V²
- **Vth**: 0.2 V (for both PMOS and NMOS)

<img width="749" alt="Parameter_Cal" src="https://github.com/user-attachments/assets/20ec0a20-c209-42c7-8249-1072c18e17bf">\
Circuit for Paramter Calculation

<img width="169" alt="Pcal2" src="https://github.com/user-attachments/assets/52f382fc-4c8a-42b0-aa9a-c520f3c603f4">\
beta effective for pmos

<img width="106" alt="Pcal3" src="https://github.com/user-attachments/assets/0fdcbbfc-0368-4477-8280-df53a24b80ee">\
vth for pmos

<img width="265" alt="Pcal4" src="https://github.com/user-attachments/assets/5304414c-4f96-4602-8d93-2274a5652862">\
beta effective for nmos

<img width="104" alt="Pcal5" src="https://github.com/user-attachments/assets/c44ecc29-50fb-4ac1-8fba-d15651d89bfd">\
vth for nmos

## Step 3: Deciding the DC Current

The DC current for the amplifier is determined based on two constraints:
- **Lower Limit**: Determined by the Slew Rate.
- **Upper Limit**: Determined by Power Dissipation (P<sub>diss</sub> = V<sub>dd</sub> * I<sub>d</sub>).

A current of **50 µA** is chosen as it satisfies both constraints.

## Step 4: PMOS Current Mirror Sizing

The width-to-length ratio (W/L) for the PMOS current mirror is selected based on the ICMR+ constraint.

## Step 5: NMOS Transconductance Selection

The transconductance (g<sub>m</sub>) for the NMOS transistor is chosen based on the Unity Gain Frequency (UGF) constraint. The W/L ratio for the NMOS is then calculated using the values of g<sub>m</sub> and I<sub>d</sub>.

## Step 6: NMOS Current Mirror Sizing

The W/L ratio for the NMOS current mirror is determined based on the ICMR- constraint.

## Final W/L Ratios

The finalized W/L ratios are as follows:
- **W/L (PMOS current mirror)**: 15
- **W/L (NMOS current mirror)**: 2
- **W/L (NMOS input pair)**: 10

With these ratios, the DC analysis is performed.

![DC_Analysis_ICMR-](https://github.com/user-attachments/assets/c9316f60-4d74-475b-82e6-0857be49c158)
DC analysis carried out at ICMR- = 0.8V

![DC_Analysis_ICMR+](https://github.com/user-attachments/assets/0c64967e-66cd-4b33-b59a-1b69af92d123)
DC analysis carried out at ICMR- = 1.6V

All transistors are in saturation in both the edge cases.

## Initial AC Analysis

An AC analysis is performed with a frequency sweep ranging from **1 Hz to 10 MHz**.

<img width="854" alt="AC_Plot4" src="https://github.com/user-attachments/assets/9ca8fc89-846b-4a1f-b9d7-62265126143d">\
AC analysis carried out at ICMR- = 0.8V, Gain ~= 32dB

<img width="852" alt="AC_Plot3" src="https://github.com/user-attachments/assets/78a5aed4-45a2-41db-b538-0729926aa507">\
AC analysis carried out at ICMR- = 1.6V, Gain ~= 30.8dB

## Optimization and Conclusion

There is no upper limit for UGF. Hence, increasing the transconductance (g<sub>m</sub>) by adjusting the W/L ratio for the input NMOS pair can be adopted to increase gain of the transistor. For w/l = 20, gain is found to be maximum while all the transistors are maintained in saturation. Further, increasing w/l, pushes the transistors out of saturation. 

## Final AC Analysis

Again, AC analysis is performed with a frequency sweep ranging from **1 Hz to 10 MHz**.

![AC_Plot_Gain_ICMR-](https://github.com/user-attachments/assets/3ee44615-cb17-48ac-9d57-a17151fd4898)

![AC_Plot_ICMR-](https://github.com/user-attachments/assets/b6a360c3-018e-44d1-bda8-b2e564168523)
AC analysis carried out at ICMR- = 0.8V, Gain ~= 38dB

![AC_Plot_Gain_ICMR+](https://github.com/user-attachments/assets/daa4d7c1-7283-4c2a-8bee-b70227808412)

![AC_Plot_ICMR+](https://github.com/user-attachments/assets/5d2b4ac4-eacc-412c-991a-6f5bd3a75c53)
AC analysis carried out at ICMR+ = 1.6V, Gain ~= 37dB

This gives almost 2dB more gain than the previous configurations. So, this is chosen as the final configuration.

**Conclusion**: The desired gain of **70 V/V** is not achieved with this amplifier design. However, a gain of **40 V/V** is realized while meeting the other design parameters.
