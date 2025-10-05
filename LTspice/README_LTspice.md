# LTspice Simulation Notes

This directory contains the LTspice schematic, netlist, and simulation plots for the 12V → 3.3V asynchronous buck converter.

### Simulation Steps
1. Open `async_buck_12V_3V3.asc` in LTspice.
2. Run the `.tran 5m` analysis.
3. Probe:
   - `V(out)` → Output voltage ripple.
   - `I(L1)` → Inductor current.
   - `I(Vin)` → Input current.
4. Compare results against theoretical design equations in `/Docs/Design_Equations.pdf`.

### Notes
- Version tested: LTspice 24.0.12  
- Ideal voltage source + pulse generator used for gate drive.  
- Frequency: 150 kHz, Duty ≈ 27.5%.  
