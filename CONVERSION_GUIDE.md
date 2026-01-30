# 1992 Ford Escort to Electric Vehicle Conversion Guide

## Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Phase 1: Planning and Preparation](#phase-1-planning-and-preparation)
4. [Phase 2: Removal of ICE Components](#phase-2-removal-of-ice-components)
5. [Phase 3: Motor Installation](#phase-3-motor-installation)
6. [Phase 4: Battery Pack Installation](#phase-4-battery-pack-installation)
7. [Phase 5: Electrical System Integration](#phase-5-electrical-system-integration)
8. [Phase 6: Auxiliary Systems](#phase-6-auxiliary-systems)
9. [Phase 7: Testing and Commissioning](#phase-7-testing-and-commissioning)
10. [Troubleshooting](#troubleshooting)

## Introduction

This guide provides detailed instructions for converting a 1992 Ford Escort from internal combustion engine (ICE) to electric propulsion using components from a Nissan Leaf. The conversion leverages the Leaf's proven electric drivetrain technology while maintaining the Escort's classic appeal.

### Estimated Timeline

- Planning and parts acquisition: 2-4 weeks
- Mechanical work: 3-6 weeks
- Electrical integration: 2-3 weeks
- Testing and refinement: 1-2 weeks

**Total: 8-15 weeks** (depending on experience and available time)

## Prerequisites

### Skills Required

- Automotive mechanical experience
- Electrical/electronic systems knowledge
- Welding and fabrication skills
- Understanding of high-voltage DC systems
- Ability to read wiring diagrams

### Tools Needed

- Complete automotive tool set
- Engine hoist
- MIG/TIG welder
- Multimeter and electrical testing equipment
- High-voltage safety equipment (insulated gloves, testing probes)
- Cutting and grinding tools
- Hydraulic jack and jack stands

### Workspace

- Well-ventilated garage or workshop
- Access to 240V power for testing
- Adequate lighting
- Fire extinguisher rated for electrical fires

## Phase 1: Planning and Preparation

### Step 1.1: Vehicle Assessment

1. Thoroughly inspect the 1992 Ford Escort donor vehicle
2. Check structural integrity, especially frame rails and suspension mounts
3. Document the current weight distribution
4. Identify mounting points for new components

### Step 1.2: Weight Calculations

- Original Ford Escort curb weight: ~2,200 lbs
- Nissan Leaf battery pack weight: ~650 lbs
- Nissan Leaf motor weight: ~130 lbs
- Expected final weight: ~2,400-2,600 lbs

### Step 1.3: Design Decisions

1. **Battery Placement**: Typically in former fuel tank area and/or trunk
2. **Motor Mounting**: Adapt to existing engine mounts or fabricate new ones
3. **Controller Location**: Protected, ventilated area (often firewall)
4. **Charging Port**: Front fender or rear quarter panel

### Step 1.4: Obtain Donor Components

- Source Nissan Leaf components (see [PARTS_LIST.md](PARTS_LIST.md))
- Verify all components are functional
- Test motor and controller if possible before installation

## Phase 2: Removal of ICE Components

### Step 2.1: Preparation

1. Disconnect battery (negative terminal first)
2. Drain all fluids (engine oil, coolant, transmission fluid, fuel)
3. Remove hood for better access
4. Label and photograph all connections before removal

### Step 2.2: Remove Engine and Transmission

1. Disconnect all electrical connections
2. Remove exhaust system from manifold back
3. Disconnect fuel lines and vacuum hoses
4. Remove radiator and cooling system
5. Unbolt transmission from driveshaft
6. Support engine with hoist
7. Remove engine mount bolts
8. Carefully lift engine and transmission out as a unit

### Step 2.3: Remove Fuel System

1. Safely remove fuel tank
2. Remove fuel lines throughout vehicle
3. Cap or remove filler neck
4. Properly dispose of fuel and fuel system components

### Step 2.4: Clean and Prepare

1. Clean engine bay thoroughly
2. Remove unnecessary brackets and mounts
3. Inspect for rust or damage requiring repair
4. Paint or rust-proof exposed areas

## Phase 3: Motor Installation

### Step 3.1: Create Motor Adapter Plate

1. Measure Nissan Leaf motor mounting pattern
2. Measure Ford Escort transmission bell housing pattern
3. Design adapter plate to mate motor to transmission
4. Fabricate adapter from 1/2" steel or aluminum plate
5. Machine or have machined for precise fit

### Step 3.2: Driveshaft Coupling

1. Measure motor output shaft and transmission input shaft
2. Source or fabricate coupling to connect motor to transmission
3. Ensure proper alignment and balance
4. Consider using professional driveline shop for this critical component

### Step 3.3: Motor Mounting

1. Position motor in engine bay
2. Fabricate motor mounts to secure motor to chassis
3. Ensure motor is properly aligned with transmission
4. Use vibration-damping motor mounts
5. Bolt motor securely to mounts
6. Verify clearance for all rotating components

### Step 3.4: Transmission Considerations

**Option A**: Keep original manual transmission
- Simplest option
- Allows traditional shifting
- Motor can handle direct drive in higher gears

**Option B**: Remove transmission, use direct drive
- Reduces weight and complexity
- May require different rear-end gearing
- Limits top speed and acceleration options

For this guide, we assume keeping the manual transmission.

## Phase 4: Battery Pack Installation

### Step 4.1: Battery Placement Planning

Nissan Leaf battery modules can be configured in various ways:

**Recommended Configuration**:
- Main battery: Former fuel tank area (underfloor)
- Secondary modules: Trunk floor
- Ensures good weight distribution

### Step 4.2: Fabricate Battery Boxes

1. Design battery enclosures with:
   - Structural support
   - Impact protection
   - Ventilation
   - Water resistance
   - Electrical insulation

2. Build from:
   - 16-gauge steel or aluminum
   - Sealed with automotive sealant
   - Mounted securely to chassis

### Step 4.3: Install Battery Modules

1. Create mounting frames for battery modules
2. Ensure batteries are securely fastened (critical for safety)
3. Connect modules in series to achieve desired voltage
   - Nissan Leaf modules: typically 7.6V each
   - Target: 360V for full system (matching Leaf voltage)
4. Install battery management system (BMS) sensors on each module
5. Route high-voltage cables in protected conduit

### Step 4.4: Battery Cooling

1. Maintain Leaf's passive air cooling system if possible
2. Route cooling air ducts to battery boxes
3. Consider adding fans for active cooling if needed
4. Monitor temperatures during testing

## Phase 5: Electrical System Integration

### Step 5.1: High-Voltage System

1. Install motor controller in protected location
2. Run high-voltage cables from battery to controller
   - Use proper gauge wire (typically 00 or 000 AWG)
   - Use orange conduit/sheathing (standard for HV)
   - Keep cables as short as practical
3. Connect controller to motor (3-phase cables)
4. Install main contactor/disconnect
5. Install fuses/circuit breakers for protection

### Step 5.2: Low-Voltage System

1. Install DC-DC converter (HV to 12V)
   - Powers original 12V accessories
   - Charges 12V auxiliary battery
2. Maintain original 12V battery for accessories
3. Connect ignition switch to controller enable signal
4. Wire throttle position sensor
5. Connect brake light switch to controller (for regen)

### Step 5.3: Instrumentation

1. Install battery state-of-charge gauge
2. Install voltage and current meters
3. Add motor temperature sensor and gauge
4. Consider adding:
   - Power meter (kW)
   - Efficiency meter
   - Range estimator

### Step 5.4: Safety Systems

1. Install high-voltage disconnect switch in accessible location
2. Add HV warning lights/labels
3. Install inertia switch to cut power in accident
4. Ensure proper grounding of all HV components
5. Install current limiter/circuit protection

See [WIRING.md](WIRING.md) for detailed wiring diagrams.

## Phase 6: Auxiliary Systems

### Step 6.1: Vacuum System (for Brakes)

Options:
- **Electric vacuum pump**: Maintains brake boost
- **Hydraulic brake booster**: Replaces vacuum system
- Install pressure switch and vacuum reservoir

### Step 6.2: Power Steering

Options:
- **Electric power steering pump**: Maintains power steering
- **Manual steering**: Remove power steering (more effort required)
- Conversion to electric pump recommended for comfort

### Step 6.3: Heating and Cooling

**Heating**:
- Electric cabin heater (12V or high-voltage)
- Heated seats for efficiency
- Resistance heater or heat pump

**Cooling**:
- Electric A/C compressor from Leaf or aftermarket
- Electric radiator fan for motor/controller cooling

### Step 6.4: Charging System

1. Install J1772 charging port (standard for North America)
2. Mount on-board charger (from Nissan Leaf)
3. Wire charger to battery pack
4. Install charge indicator lights
5. Test with Level 1 (120V) and Level 2 (240V) charging

## Phase 7: Testing and Commissioning

### Step 7.1: Pre-Power Checks

1. Verify all connections are tight
2. Check for proper grounding
3. Inspect high-voltage cable routing
4. Ensure no exposed high-voltage conductors
5. Verify proper fusing and circuit protection

### Step 7.2: Initial Power-Up

1. Put on high-voltage safety equipment
2. Close main contactor with controller disabled
3. Measure battery pack voltage
4. Check for voltage leaks to chassis (should be >500kΩ)
5. Enable controller
6. Check for error codes

### Step 7.3: Static Testing

1. With vehicle on jack stands (wheels free):
2. Enable motor controller
3. Gently apply throttle
4. Verify motor rotation direction
5. Test regenerative braking
6. Check all gauges and indicators

### Step 7.4: Road Testing

**First Drive**:
1. Choose safe, empty parking lot
2. Have observer for safety
3. Start with low-speed operation
4. Test acceleration, braking, and handling
5. Monitor temperatures and voltages

**Extended Testing**:
1. Gradually increase test distances
2. Monitor battery performance
3. Check for vibrations or unusual noises
4. Fine-tune controller parameters
5. Test charging system

### Step 7.5: Calibration

1. Adjust throttle response curve
2. Set regenerative braking strength
3. Configure battery management parameters
4. Calibrate state-of-charge indicator
5. Set under-voltage and over-voltage protection

## Troubleshooting

### Motor Won't Run

- Check main contactor operation
- Verify controller has power
- Check enable/ignition signal to controller
- Inspect motor phase connections
- Review controller error codes

### Intermittent Power Loss

- Check high-voltage connections for tightness
- Inspect BMS for individual cell issues
- Verify proper cooling of controller
- Check for loose grounds

### Excessive Battery Drain

- Check for parasitic draws on 12V system
- Verify DC-DC converter efficiency
- Check for BMS staying active when parked
- Inspect for current leaks in HV system

### Poor Range

- Verify battery pack capacity
- Check tire pressure
- Assess driving style (acceleration/braking)
- Inspect for mechanical drag (brakes, bearings)
- Verify aerodynamics (seal gaps, remove excess weight)

### Charging Issues

- Check J1772 port connections
- Verify on-board charger operation
- Inspect BMS charging parameters
- Test with different charging stations

## Performance Expectations

### Range

- Expected range: 60-90 miles (depending on battery size and driving)
- City driving: Higher efficiency due to regenerative braking
- Highway: Reduced range due to higher power consumption

### Performance

- 0-60 mph: ~10-12 seconds (adequate for daily driving)
- Top speed: 85-95 mph (limited by gearing and motor)
- Regenerative braking extends range and reduces brake wear

### Charging

- Level 1 (120V): 12-20 hours for full charge
- Level 2 (240V): 4-6 hours for full charge
- DC fast charging: Not typically available for DIY conversions

## Maintenance

### Regular Checks

- Battery pack voltage and balance (monthly)
- Motor/controller temperature operation (after long drives)
- Tire pressure (weekly)
- Brake system (monthly)
- All electrical connections (quarterly)

### Annual Maintenance

- Full battery capacity test
- Verify torque on all high-voltage connections
- Inspect motor bearings
- Test safety systems
- Update controller firmware if available

## Legal Considerations

- Check local laws regarding vehicle modifications
- May require engineering inspection
- Update vehicle registration (some jurisdictions)
- Notify insurance company
- Emissions testing may no longer apply

## Conclusion

Converting a 1992 Ford Escort to electric using Nissan Leaf components is a challenging but rewarding project. With proper planning, execution, and safety precautions, you can create a unique and sustainable electric vehicle.

Remember: Safety is paramount when working with high-voltage systems. If you're unsure about any step, consult with experts or seek professional assistance.

Good luck with your conversion!
