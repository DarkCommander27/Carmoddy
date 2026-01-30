# Safety Guidelines - EV Conversion

## ⚠️ CRITICAL SAFETY INFORMATION

Converting a vehicle to electric propulsion involves working with high-voltage DC electrical systems that can be **LETHAL**. This is not a project for beginners. Only attempt this conversion if you have appropriate knowledge, skills, and safety equipment.

**High voltage can kill you.** Take every safety precaution seriously.

## Overview

This document covers essential safety information for converting a 1992 Ford Escort to electric using Nissan Leaf components. The primary hazards include:

- **Electrical shock**: 360V DC can cause death
- **Arc flash**: High-voltage arcs can cause severe burns
- **Chemical**: Battery electrolyte exposure
- **Fire**: Electrical and battery fires
- **Mechanical**: Heavy components and vehicle modifications
- **Crush hazards**: Working under vehicle

## High-Voltage Safety

### Understanding High-Voltage DC

- **Nissan Leaf battery pack**: 360V nominal (403V fully charged)
- **Lethal voltage**: Generally considered >50V DC
- **Current availability**: Battery can deliver 300+ amps
- **Energy stored**: 24-30 kWh (equivalent to 1-2 gallons of gasoline in energy)

**Key Point**: Unlike AC, DC doesn't "let go" - muscle contractions can prevent releasing an energized conductor.

### High-Voltage Safety Equipment

#### Required Personal Protective Equipment (PPE)

1. **Class 0 or Higher Insulated Gloves**
   - Voltage rating: Minimum 1000V (Class 0)
   - System operates at 360V nominal, 403V max (requires 1.5x safety margin)
   - Must be tested annually per ASTM F496
   - Inspect before each use for damage
   - Use with leather protector gloves
   - Cost: $150-$300

2. **Insulated Tools**
   - Screwdrivers, wrenches, pliers rated for 1000V
   - Insulated handles with intact coating
   - Cost: $100-$200 for basic set

3. **Arc-Rated Safety Glasses**
   - Protect from arc flash
   - Minimum rating: ANSI Z87.1
   - Cost: $20-$50

4. **Non-Conductive Footwear**
   - Rubber-soled shoes (no metal eyelets/shanks)
   - Dry at all times
   - Cost: $50-$150

5. **Voltage Detector**
   - Non-contact high-voltage detector
   - Audible and visual indication
   - Test before each use
   - Cost: $50-$150

#### Optional but Recommended

- Insulated mat to stand on when working
- Face shield for high-energy work
- Fire-resistant clothing (Nomex or similar)

### High-Voltage Work Procedures

#### The Safe Approach: Always Follow These Steps

1. **Assume Live**: Treat all HV components as energized until proven otherwise

2. **Lockout/Tagout**:
   - Remove service disconnect plug
   - Lock out with padlock if possible
   - Tag with "DO NOT OPERATE" tag
   - Keep key on your person

3. **Verify De-energization**:
   - Wait minimum 5 minutes for capacitor discharge
   - Use HV detector to verify no voltage at multiple points
   - Measure voltage with high-voltage multimeter (<5V safe)
   - If needed, discharge capacitors using proper discharge tool (insulated stick with 1kΩ, 50W resistor)

4. **Ground if Necessary**:
   - For certain procedures, ground HV bus to chassis
   - Use proper grounding equipment
   - Verify ground connection before proceeding

5. **Barrier and Signs**:
   - If leaving work area, replace panels
   - Post warning signs
   - Prevent unauthorized access

#### One-Hand Rule

When working on potentially live circuits:
- Keep one hand behind your back or in pocket
- Prevents current path across chest (through heart)
- Use insulated tools only
- Stand on insulated mat

### High-Voltage Component Identification

Mark all HV components with orange warning labels:

**Required Labels**:
- Battery enclosures: "DANGER - HIGH VOLTAGE - 360V DC"
- HV cables: Orange sheathing (standard)
- Motor controller: "DANGER - HIGH VOLTAGE INSIDE"
- On-board charger: "DANGER - HIGH VOLTAGE INSIDE"
- Motor: "CAUTION - HIGH VOLTAGE CONNECTIONS"
- Service disconnect: "MAIN HV DISCONNECT"

### Arc Flash Hazards

High-voltage DC can create sustained arcs:

**Prevention**:
- Never work on live circuits unless absolutely necessary
- Use insulated tools
- Ensure all connections are tight before energizing
- Install HV fuses/breakers properly rated

**If Arc Occurs**:
- Do not look at arc (eye damage)
- Shut off power immediately
- Evacuate area
- Check for fire

## Battery Safety

### Lithium-Ion Battery Hazards

Nissan Leaf uses lithium manganese oxide batteries:

**Hazards**:
- **Thermal runaway**: Overheating can cause fire
- **Fire**: Difficult to extinguish, produces toxic fumes
- **Electrical**: High voltage and current
- **Chemical**: Electrolyte is corrosive and flammable
- **Physical**: Heavy modules (~13.5 lbs each, 48 modules total = ~650 lbs)

### Battery Handling Procedures

1. **Inspect Before Use**:
   - Check for swelling (damaged cells)
   - Look for corrosion on terminals
   - Smell for unusual odors (sweet = electrolyte leak)
   - Verify voltage of each module

2. **Lifting and Moving**:
   - Complete battery pack: ~650 lbs (use multiple people or hoist)
   - Individual modules: 4 lbs (manageable but handle carefully)
   - Never drop or impact modules
   - Support evenly to prevent case stress

3. **Storage**:
   - Store at 30-60% state of charge (3.6-3.8V per cell)
   - Cool, dry location
   - Away from flammable materials
   - Protected from physical damage
   - Monitor voltage monthly

### Battery Fire Safety

**Prevention**:
- Proper BMS monitoring and protection
- Adequate ventilation to prevent gas buildup
- Protect from physical damage
- Avoid overcharging or over-discharging
- Monitor temperatures

**If Battery Fire Occurs**:

1. **Evacuate Immediately**: Get everyone away from vehicle
2. **Call 911**: Tell them it's an electric vehicle battery fire
3. **Do Not Attempt to Fight Fire**: Leave to professional firefighters
   - Only attempt suppression if: fire is very small, you have proper training and equipment, and you have a clear escape route
4. **If Attempting Suppression** (trained personnel only):
   - Class D extinguisher for small fires
   - Large amounts of water (if electrically safe and fire is accessible)
5. **Toxic Fumes**: Stay upwind, wear respirator if available
6. **Thermal Runaway**: Can reignite hours later; monitor

**Battery Fire Extinguisher**:
- Class D extinguisher rated for metal fires
- Large amounts of water can also work (if electrically safe)
- ABC extinguisher NOT recommended (may spread fire)
- Cost: $50-$150

### Cell Balancing and BMS

**Why Important**:
- Imbalanced cells can lead to overcharge or undercharge
- Overcharged cells can vent or catch fire
- BMS monitors and protects each cell

**Regular Checks**:
- Monitor cell voltages weekly initially
- Check for imbalance >50mV
- Verify BMS is functioning
- Don't bypass BMS safety features

## Electrical Shock Prevention

### First Aid for Electrical Shock

**If Someone is Being Shocked**:

1. **DO NOT TOUCH** the person (you'll be shocked too)
2. **Cut Power**: Open service disconnect if safe
3. **Use Non-Conductive Object**: Push person away with wood, plastic
4. **Call 911** immediately
5. **Start CPR** if trained and person is not breathing
6. **Use AED** if available

**Even if Person Seems OK**:
- Electrical shock can cause delayed cardiac issues
- Seek medical attention immediately
- Monitor for 24 hours

### Preventing Accidental Contact

1. **Cover All Connections**:
   - Use insulated boots on terminals
   - Shrink wrap or tape exposed conductors
   - Install barriers around HV components

2. **Interlocks**:
   - Install switches on all HV access panels
   - Opening panel disables HV system
   - Test interlocks regularly

3. **Service Disconnect**:
   - Located in accessible position
   - Clearly labeled
   - Interrupts HV+ line
   - Removable plug for lockout

4. **Color Coding**:
   - Orange = High Voltage (360V)
   - Red = 12V positive
   - Black = Ground
   - Never deviate from standard colors

## Mechanical Safety

### Working Under Vehicle

**Requirements**:
- Use proper jack stands rated for vehicle weight
- Never use jack alone to support vehicle
- Wheel chocks on wheels remaining on ground
- Solid, level surface
- Inspect jack stands for damage before use

**Battery Installation Safety**:
- Batteries add significant weight (~650 lbs)
- Ensure mounts are structural and properly welded
- Test weight distribution doesn't overload suspension
- Secure battery boxes to prevent movement in accident

### Lifting Heavy Components

**Motor and Battery Pack**:
- Use engine hoist rated for weight
- Inspect hoist and chains before use
- Never work under suspended load
- Use helper to guide components
- Secure load with proper sling/chain placement

**Back Safety**:
- Lift with legs, not back
- Get help for >50 lb components
- Use mechanical advantage when possible

### Welding Safety

**When Fabricating Mounts**:
- Welding near battery = EXTREME DANGER
- **ALWAYS** disconnect batteries before welding
- Wait minimum 10 minutes after disconnect
- **VERIFY de-energization with multimeter** before welding
- Ground welding current path away from HV components
- Fire extinguisher on hand
- Adequate ventilation

**Battery Exposure During Welding**:
- Welding spark = battery fire risk
- Cover battery boxes with fire blanket
- Never weld directly on battery enclosure with batteries inside

## Chemical Safety

### Battery Electrolyte

**Characteristics**:
- Lithium salt electrolyte (LiPF6 in organic solvents)
- Corrosive to skin and eyes
- Flammable
- Reacts with water to produce hydrofluoric acid (HF) in solution
- At high temperatures or during fire, can release toxic HF gas

**In Case of Leak**:
- Evacuate area
- Ventilate
- Wear nitrile gloves and eye protection
- Absorb with sand or chemical absorbent (not water)
- Dispose as hazardous waste
- Seek medical attention if skin contact

### Other Chemicals

- **Dielectric grease**: Use for HV connections
- **Thermal paste**: For heat sinks
- **Cutting fluids**: When machining
- **Welding fumes**: Adequate ventilation

Always read and follow Safety Data Sheets (SDS).

## Fire Safety

### Fire Extinguisher Requirements

**Type and Location**:
- **ABC or BC rated** (electrical fires)
- **5-10 lb** capacity minimum
- Mounted in vehicle cabin (easily accessible)
- Note: ABC extinguishers are suitable for general electrical fires but NOT for lithium battery fires
- For battery fires in workshop, use Class D extinguisher
- Check monthly (pressure gauge in green)
- Know how to use (PASS method: Pull, Aim, Squeeze, Sweep)

**Additional Recommended**:
- Class D extinguisher in workshop (for battery fires)
- Fire blanket (to smother small fires)

### Workshop Fire Safety

- **Smoke detectors**: Install and test monthly
- **Exit plan**: Know two ways out
- **No smoking**: Near batteries or during charging
- **Flammable storage**: Keep fuel, solvents away from batteries
- **Charging safety**: Monitor first few charges closely

## Charging Safety

### Level 1 (120V) and Level 2 (240V) Charging

**Electrical Safety**:
- Use GFCI-protected outlets
- Inspect charge cable for damage before each use
- Don't use extension cords (if unavoidable, use heavy-duty 12AWG minimum)
- Don't charge in rain unless equipment is rated for wet conditions
- Don't charge near flammable materials

**During Charging**:
- Monitor first several charging sessions
- Check for unusual smells or sounds
- Feel cables for excessive heat (warm is normal, hot is not)
- Don't exceed charging circuit capacity (see specifications)

### Charging in Garage

- **Ventilation**: Ensure adequate air flow
- **Monitoring**: Check periodically during charge
- **Unplug when complete**: Reduces wear on equipment
- **Keep clear**: Don't pile items on or near charging vehicle

## Testing and Commissioning Safety

### Initial Power-Up

**First-Time Energization**:
1. Ensure all personnel are clear
2. Put on full HV safety equipment
3. Have fire extinguisher ready
4. Close contactor from distance if possible
5. Monitor voltages and temperatures continuously
6. Have assistant ready to hit emergency stop

### Road Testing

**First Drive Precautions**:
- Choose empty parking lot or private road
- Have chase vehicle for emergency
- Fire extinguisher in vehicle
- Cell phone charged
- Inspect thoroughly after each test drive
- Check for hot spots with IR thermometer

**What to Monitor**:
- Battery voltage and balance
- Motor and controller temperature
- Unusual noises or vibrations
- Proper operation of all safety systems
- Brake function (both friction and regenerative)

## Legal and Regulatory Considerations

### Vehicle Registration

- Conversion may require inspection and re-registration
- Some jurisdictions require engineering certification
- Check state/provincial laws before starting

### Insurance

- **NOTIFY YOUR INSURANCE COMPANY**
- Some insurers won't cover modified vehicles
- Shop around for EV-friendly insurers
- Document conversion for insurance purposes

### Liability

- Understand that you're responsible for safety of modification
- Consider additional liability insurance
- Keep detailed records of all work performed
- Use qualified help for complex tasks

## Environmental Considerations

### Proper Disposal

**Battery Disposal**:
- Never throw lithium batteries in regular trash
- Contact recycling center for lithium battery disposal
- Some auto parts stores accept for recycling
- Check for local hazardous waste collection days

**Other Components**:
- Recycle removed engine, transmission (scrap metal)
- Dispose of fluids properly (oil, coolant, fuel)
- Recycle electronics when replaced

### Fuel Removal

- **Extreme Fire Hazard**
- Drain fuel into approved containers
- Dispose at hazardous waste facility or use in other vehicle
- Never pour on ground or down drain
- Clean residual fuel from tank before disposal

## Working Alone vs. with Helper

### When Helper is REQUIRED

- Initial HV system energization
- First test drives
- Any work under vehicle
- Moving heavy components (>50 lbs)
- Any time you feel unsafe

### Helper's Responsibilities

- Know where emergency disconnect is
- Know how to call 911
- Basic first aid knowledge
- Be alert and sober
- Don't distract person doing critical work

## Emergency Procedures

### Emergency Shutdown

**In Vehicle**:
1. Turn off ignition (disables motor controller)
2. Main service disconnect (if accessible)

**In Workshop**:
1. Main service disconnect
2. Shore power disconnect (if charging)
3. Verify de-energization with meter

### Accident Scenarios

**Minor Collision**:
- Check for HV system damage
- Verify no exposed HV conductors
- Check battery box integrity
- If any damage to HV system, don't drive; tow

**Major Collision**:
- Exit vehicle immediately if safe
- Open service disconnect if accessible and safe
- Move far from vehicle
- Call 911, inform them of HV system
- Don't allow anyone near vehicle
- Inform first responders: "Electric vehicle with 360-volt battery"

### First Responder Information

**Create Info Card** to keep in glove box:

```
ELECTRIC VEHICLE - HIGH VOLTAGE

Battery: 360V DC, 24-30 kWh lithium-ion
Location: [Trunk floor and/or fuel tank area]

Service Disconnect: [Location]
  - Opens high-voltage circuit
  - [Description of how to open]

Emergency Contact: [Your name and phone]

WARNING: Battery can reignite after fire is extinguished
```

## Safety Checklist Before Each Drive

- [ ] Visual inspection of HV cables and connections
- [ ] Check for unusual smells
- [ ] Verify BMS shows no faults
- [ ] Test emergency shutdown procedure
- [ ] Check tire pressure
- [ ] Verify brake function
- [ ] Check state of charge
- [ ] Ensure fire extinguisher is accessible

## Safety Training Resources

### Recommended Training

Before starting this project, consider:

- **Hybrid/EV Safety Training**: Many technical colleges offer courses
- **High-Voltage Electrical Safety**: OSHA or NFPA 70E training
- **First Aid/CPR**: American Red Cross or equivalent
- **Fire Safety**: Local fire department may offer training

### Information Resources

- **NFPA 70E**: Standard for Electrical Safety in the Workplace
- **SAE J1772**: EV charging connector standard
- **ISO 6469**: Safety requirements for electric vehicles
- **DIY Electric Car Forums**: Community knowledge
- **EV conversion companies**: May offer consulting

## Safety is Not Optional

This cannot be stressed enough: **High-voltage electrical systems are deadly**. Every safety procedure in this document exists because of injuries or deaths that have occurred.

**If you are not comfortable with any aspect of this conversion, get help from qualified professionals.**

### When to Stop and Get Help

- You don't understand a procedure
- You don't have proper safety equipment
- Something seems wrong but you can't identify it
- You're tired or impaired
- You're working alone on a critical task
- Equipment is damaged or malfunctioning

## Final Safety Reminders

1. ✅ Treat all HV as live until proven otherwise
2. ✅ Use proper PPE every time
3. ✅ Follow lockout/tagout procedures
4. ✅ Keep fire extinguisher accessible
5. ✅ Test safety systems regularly
6. ✅ Never bypass safety features
7. ✅ Document your work
8. ✅ When in doubt, seek expert help

**Your life is worth more than completing this project quickly.**

Stay safe, and enjoy your electric Ford Escort!
