# LRU: Ice Detection Sensor

## Overview

Ice detection sensors monitor ice accretion on wing surfaces to trigger anti-icing and de-icing systems. This directory contains complete documentation for ice detection sensor LRUs including specifications, installation procedures, maintenance manuals, and component breakdowns.

## Contents

### Top-Level Documents
- **SPECIFICATIONS.pdf** - Technical specifications and performance characteristics
- **PART_NUMBERS.csv** - Part numbers, variants, and interchangeability data
- **INSTALLATION.pdf** - Installation procedures and mounting requirements
- **TEST_PROCEDURES.pdf** - Acceptance testing and functional verification

### ACM/ - Aircraft Component Manuals
- **ACM_ICE_DETECTION_SENSOR.pdf** - Master component manual with complete system description
- **COMPONENT_BREAKDOWN.pdf** - Exploded views and assembly diagrams
- **MAINTENANCE_MANUAL.pdf** - Maintenance tasks, schedules, and procedures
- **ILLUSTRATED_PARTS_CATALOG.pdf** - Parts identification and ordering information
- **TROUBLESHOOTING_GUIDE.pdf** - Fault isolation and diagnostic procedures

### SUBCOMPONENTS/ - Subassembly Documentation
- **PROBE_ELEMENT.pdf** - Sensor probe exposed to airstream
- **SIGNAL_PROCESSING_UNIT.pdf** - Electronics module
- **HEATER_ELEMENT.pdf** - Anti-icing heater
- **CONNECTOR_ASSEMBLY.pdf** - Electrical interface

## Technical Summary

**Function**: Ice accretion detection and monitoring
**Type**: Magnetostrictive or resonant frequency sensor
**Location**: Wing leading edge
**Interfaces**: ATA-30 Ice/Rain Protection, ATA-24 Electrical Power, ATA-92 EWIS

## References

- See [HW_CONFIG README](../README.md) for complete hardware configuration guidelines
- See [ATA-30 Ice Protection](../../ATA-30_ICE_RAIN_PROTECTION/) for ice protection system integration
- See [ATA-92 EWIS](../../ATA-92_EWIS/) for wiring interfaces
