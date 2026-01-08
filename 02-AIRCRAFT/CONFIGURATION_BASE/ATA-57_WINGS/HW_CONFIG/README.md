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
│   └── TEST_PROCEDURES.pdf
├── LRU_FLAP_DRIVE_UNIT/        # Flap extension/retraction systems
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   └── TEST_PROCEDURES.pdf
├── LRU_SLAT_ACTUATOR/          # Slat control actuators
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   └── TEST_PROCEDURES.pdf
├── LRU_SPOILER_ACTUATOR/       # Spoiler panel actuators
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   └── TEST_PROCEDURES.pdf
├── LRU_WING_TIP_LIGHT/         # Navigation and position lights
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   └── TEST_PROCEDURES.pdf
├── LRU_ICE_DETECTION/          # Ice protection sensors
│   ├── SPECIFICATIONS.pdf
│   ├── PART_NUMBERS.csv
│   ├── INSTALLATION.pdf
│   └── TEST_PROCEDURES.pdf
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

- [Configuration Rules](../../ATA-00_GENERAL/RULES.md)
- [Part Numbering](../../../../00-PROGRAM/CONFIG_MGMT/02-PART_NUMBERING.md)
- [Item Master](../../../../00-PROGRAM/CONFIG_MGMT/08-ITEM_MASTER/)
- [ATA-92 EWIS](../ATA-92_EWIS/) (for wiring)

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
