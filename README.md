# Room Heating Control Blueprint for Home Assistant

This blueprint allows you to manage the heating system of a room with multiple modes: **OFF**, **ELECTRIC**, **GAS**, and **ELECTRIC+GAS**. It works with smart devices such as a smart heater (electric), a smart valve (gas), and a temperature sensor to ensure optimal comfort.

## Features

- **Four Modes of Operation**:
  - **OFF**: Turns off all heating devices and sets the valve to a predefined low temperature.
  - **ELECTRIC**: Controls the electric heater based on the room's temperature and the desired setpoint.
  - **GAS**: Sets the smart valve to the desired temperature while turning off the electric heater.
  - **ELECTRIC+GAS**: Controls both the electric heater and the smart valve simultaneously for maximum efficiency.
  
- **Dynamic Temperature Control**:
  - Automatically turns the electric heater on/off based on the current temperature compared to the desired temperature.
  - Adjusts the smart valve temperature depending on the selected mode.

- **Customizable Inputs**:
  - Select the entities for the mode control buttons, the electric heater, the temperature sensor, and the smart valve.
  - Define the desired temperature for the room.
  - Specify a default temperature for the valve when in **OFF** or **ELECTRIC** mode.

## How It Works

1. **OFF Mode**:
   - Turns off the electric heater.
   - Sets the valve to a predefined low temperature.

2. **ELECTRIC Mode**:
   - Controls the electric heater based on the temperature sensor and the desired setpoint.
   - Sets the valve to a predefined low temperature.

3. **GAS Mode**:
   - Sets the smart valve to the desired room temperature.
   - Turns off the electric heater.

4. **ELECTRIC+GAS Mode**:
   - Controls the electric heater based on the temperature sensor and the desired setpoint.
   - Sets the smart valve to the desired room temperature.

## How to Use

1. Import this blueprint into Home Assistant.
2. Configure the following inputs:
   - Four control buttons (OFF, ELECTRIC, GAS, ELECTRIC+GAS).
   - The electric heater switch.
   - The temperature sensor.
   - The smart valve.
   - Desired room temperature and default valve temperature.
3. Enjoy automated and efficient room heating management!

## Example Use Case

Imagine you want to keep your room at 22°C:
- When the temperature drops below 22°C in **ELECTRIC** or **ELECTRIC+GAS** mode, the heater turns on.
- When the temperature exceeds 22°C, the heater turns off.
- In **GAS** or **ELECTRIC+GAS** mode, the valve adjusts to maintain 22°C.
- Switching to **OFF** ensures all heating is turned off, and the valve sets to a predefined low temperature.

## Compatibility

- Home Assistant Core
- Smart heater (electric) supporting the `switch` domain.
- Smart valve (gas) supporting the `climate` domain.
- Temperature sensor supporting the `sensor` domain.

## Blueprint Code

You can find the YAML code for this blueprint in this repository under [blueprint.yaml](blueprint.yaml).
