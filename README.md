**Overview**

This repository contains a Pulse Width Modulation (PWM) Generator implemented in Verilog, along with a Testbench to verify its functionality. The design allows control of the duty cycle using 4 switches, with selectable duty cycles of 0%, 20%, 40%, 60%, and 80%.

**Features**

Generates PWM signal with variable duty cycle.
Uses a 50MHz clock for operation.
Provides switch-based duty cycle control.
Implements a 4-bit counter for timing.
Includes Testbench for simulation.

**File Structure**

├── pwm.v         # Verilog code for PWM Generator
├── pwm_tb.v      # Testbench for PWM module
├── README.md     # Project Documentation

**Module Descriptions**

1. PWM Module (pwm.v)

Generates a PWM signal with a duty cycle controlled by inc[3:0].
Uses a 4-bit counter (0-9) to set the PWM cycle.
Supports duty cycles: 0%, 20%, 40%, 60%, 80%.
Includes a reset signal to initialize the system.

Inputs:

clk  → 50MHz Clock input.
rst  → Reset signal.
inc  → 4-bit input for duty cycle control.

Output:

pwm_out  → PWM signal output.


2. Testbench (pwm_tb.v)

Simulates the PWM module.
Generates a 50MHz clock.
Tests different duty cycle values.
Observes PWM signal transitions.

Test Sequence:

Reset system.
Apply different duty cycle settings (20%, 40%, 60%, 80%).
Verify PWM output.

**Future Enhancements**

Add duty cycle percentage display.
Implement frequency control.
Support dynamic duty cycle adjustments.
