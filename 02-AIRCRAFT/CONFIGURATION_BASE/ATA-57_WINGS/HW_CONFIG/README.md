# HW_CONFIG - Hardware Configuration

This directory contains hardware configuration data including LRU (Line Replaceable Unit) configurations, physical connections, installation specifications, and part numbers.

## Purpose

Hardware configuration documentation ensures:
- Correct component selection and installation
- Proper physical interfaces and connections
- Traceability to design requirements
- Support for maintenance and logistics
- Configuration control of hardware items

## Contents

This directory should contain:

### LRU Configurations
- **Component specifications** - Technical data for each LRU
- **Part numbers** - Manufacturer and internal part numbers
- **Variants and options** - Different configurations and alternatives
- **Interchangeability data** - Substitutable components

### Physical Configuration
- **Installation drawings** - Mounting locations and arrangements
- **Connector pinouts** - Electrical and data connections
- **Harness routings** - Cable and wire routing paths
- **Interface definitions** - Physical interface specifications

### Hardware Documentation
- **Datasheets** - Manufacturer specifications
- **Assembly procedures** - Installation instructions
- **Test procedures** - Acceptance and functional tests
- **Maintenance manuals** - Repair and troubleshooting guides

## File Organization

```
HW_CONFIG/
├── LRU_AILERON_ACTUATOR/       # Aileron control actuators
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   ├── TEST_PROCEDURES.pdf
│   ├── ACM/                    # Aircraft Component Manual
│   │   ├── ACM_AILERON_ACTUATOR.pdf
│   │   ├── COMPONENT_BREAKDOWN.pdf
│   │   ├── MAINTENANCE_MANUAL.pdf
│   │   ├── ILLUSTRATED_PARTS_CATALOG.pdf
│   │   └── TROUBLESHOOTING_GUIDE.pdf
│   └── SUBCOMPONENTS/
│       ├── ACTUATOR_MOTOR.pdf
│       ├── CONTROL_VALVE.pdf
│       ├── POSITION_SENSOR.pdf
│       └── MOUNTING_BRACKETS.pdf
├── LRU_FLAP_DRIVE_UNIT/        # Flap extension/retraction systems
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   ├── TEST_PROCEDURES.pdf
│   ├── ACM/                    # Aircraft Component Manual
│   │   ├── ACM_FLAP_DRIVE_UNIT.pdf
│   │   ├── COMPONENT_BREAKDOWN.pdf
│   │   ├── MAINTENANCE_MANUAL.pdf
│   │   ├── ILLUSTRATED_PARTS_CATALOG.pdf
│   │   └── TROUBLESHOOTING_GUIDE.pdf
│   └── SUBCOMPONENTS/
│       ├── PCU_POWER_CONTROL_UNIT.pdf
│       ├── GEARBOX_ASSEMBLY.pdf
│       ├── TRANSMISSION_SHAFT.pdf
│       └── TORQUE_LIMITER.pdf
├── LRU_SLAT_ACTUATOR/          # Slat control actuators
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   ├── TEST_PROCEDURES.pdf
│   ├── ACM/                    # Aircraft Component Manual
│   │   ├── ACM_SLAT_ACTUATOR.pdf
│   │   ├── COMPONENT_BREAKDOWN.pdf
│   │   ├── MAINTENANCE_MANUAL.pdf
│   │   ├── ILLUSTRATED_PARTS_CATALOG.pdf
│   │   └── TROUBLESHOOTING_GUIDE.pdf
│   └── SUBCOMPONENTS/
│       ├── DRIVE_MOTOR.pdf
│       ├── GEARBOX.pdf
│       ├── POSITION_TRANSMITTER.pdf
│       └── TRACK_ASSEMBLY.pdf
├── LRU_SPOILER_ACTUATOR/       # Spoiler panel actuators
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   ├── TEST_PROCEDURES.pdf
│   ├── ACM/                    # Aircraft Component Manual
│   │   ├── ACM_SPOILER_ACTUATOR.pdf
│   │   ├── COMPONENT_BREAKDOWN.pdf
│   │   ├── MAINTENANCE_MANUAL.pdf
│   │   ├── ILLUSTRATED_PARTS_CATALOG.pdf
│   │   └── TROUBLESHOOTING_GUIDE.pdf
│   └── SUBCOMPONENTS/
│       ├── HYDRAULIC_CYLINDER.pdf
│       ├── CONTROL_VALVE_ASSEMBLY.pdf
│       ├── LVDT_SENSOR.pdf
│       └── ATTACHMENT_FITTINGS.pdf
├── LRU_WING_TIP_LIGHT/         # Navigation and position lights
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   ├── TEST_PROCEDURES.pdf
│   ├── ACM/                    # Aircraft Component Manual
│   │   ├── ACM_WING_TIP_LIGHT.pdf
│   │   ├── COMPONENT_BREAKDOWN.pdf
│   │   ├── MAINTENANCE_MANUAL.pdf
│   │   ├── ILLUSTRATED_PARTS_CATALOG.pdf
│   │   └── TROUBLESHOOTING_GUIDE.pdf
│   └── SUBCOMPONENTS/
│       ├── LED_ASSEMBLY.pdf
│       ├── POWER_SUPPLY_MODULE.pdf
│       ├── LENS_ASSEMBLY.pdf
│       └── MOUNTING_HOUSING.pdf
├── LRU_ICE_DETECTION/          # Ice protection sensors
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   ├── TEST_PROCEDURES.pdf
│   ├── ACM/                    # Aircraft Component Manual
│   │   ├── ACM_ICE_DETECTION_SENSOR.pdf
│   │   ├── COMPONENT_BREAKDOWN.pdf
│   │   ├── MAINTENANCE_MANUAL.pdf
│   │   ├── ILLUSTRATED_PARTS_CATALOG.pdf
│   │   └── TROUBLESHOOTING_GUIDE.pdf
│   └── SUBCOMPONENTS/
│       ├── PROBE_ELEMENT.pdf
│       ├── SIGNAL_PROCESSING_UNIT.pdf
│       ├── HEATER_ELEMENT.pdf
│       └── CONNECTOR_ASSEMBLY.pdf
├── CONNECTORS/                  # Wing-specific connector definitions
│   ├── WING_ROOT_CONNECTORS.pdf
│   ├── CONTROL_SURFACE_CONNECTORS.pdf
│   └── SENSOR_CONNECTORS.pdf
├── ASSEMBLIES/                  # Wing hardware assemblies
│   ├── FLAP_TRACK_ASSEMBLY.pdf
│   ├── SLAT_TRACK_ASSEMBLY.pdf
│   └── WING_TIP_ASSEMBLY.pdf
└── BOM/                         # Wing bills of materials
    ├── LEFT_WING_BOM.csv
    ├── RIGHT_WING_BOM.csv
    └── WING_CONTROL_SURFACES_BOM.csv
```

## LRU Placement Rules

Per [Configuration Rules](../../ATA-00_GENERAL/RULES.md):
- LRUs reside in their **primary functional ATA chapter**
- Related hardware stays together with host system
- Cross-reference other chapters when interfaces exist

## Aircraft Component Manuals (ACM) Structure

Each LRU directory contains a dedicated **ACM/** subdirectory with comprehensive component documentation following ATA Spec 2200 standards:

### ACM Documentation Set

For each LRU, the Aircraft Component Manual package includes:

1. **ACM_[LRU_NAME].pdf** - Master component manual
   - Component description and function
   - Operating principles and theory
   - System interfaces and dependencies
   - Performance characteristics and limitations

2. **COMPONENT_BREAKDOWN.pdf** - Detailed component breakdown structure
   - Exploded view diagrams with item numbers
   - Assembly/disassembly sequences
   - Subcomponent identification and relationships
   - Hardware bill of materials (HBOM) with part numbers

3. **MAINTENANCE_MANUAL.pdf** - Maintenance procedures
   - Scheduled maintenance tasks (inspection, lubrication, functional checks)
   - Corrective maintenance procedures
   - Special tools and equipment requirements
   - Maintenance interval schedule
   - Wear limits and replacement criteria

4. **ILLUSTRATED_PARTS_CATALOG.pdf** - Parts identification and ordering
   - Illustrated parts breakdown with nomenclature
   - Manufacturer part numbers and cage codes
   - Interchangeability and substitution data
   - Effectivity and configuration applicability
   - Vendor information and supply chain references

5. **TROUBLESHOOTING_GUIDE.pdf** - Fault isolation and diagnostic procedures
   - Fault symptom tables
   - Diagnostic flowcharts and decision trees
   - Built-in test (BIT) codes and meanings
   - Repair vs. replace decision criteria
   - Return to service criteria

### Subcomponents Directory

Each LRU includes a **SUBCOMPONENTS/** directory containing detailed documentation for individual subassemblies:
- Component-level specifications
- Interface control drawings
- Replacement procedures
- Component-specific testing requirements

### ACM Cross-References

ACM documentation links to:
- **Installation drawings** - Reference to mounting and installation specs
- **Wiring diagrams** - Cross-reference to ATA-92 EWIS documentation
- **System schematics** - Functional diagrams showing LRU in system context
- **Interface Control Documents (ICD)** - Detailed interface specifications
- **Test procedures** - Acceptance test procedures (ATP) and functional test procedures (FTP)

### ACM Version Control

All ACM documents are configuration-controlled:
- Document revision level tracked in header
- Change history documented
- Effectivity tied to LRU part number and serial number applicability
- CCB approval required for changes per [Change Control](#change-control)

## Wing System Architecture

ATA-57 Wings encompasses the following major systems and their associated LRUs:

### Primary Flight Control System (Wings)
- **Aileron System** - Roll control surfaces and actuation
  - Outboard aileron actuators (hydraulic/electric)
  - Inboard aileron actuators (hydraulic/electric)
  - Aileron position feedback sensors
- **Spoiler/Speedbrake System** - Lift dump and speed control
  - Ground spoiler actuators
  - Flight spoiler actuators
  - Spoiler position sensors

### High-Lift System
- **Leading Edge Devices** - Slat system components
  - Slat drive motors and gearboxes
  - Slat track assemblies
  - Slat position sensors (LVDT/RVDT)
  - Slat asymmetry detection
- **Trailing Edge Devices** - Flap system components
  - Flap drive power control units (PCU)
  - Flap transmission assemblies
  - Flap position transmitters
  - Flap load sensors

### Wing Structure & Protection
- **Ice Protection System** - Anti-icing and de-icing
  - Leading edge heating elements
  - Ice detection probes
  - Anti-ice control valves (if pneumatic)
- **Structural Monitoring** - Health monitoring systems
  - Strain gauges
  - Fatigue monitoring sensors
  - Wing deflection sensors

### Wing Integration Items
- **Fuel System Interface** - Wing tank components (see ATA-28)
- **Landing Gear Interface** - Wing-mounted gear components (see ATA-32)
- **Powerplant Interface** - Engine pylon attachments (see ATA-71-80)
- **Electrical Power** - Wing-mounted generators/APU interfaces (see ATA-24)

## Hardware Categories

### Wing-Specific Electronic LRUs
- **Wing Control Computers** - Flight control processing units
- **Slat/Flap Position Sensors** - LVDT/RVDT position transducers
- **Load Sensors** - Strain gauges and load monitoring systems
- **Ice Detection Systems** - Ice detection probes and sensors
- **Angle of Attack Sensors** - AOA vanes and transmitters
- **Wing Tip Devices Controllers** - Winglet/sharklet control interfaces

### Wing-Specific Mechanical LRUs
- **Primary Flight Control Actuators** - Aileron, spoiler actuators
- **High-Lift System Actuators** - Slat and flap drive mechanisms
- **Flap Track Assemblies** - Flap deployment mechanisms
- **Slat Track Assemblies** - Slat extension/retraction mechanisms
- **Wing Tip Fairings** - Aerodynamic wing tip components
- **Access Panels and Doors** - Inspection and maintenance access
- **Structural Fittings** - Wing attachment and load transfer components

### Wing-Specific Electrical LRUs
- **Wing Anti-Ice Heaters** - Leading edge ice protection elements
- **Navigation Lights** - Wing tip position lights
- **Landing/Taxi Lights** - Wing-mounted illumination systems
- **Fuel Quantity Probes** - Wing tank fuel level sensors
- **Lightning Strike Protection** - Static dischargers and bonding
- **Wiring Harnesses** - Wing-specific harness assemblies (reference ATA-92)

## LRU Component Manual Breakdown

Detailed component breakdown for key wing LRUs with ACM linkage:

### Aileron Actuator (LRU_AILERON_ACTUATOR)

**ACM Reference**: `HW_CONFIG/LRU_AILERON_ACTUATOR/ACM/ACM_AILERON_ACTUATOR.pdf`

**Major Subcomponents**:
- **Actuator Motor** - Electro-hydraulic or electric motor assembly
  - Stator assembly with windings
  - Rotor assembly with bearings
  - Feedback resolver/encoder
  - Motor housing and seals
- **Control Valve** - Servo control valve for hydraulic actuators
  - Valve body and spool
  - Solenoid coils
  - Filter assembly
  - Pressure transducers
- **Position Sensor** - LVDT or RVDT position feedback
  - Primary and secondary windings
  - Core assembly
  - Signal conditioning electronics
- **Mounting Brackets** - Structural attachment hardware
  - Upper and lower attachment fittings
  - Bushing assemblies
  - Hardware kit (bolts, washers, lock nuts)

**Related Manuals**:
- Component Maintenance Manual (CMM): Detailed servicing procedures
- Illustrated Parts Catalog (IPC): Parts identification and ordering
- Wiring Diagram Manual (WDM): Reference to ATA-92 for electrical connections

### Flap Drive Unit (LRU_FLAP_DRIVE_UNIT)

**ACM Reference**: `HW_CONFIG/LRU_FLAP_DRIVE_UNIT/ACM/ACM_FLAP_DRIVE_UNIT.pdf`

**Major Subcomponents**:
- **PCU (Power Control Unit)** - Central flap control processor
  - Control electronics module
  - Power distribution unit
  - Built-in test equipment (BITE)
  - Interface connectors
- **Gearbox Assembly** - Mechanical power transmission
  - Input shaft and bearings
  - Gear train (primary and secondary)
  - Output shaft and coupling
  - Lubrication system
- **Transmission Shaft** - Torque transmission between flap stations
  - Flexible couplings
  - Universal joints
  - Shaft sections with splines
  - Support bearings
- **Torque Limiter** - Overload protection device
  - Clutch assembly
  - Shear pin or breakaway coupling
  - Indicator flag for fault detection

**Related Manuals**:
- System Schematic Manual (SSM): Flap system functional diagrams
- Fault Isolation Manual (FIM): Troubleshooting procedures
- Structural Repair Manual (SRM): Interface attachment repairs

### Slat Actuator (LRU_SLAT_ACTUATOR)

**ACM Reference**: `HW_CONFIG/LRU_SLAT_ACTUATOR/ACM/ACM_SLAT_ACTUATOR.pdf`

**Major Subcomponents**:
- **Drive Motor** - Electric motor for slat extension/retraction
  - Brushless DC motor assembly
  - Motor controller electronics
  - Thermal protection sensors
  - Mounting flange
- **Gearbox** - Speed reduction and torque multiplication
  - Planetary gear stages
  - Output gear and coupling
  - Seals and lubrication ports
- **Position Transmitter** - Slat position feedback sensor
  - Synchro or resolver assembly
  - Mounting bracket
  - Signal output connector
- **Track Assembly** - Mechanical guide for slat movement
  - Track beam structure
  - Roller assemblies
  - Wear pads
  - End stops and limit switches

**Related Manuals**:
- Installation Manual: Mounting and rigging procedures
- Test Manual: Functional and operational checks
- Inspection Manual: Visual and NDT inspection criteria

### Spoiler Actuator (LRU_SPOILER_ACTUATOR)

**ACM Reference**: `HW_CONFIG/LRU_SPOILER_ACTUATOR/ACM/ACM_SPOILER_ACTUATOR.pdf`

**Major Subcomponents**:
- **Hydraulic Cylinder** - Linear actuator
  - Cylinder barrel
  - Piston and piston rod
  - End caps and seals
  - Hydraulic ports and fittings
- **Control Valve Assembly** - Servo valve for position control
  - Servo valve body
  - Torque motor
  - Feedback spring
  - Filter screen
- **LVDT Sensor** - Linear position feedback
  - LVDT core attached to piston rod
  - LVDT coil assembly
  - Signal conditioning module
- **Attachment Fittings** - Structural interface hardware
  - Clevis attachments (upper and lower)
  - Spherical bearings
  - Safety locking devices

**Related Manuals**:
- Hydraulic System Manual: Reference to ATA-29 hydraulic interfaces
- Operations Manual: Normal and emergency operation procedures
- Life Limits Manual: Component replacement intervals

### Wing Tip Light (LRU_WING_TIP_LIGHT)

**ACM Reference**: `HW_CONFIG/LRU_WING_TIP_LIGHT/ACM/ACM_WING_TIP_LIGHT.pdf`

**Major Subcomponents**:
- **LED Assembly** - Light emitting diode array
  - LED array board
  - Heat sink
  - Optics/reflector
  - Intensity control circuit
- **Power Supply Module** - Voltage regulation and conditioning
  - AC/DC converter
  - Current limiter
  - Over-voltage protection
  - EMI filter
- **Lens Assembly** - Optical lens and housing
  - Polycarbonate lens
  - Gasket seal
  - Retaining ring
- **Mounting Housing** - Weatherproof enclosure
  - Housing body (cast aluminum)
  - Connector backshell
  - Mounting holes and gasket
  - Drain provisions

**Related Manuals**:
- Lighting System Manual: Reference to ATA-33
- Electrical Load Analysis: Power consumption and circuit protection
- Environmental Qualification Report: DO-160 test results

### Ice Detection Sensor (LRU_ICE_DETECTION)

**ACM Reference**: `HW_CONFIG/LRU_ICE_DETECTION/ACM/ACM_ICE_DETECTION_SENSOR.pdf`

**Major Subcomponents**:
- **Probe Element** - Sensor probe exposed to airstream
  - Sensing tip (magnetostrictive or resonant)
  - Probe body
  - Heater coil for de-icing
  - Mounting threads
- **Signal Processing Unit** - Electronics module
  - Oscillator circuit
  - Frequency detector
  - Amplifier and comparator
  - Output relay/transistor
- **Heater Element** - Anti-icing heater
  - Resistance heating element
  - Thermostat control
  - Power leads
- **Connector Assembly** - Electrical interface
  - Circular connector (MIL-DTL-38999 or equivalent)
  - Contact pins and sockets
  - Backshell and strain relief

**Related Manuals**:
- Ice Protection System Manual: Reference to ATA-30
- Sensor Calibration Manual: Sensitivity adjustment procedures
- Lightning Protection Manual: Bonding and grounding requirements

## Configuration Data Requirements

Each hardware item should document:
- **Identification** - Part number, serial number, nomenclature
- **Specifications** - Technical performance characteristics
- **Interfaces** - Physical, electrical, data connections
- **Installation** - Mounting, routing, adjustment procedures
- **Testing** - Acceptance criteria and test methods
- **Maintenance** - Service intervals, repair procedures

## Change Control

Hardware configuration changes require:
- Engineering Change Request (ECR)
- Impact analysis on interfaces and installation
- CCB approval
- Update to related ICDs and wiring (ATA-92)
- Documentation in CHANGE_LOG

## Wiring Note

⚠️ **Important**: All wiring configurations reside in **ATA-92_EWIS** per EWIS rules. Hardware chapters only reference wiring interfaces.

## References

### Configuration Management
- [Configuration Rules](../../ATA-00_GENERAL/RULES.md)
- [Part Numbering](../../../../00-PROGRAM/CONFIG_MGMT/02-PART_NUMBERING.md)
- [Item Master](../../../../00-PROGRAM/CONFIG_MGMT/08-ITEM_MASTER/)
- [ATA-92 EWIS](../ATA-92_EWIS/) (for wiring)

### Aircraft Component Manuals (ACM)
Each LRU has dedicated ACM documentation in its respective subdirectory:
- `LRU_[NAME]/ACM/ACM_[NAME].pdf` - Master component manual
- `LRU_[NAME]/ACM/COMPONENT_BREAKDOWN.pdf` - Detailed breakdown with exploded views
- `LRU_[NAME]/ACM/MAINTENANCE_MANUAL.pdf` - Maintenance procedures and schedules
- `LRU_[NAME]/ACM/ILLUSTRATED_PARTS_CATALOG.pdf` - Parts identification and ordering
- `LRU_[NAME]/ACM/TROUBLESHOOTING_GUIDE.pdf` - Fault isolation procedures
- `LRU_[NAME]/SUBCOMPONENTS/` - Individual subcomponent documentation

### Related ATA Chapters
- **ATA-24** - Electrical Power (wing-mounted generators/APU interfaces)
- **ATA-27** - Flight Controls (control system interfaces)
- **ATA-28** - Fuel System (wing tank components)
- **ATA-29** - Hydraulic Power (hydraulic actuator supply)
- **ATA-30** - Ice and Rain Protection (anti-ice/de-ice systems)
- **ATA-32** - Landing Gear (wing-mounted gear interfaces)
- **ATA-33** - Lights (navigation and landing lights)
- **ATA-71-80** - Powerplant (engine pylon attachments)
- **ATA-92** - EWIS (all electrical wiring and interconnections)

### Standards and Specifications
- **ATA Spec 2200** - Information Standards for Aviation Maintenance
- **ATA iSpec 2200** - Digital component maintenance manual format
- **S1000D** - International specification for technical publications
- **DO-160** - Environmental Conditions and Test Procedures for Airborne Equipment
- **SAE AS50881** - Wiring Aerospace Vehicle (reference via ATA-92)
- **MIL-STD-1553** - Digital time division command/response multiplex data bus (where applicable)

## Environmental Requirements

Hardware must comply with:
- **DO-160**: Environmental conditions and test procedures
- Temperature ranges and thermal management
- Vibration and shock requirements
- EMI/EMC requirements
- Altitude and pressure requirements

### Wing-Specific Environmental Considerations

**Temperature Extremes**:
- Leading edge de-ice systems: Operating range -55°C to +85°C
- Control surface actuators: -55°C to +71°C ambient
- Wing tip navigation lights: -55°C to +55°C

**Vibration and Shock**:
- Wing flex and flutter conditions per structural analysis
- Engine-induced vibration for wing-mounted engines
- Ground handling loads and impact scenarios

**Altitude and Pressure**:
- Sealed LRU compartments: Pressure differential considerations
- Fuel tank components: Ullage pressure variations
- Control surface seals: Altitude compensation

**Lightning and Static**:
- Wing tip static dischargers: Lightning strike zones 1A, 2A, 3
- Composite material bonding requirements
- Fuel system lightning protection per ATA-28 interface

**Icing Conditions**:
- Ice accretion on sensors and probes
- Leading edge ice protection certification
- De-ice system redundancy requirements

**Contamination**:
- Hydraulic fluid compatibility for actuators
- Fuel system vapor exposure for wing tank sensors
- Corrosion protection for external-mounted hardware

---

**Status**: Active  
**Owner**: Systems Engineering  
**Last Updated**: 2024-01-15
