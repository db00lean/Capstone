The Inductor/Switching Frequency simulations are designed as follows:

Input: 5V
Output: 60V

Switching Frequencies of 200KHz to 700KHz in 100KHz intervals will be tested by changing the value
of the resistor on the Rt pin. The inductor will remain constant for each set of frequency tests.

A higher switching frequency should allow smaller inductor/capacitor values at the cost of increased switching losses and gate driving current.

A lower switching frequency should give better performance at the cost of large component sizes.

Required Plots:

-Output Voltage: Larger inductor values arise from lower switching frequencies, but have a direct effect on the ripple current.

-Gate Currents: Higher Switching frequencies will create larger gate driving currents, so each plots needs to show the gate currents of each of the four Power MOSFETs. These need to be tested and ensured that they're below the maximum specification of the FETs we purchased.





