# Wiring Diagram and Electrical Integration

## Overview

This document provides wiring diagrams and electrical integration instructions for the 1992 Ford Escort EV conversion using Nissan Leaf components. The electrical system is divided into two main voltage domains:

- **High-Voltage System**: 360V DC (battery to motor)
- **Low-Voltage System**: 12V DC (accessories and controls)

⚠️ **DANGER**: High-voltage systems can be lethal. Always follow safety procedures and use proper protective equipment.

## System Architecture

```
[Battery Pack 360V] 
       |
       +--[Main Fuse]--[Service Disconnect]--+
                                               |
                                               +--[Pre-charge Circuit]
                                               |
                                               +--[Main Contactor]--+
                                                                    |
                         +------------------------------------------+
                         |                                          |
                    [On-Board Charger]                      [Inverter/PDM]
                         |                                          |
                    [J1772 Port]                               [Motor EM57]
                                                                   |
       +--[DC-DC Converter]--[12V Battery]--[12V Accessories]     |
       |                                                           |
       +-----------------------------------------------------------+
           (Connected to HV+ line from main contactor)
```

## High-Voltage System Wiring

### Main High-Voltage Circuit

#### Component Connection Sequence

1. **Battery Pack (+)** 
   - Connection: Positive terminal of battery pack
   - Cable: 2/0 AWG or larger, orange insulation
   
2. **Main Fuse** (300A DC-rated)
   - Location: Near battery pack
   - Purpose: Overcurrent protection
   
3. **Service Disconnect**
   - Type: Manual disconnect switch
   - Location: Accessible location (under hood or trunk)
   - Position: Normally closed during operation
   
4. **Pre-charge Circuit**
   - Components: 
     - Pre-charge resistor (500Ω, 50W)
     - Pre-charge contactor (normally open)
   - Purpose: Gradually charges controller capacitors
   - Operation: Closes 2-5 seconds before main contactor

5. **Main Contactor**
   - Rating: 400V DC, 300A continuous
   - Control: 12V coil from vehicle ignition
   - Purpose: Primary HV switching

6. **Power Distribution Module (PDM)**
   - Input: 360V DC from battery
   - Output: 3-phase AC to motor
   - Additional: Feeds DC-DC converter and OBC

### High-Voltage Cable Specifications

| Connection | Cable Type | Length | Notes |
|------------|-----------|--------|-------|
| Battery (+) to Main Fuse | 2/0 AWG | 2-4 ft | Orange insulation |
| Main Fuse to Service Disconnect | 2/0 AWG | 3-5 ft | Orange insulation |
| Service Disconnect to Contactor | 2/0 AWG | 4-6 ft | Orange insulation |
| Contactor to PDM | 2/0 AWG | 5-10 ft | Orange insulation |
| PDM to Motor (3-phase) | 2/0 AWG (3 cables) | 3-6 ft | From Leaf harness |
| Battery (-) to Chassis | 2/0 AWG | 2-4 ft | Return path |

### High-Voltage Safety Interlocks

```
[HV Panel 1]--[Interlock Switch 1]--+
                                      |
[HV Panel 2]--[Interlock Switch 2]--+--[Interlock Loop]--[PDM Enable]
                                      |
[Service Plug]--[Interlock Switch 3]-+
```

**Interlock Loop Operation**:
- All switches in series
- Any panel removal or service plug disconnection opens loop
- Open loop disables high-voltage system
- Use normally-closed micro switches

### Motor Inverter/Controller (PDM) Connections

**Note**: PDM (Power Distribution Module) refers to the Nissan Leaf's motor controller/inverter unit.

### PDM Input/Output Table

| Terminal | Function | Connection | Wire Size |
|----------|----------|------------|-----------|
| HV+ | High voltage positive | Main contactor output | 2/0 AWG |
| HV- | High voltage negative | Battery negative | 2/0 AWG |
| U, V, W | Motor phases | Motor windings | 2/0 AWG (3x) |
| +12V | Control power | 12V battery | 14 AWG |
| GND | Control ground | Chassis ground | 14 AWG |
| ENABLE | Enable signal | Ignition switch (through BMS) | 18 AWG |
| THROTTLE+ | Throttle sensor power | 5V output | 22 AWG |
| THROTTLE- | Throttle sensor ground | Ground | 22 AWG |
| THROTTLE_SIG | Throttle signal | Accelerator position sensor | 22 AWG |
| BRAKE | Brake signal | Brake light switch | 20 AWG |
| GEAR_POS | Gear position (optional) | Shifter sensor | 20 AWG |
| CAN_H | CAN bus high | BMS CAN high | 24 AWG shielded |
| CAN_L | CAN bus low | BMS CAN low | 24 AWG shielded |

### Throttle Position Sensor Wiring

```
[Throttle Position Sensor]
    Pin 1: +5V (from PDM)
    Pin 2: Signal (0-5V to PDM)
    Pin 3: Ground (to PDM)

Accelerator Pedal Position:
    0% (idle) = 0.5V
    100% (full) = 4.5V
```

**Installation**:
1. Mount sensor on accelerator pedal
2. Use shielded 3-conductor cable
3. Route away from HV cables
4. Calibrate using PDM settings

## Low-Voltage (12V) System

### DC-DC Converter Connections

```
[DC-DC Converter]
    HV Input+ ---> Main HV+ (from contactor)
    HV Input- ---> Main HV-
    12V Output+ ---> 12V Battery (+) and alternator wire
    12V Output- ---> Chassis ground
    Enable ---> Ignition on signal
```

**Specifications**:
- Input: 360V DC nominal (250-403V range)
- Output: 14.4V DC (regulated)
- Current: 100A continuous
- Replaces alternator function

### 12V Battery Location
- Keep original 12V battery
- Powers accessories when HV system is off
- Charged by DC-DC converter during operation

### Ignition and Control Wiring

```
[Ignition Switch]
    OFF position: All systems off
    ACC position: 12V accessories only
    ON position: PDM enabled, ready to drive
    START position: Not used (no starter motor)
```

**Control Circuit**:
```
[Ignition Switch ON] 
    |
    +--[BMS OK Signal]--AND--[Main Contactor Coil]
    |
    +--[PDM Enable Input]
    |
    +--[DC-DC Converter Enable]
```

### Brake Light Switch Integration

```
[Brake Pedal Switch]
    Output 1: Brake lights (existing circuit)
    Output 2: PDM brake input (for regenerative braking)
```

**Function**:
- Brake press activates regenerative braking
- Regen strength adjustable in PDM settings
- Brake lights activate during regen

## Battery Management System (BMS) Wiring

### BMS Module Connections

Each battery module requires:
- Voltage sense wires (2 per module)
- Temperature sensor (thermistor)
- Balancing wires (if active balancing)

```
[BMS Controller]
    Module 1-48: Voltage sense (ribbon cable or individual wires)
    Temperature 1-12: Thermistor inputs (4 modules per sensor)
    CAN_H/L: Communication to PDM
    +12V: Power supply
    GND: Ground
    ENABLE_OUT: To main contactor coil (via ignition)
```

### BMS Safety Features

| Condition | BMS Action | Result |
|-----------|------------|---------|
| Cell over-voltage (>4.2V) | Open ENABLE_OUT | Contactor opens, HV disconnected |
| Cell under-voltage (<2.8V) | Open ENABLE_OUT | Contactor opens, HV disconnected |
| Over-temperature (>60°C) | Open ENABLE_OUT | Contactor opens, HV disconnected |
| Cell imbalance (>100mV) | Warning light | Continue operation, check needed |
| Communication loss | Open ENABLE_OUT | Safe shutdown |

## Charging System Wiring

### J1772 Port Connections

```
[J1772 Inlet]
    Pin 1 (L1): AC Line ---> OBC AC Input
    Pin 2 (L2): AC Neutral ---> OBC AC Neutral  
    Pin 3 (Ground): Earth Ground ---> Chassis
    Pin 4 (Pilot): Control Signal ---> OBC Control
    Pin 5 (Proximity): Proximity detect ---> OBC
```

### On-Board Charger (OBC) Wiring

```
[On-Board Charger]
    AC Input (L1/L2): From J1772 port
    AC Ground: Chassis ground
    DC Output (+): Battery pack positive (through contactor)
    DC Output (-): Battery pack negative
    CAN_H/L: Communication with BMS
    +12V: Control power
    Pilot Signal: From J1772 pin 4
    Proximity: From J1772 pin 5
```

**Charge Control Sequence**:
1. J1772 cable plugged in (proximity detected)
2. Vehicle confirms ready to charge (pilot handshake)
3. BMS confirms battery ready to accept charge
4. OBC closes internal contactors
5. Charging begins at negotiated rate
6. BMS monitors and can stop charge if needed

### Charge Port Location

Recommended locations:
- **Front fender**: Where fuel door would be
- **Rear quarter panel**: Near tail light

Installation:
- Waterproof mounting
- Cable routing to OBC location
- Indicator light visible to driver

## Instrumentation and Gauges

### State of Charge Gauge

```
[BMS SOC Output] ---> [Gauge Display]
    Signal: 0-5V or CAN bus message
    0V or 0% = Empty
    5V or 100% = Full
```

Options:
- Analog gauge (0-5V input)
- Digital display (serial or CAN)
- Repurpose fuel gauge

### Voltage Meter

```
[Battery Pack HV+] ---> [Voltage Divider] ---> [Digital Meter]
```

**Voltage Divider**:
- Input: 0-450V DC
- Output: 0-5V DC
- Resistor Ratio: R1:R2 = 89:1 (where R2 is the lower resistor to ground)
- For example: R1 = 890kΩ, R2 = 10kΩ
- Resistors: High-voltage rated, 1% tolerance

### Current Meter (Ammeter)

```
[HV+ Line] ---> [Shunt Resistor] ---> [Current Display]
```

**Current Shunt**:
- Rating: 500A, 50mV
- Location: In HV+ line near battery
- Display: Shows current where 50mV across shunt = 500A
- Conversion: 0.1mV per amp (or 10A per mV)

### Temperature Sensors

Monitor:
- Motor temperature
- Controller temperature
- Battery pack temperature

Use K-type thermocouples or thermistors with digital displays.

## Warning Lights and Indicators

### Dashboard Indicators

| Indicator | Function | Trigger |
|-----------|----------|---------|
| HV Active (Orange) | High voltage present | Main contactor closed |
| Ready (Green) | System ready to drive | PDM enabled, no faults |
| Charging (Blue) | Vehicle charging | OBC active |
| Fault (Red) | System fault | BMS or PDM error |
| Low Battery (Yellow) | Low state of charge | SOC < 20% |

### Wiring for Indicators

```
[PDM Status Output] ---> [Dashboard LED]
[BMS Status Output] ---> [Dashboard LED]
[OBC Status Output] ---> [Dashboard LED]

Each with appropriate resistor for LED current limiting.
```

## Grounding and Shielding

### Grounding Strategy

1. **HV Ground**: Battery negative to chassis at single point (near battery)
2. **LV Ground**: 12V battery negative to chassis at single point
3. **Ground Bonding**: HV and LV grounds should be bonded at the same chassis location to prevent ground potential differences
4. **Signal Ground**: All low-voltage signals reference common ground bus
5. **Motor Case**: Bonded to chassis for safety

**Important**: Single-point grounding strategy with HV and LV grounds bonded together prevents ground loops and dangerous voltage differences.

### Cable Shielding

Shield the following:
- CAN bus cables (drain shield to ground at one end only)
- Throttle sensor cable (shield to ground at controller end)
- Any analog sensor cables

## Safety Features Summary

### Critical Safety Circuits

1. **Interlock Loop**: Disables HV when panels removed
2. **BMS Protection**: Monitors and protects battery
3. **Inertia Switch**: Disconnects HV in accident
4. **Emergency Disconnect**: Manual HV shutdown

### Inertia Switch Installation

```
[Inertia Switch] --in series with--> [Main Contactor Coil]
```

- Location: Mounted to chassis (like original fuel pump inertia switch)
- Impact threshold: Set to trigger in moderate collision
- Reset: Manual button after inspection

## Testing Procedures

### High-Voltage System Testing

1. **Insulation Resistance Test**:
   - Disconnect HV from chassis
   - Measure HV+ to chassis: >500kΩ
   - Measure HV- to chassis: >500kΩ

2. **Pre-charge Circuit Test**:
   - Measure voltage across main contactor before close
   - Should see gradual rise over 2-5 seconds
   - Voltage should reach ~90% of pack voltage before main contactor closes

3. **Contactor Operation**:
   - Verify clean, crisp engagement (no arcing)
   - Check coil voltage: 12V ±0.5V
   - Measure contact resistance: <1mΩ

### Low-Voltage System Testing

1. **DC-DC Converter**:
   - Measure output voltage: 14.4V ±0.2V
   - Load test: 50A draw maintains voltage
   - Verify shutdown when HV disabled

2. **BMS Communication**:
   - Check CAN bus messages (120Ω termination)
   - Verify all module voltages reported
   - Confirm temperature readings

3. **Throttle Calibration**:
   - Pedal released: 0.5V ±0.1V
   - Pedal full: 4.5V ±0.1V
   - Linear response through range

## Wiring Harness Fabrication Tips

1. **Use Proper Connectors**:
   - Weatherproof for exterior
   - High-current for HV (Anderson, Deutsch)
   - Sealed for CAN bus

2. **Label Everything**:
   - Wire labels every 12 inches
   - Connection labels at both ends
   - Keep documentation

3. **Strain Relief**:
   - Support cables every 18-24 inches
   - Prevent vibration damage
   - Allow for movement without tension

4. **Protection**:
   - Split loom or conduit for all cables
   - Keep HV and LV separated
   - Route away from heat sources

## Troubleshooting Guide

### No High Voltage at PDM

Check:
- Main fuse continuity
- Service disconnect position
- Contactor operation (should hear click)
- Pre-charge circuit function
- Interlock loop continuity

### PDM Won't Enable

Check:
- 12V power to PDM
- Enable signal from BMS
- Ignition switch position
- CAN bus communication
- Fault codes in PDM

### Charging Not Working

Check:
- J1772 cable connection
- Pilot signal handshake
- OBC 12V power
- BMS allowing charge
- AC power at inlet

### Intermittent Power Loss

Check:
- All HV connections tight
- Contactor contact wear
- BMS intermittent faults
- Thermal issues (overheating)
- Ground connections

## Maintenance Checklist

### Monthly

- [ ] Inspect all HV connections for tightness
- [ ] Check for signs of overheating (discoloration)
- [ ] Verify interlock loop function
- [ ] Test emergency disconnect

### Quarterly

- [ ] Perform insulation resistance test
- [ ] Check contactor contact resistance
- [ ] Verify BMS cell balance
- [ ] Inspect all cable routing for wear

### Annually

- [ ] Torque all HV connections to spec
- [ ] Replace any worn connectors
- [ ] Update firmware if available
- [ ] Full system diagnostic

## Wiring Color Codes

### High-Voltage (360V)

| Color | Function |
|-------|----------|
| Orange | HV positive |
| Orange with blue stripe | HV negative |
| Orange with white stripe | HV phase U |
| Orange with black stripe | HV phase V |
| Orange with green stripe | HV phase W |

### Low-Voltage (12V)

| Color | Function |
|-------|----------|
| Red | +12V switched (ignition) |
| Yellow | +12V constant |
| Black | Ground |
| Green | Signals/sensors |
| Blue | Accessories |
| Purple | Lighting |

## Conclusion

Proper wiring is critical for safe and reliable operation of your EV conversion. Take your time, double-check all connections, and test thoroughly before road operation.

**Always prioritize safety when working with high-voltage systems.**

For additional questions or clarification, consult with an experienced EV converter or electrical engineer.
