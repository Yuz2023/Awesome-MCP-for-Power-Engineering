# Awesome MCP for Power Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of [Model Context Protocol (MCP)](https://modelcontextprotocol.io) servers for
> power engineering — power electronics, power systems and the grid, real-time / HIL simulation,
> multiphysics / EM / thermal, motor and machine design, battery / storage / renewables, EDA,
> FPGA / DSP / embedded control, instrumentation, and SCADA / industrial protocols.

MCP lets AI agents (Claude, Codex, Copilot, …) interact with specialized engineering tools —
circuit and EMT simulators, FEA solvers, EDA suites, lab instruments, and industrial software —
instead of re-implementing them. This list tracks publicly documented implementations.

This page is a curated selection of public implementations. The
**[extended catalog →](./awesome-mcp-power-engineering-full-catalog.md)** records additional
alternatives without claiming that every project has been installed or tested against licensed
software or hardware.

*Last reviewed: 2026-07-16. Public repositories were `Source-inspected` where available; first-party
documentation was reviewed otherwise. A `Source-inspected` entry is not a simulator-runtime,
target, instrument, or hardware validation. The ecosystem moves quickly; please open an issue or
pull request with a public source when an entry changes.*

## Contents

- [How to read the tables](#how-to-read-the-tables)
- [Core power engineering](#core-power-engineering)
  - [Power systems / grid / EMT](#power-systems--grid--emt)
  - [Power electronics / circuit / SPICE](#power-electronics--circuit--spice)
  - [System-level modeling / Modelica / FMI](#system-level-modeling--modelica--fmi)
  - [Real-time / HIL simulation](#real-time--hil-simulation)
  - [Motor condition monitoring / diagnostics](#motor-condition-monitoring--diagnostics)
  - [Battery / storage / PV](#battery--storage--pv)
  - [Wind](#wind)
  - [Instrumentation / test and measurement](#instrumentation--test-and-measurement)
- [Adjacent and enabling engineering tools](#adjacent-and-enabling-engineering-tools)
  - [SCADA / PLC / industrial automation and protocols](#scada--plc--industrial-automation-and-protocols)
  - [Multiphysics / CAE / FEA](#multiphysics--cae--fea)
  - [Electromagnetic / antenna / photonics](#electromagnetic--antenna--photonics)
  - [PCB / ECAD](#pcb--ecad)
  - [IC / ASIC EDA](#ic--asic-eda)
  - [FPGA / HDL verification](#fpga--hdl-verification)
  - [Embedded controller toolchains](#embedded-controller-toolchains)
  - [Bus / network simulation and test](#bus--network-simulation-and-test)
  - [Digital twin / virtual commissioning](#digital-twin--virtual-commissioning)
  - [Engineering data / component selection](#engineering-data--component-selection)
  - [Building / energy-system modeling](#building--energy-system-modeling)
- [Public implementation gaps](#public-implementation-gaps)
- [Contributing](#contributing)
- [Citation](#citation)
- [License](#license)

## How to read the tables

The columns deliberately separate facts that are often conflated:

- **Publisher:** `First-party` is published by the vendor; `Project steward` is published by the
  official upstream project maintainer; `Institutional` is published by a research institution;
  and `Community` is third-party.
- **Availability:** `Available`, `Unassessed`, `Alpha`, `Early Access`, `Experimental`, or
  `Reference`. This reports the publisher's status when established; `Unassessed` means the latest
  review did not establish one. Availability is separate from validation.
- **Access:** whether source is publicly available, or the server is bundled, hosted, or tied to
  commercial software. `Source available` makes no claim about the project's license.
- **Validation:** `Repository-checked`, `Vendor-documented`, `Source-inspected`, `Mock-tested`, or a
  stronger runtime level when direct evidence is available. No entry implies hardware validation
  unless it says so.

Projects that only search documentation are kept out of the curated tables.

## Core power engineering

### Power systems / grid / EMT

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Multi-engine grid studies: PSS/E, PowerWorld, PowerFactory, PSLF, ANDES, OpenDSS, pandapower, PSCAD, PyPSA, Egret, HOPE, LTspice, surge | [Power-Agent/PowerMCP](https://github.com/Power-Agent/PowerMCP) | Community | Alpha | Source available; vendor products may be required | Source-inspected |
| PyPSA | [open-energy-transition/pypsa-mcp](https://github.com/open-energy-transition/pypsa-mcp) | Community | Unassessed | Source available | Source-inspected |
| OpenDSS | [ahmedelshazly27/opendss-mcp-server](https://github.com/ahmedelshazly27/opendss-mcp-server) | Community | Unassessed | Source available | Source-inspected |
| DIgSILENT PowerFactory | [Diptargha/mcp-powerfactory](https://github.com/Diptargha/mcp-powerfactory) | Community | Unassessed | Source available; PowerFactory required | Source-inspected |

### Power electronics / circuit / SPICE

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| SIMBA | [SIMBA Assistant (embedded MCP server)](https://doc.simba.io/version_history/26_03/) | First-party · AESIM.Tech / Powersys | Available (SIMBA 26.03+) | Optional commercial add-on (SIMBA Assistant module); MCP server embedded, not standalone | Vendor-documented |
| LTspice | [Cognitohazard/ltspice-mcp](https://github.com/Cognitohazard/ltspice-mcp) · [xuio/ltspice-mcp](https://github.com/xuio/ltspice-mcp) | Community | Unassessed | Source available; LTspice required | Source-inspected |
| ngspice | [gtnoble/ngspice-mcp](https://github.com/gtnoble/ngspice-mcp) · [Cognitohazard/ltspice-mcp](https://github.com/Cognitohazard/ltspice-mcp) | Community | Unassessed | Source available | Source-inspected |
| QSPICE | [kh6570/HAbedini-qspice-mcp](https://github.com/kh6570/HAbedini-qspice-mcp) | Community | Unassessed | Source available; QSPICE required | Source-inspected |
| LTspice / ngspice / QSPICE via spicelib | [lucasgerads/spicelib-mcp](https://github.com/lucasgerads/spicelib-mcp) | Community | Unassessed | Source available; selected simulator required | Source-inspected |
| PLECS | [haitangccy/plecs-mcp](https://github.com/haitangccy/plecs-mcp) | Community | Unassessed | Source available; PLECS required | Mock-tested; no live PLECS evidence recorded here |
| PSIM | [zongseung/psim-mcp](https://github.com/zongseung/psim-mcp) | Community | Unassessed | Source available; PSIM required (mock adapter for development without PSIM) | Source-inspected |

### System-level modeling / Modelica / FMI

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| MATLAB | [matlab/matlab-mcp-server](https://github.com/matlab/matlab-mcp-server) | First-party · MathWorks | Available | Source available under MathWorks license terms; MATLAB required | Source-inspected and Vendor-documented |
| Simulink Agentic Toolkit used with MATLAB MCP Server | [toolkit](https://github.com/matlab/simulink-agentic-toolkit) · [MATLAB MCP Server](https://github.com/matlab/matlab-mcp-server) | First-party · MathWorks | Available | Source available under MathWorks license terms; required MathWorks products | Source-inspected and Vendor-documented |
| ODE Modelica IDE | [Orthogonalpub/modelica_simulation_mcp_server](https://github.com/Orthogonalpub/modelica_simulation_mcp_server) | First-party · Orthogonal Supersystems | Available | Hosted; token required | Source-inspected |
| OpenModelica / OMEdit | [built-in experimental MCP server](https://github.com/OpenModelica/OpenModelica/blob/master/OMEdit/OMEditLIB/MCP/README.md) | Project steward · OSMC | Experimental (OpenModelica 1.27.0; disabled by default) | Bundled | Source-inspected and Vendor-documented |
| FMU / FMI via FMPy | [Novia-RDI-Seafaring/mcp-fmi](https://github.com/Novia-RDI-Seafaring/mcp-fmi) | Community | Unassessed | Source available | Source-inspected |
| MWORKS.Sysplorer | [ACupOfHim/mworks-mcp-server](https://github.com/ACupOfHim/mworks-mcp-server) | Community | Unassessed | Source available; Sysplorer required | Source-inspected |

### Real-time / HIL simulation

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| dSPACE VEOS | [dspace-group/VeosMCP](https://github.com/dspace-group/VeosMCP) | First-party · dSPACE | Alpha (v0.1.0-rc) | Source available; VEOS required | Source-inspected |

VEOS is the PC-based (offline / SIL) member of the dSPACE toolchain. Direct MCP integrations for
real-time targets (SCALEXIO, OPAL-RT, Typhoon HIL, RTDS, …) remain open — see
[Public implementation gaps](#public-implementation-gaps).

### Motor condition monitoring / diagnostics

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Motor-current-signature-analysis fault diagnosis | [LGDiMaggio/mcp-motor-current-signature-analysis](https://github.com/LGDiMaggio/mcp-motor-current-signature-analysis) | Community | Unassessed | Source available | Source-inspected |

### Battery / storage / PV

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Battery electrochemical simulation via PyBaMM | [BinuShefieldShifani/Batterytwin-mcp](https://github.com/BinuShefieldShifani/Batterytwin-mcp) | Community | Unassessed | Source available | Source-inspected |
| NREL PVWatts v8 | [hoodsy/solar-data-mcp](https://github.com/hoodsy/solar-data-mcp) | Community | Unassessed | Source available; external API | Source-inspected |
| Alpha ESS inverter and storage telemetry/control | [michaelkrasa/alpha-ess-mcp-server](https://github.com/michaelkrasa/alpha-ess-mcp-server) | Community | Unassessed | Source available; device/API credentials required | Source-inspected; no device validation recorded here |

### Wind

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| QBlade aeroelastic / BEM / LLFVW | [JakubRasken/qblade-mcp-server](https://github.com/JakubRasken/qblade-mcp-server) | Community | Experimental | Source available; QBlade required | Source-inspected |

### Instrumentation / test and measurement

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Rohde & Schwarz SCPI instruments | [RsInstrument MCP Server](https://rsinstrument.readthedocs.io/en/latest/StepByStepGuide.html#mcp-server) | First-party · Rohde & Schwarz | Available (RsInstrument 1.120.0+) | Source available package; instruments required | Source-inspected and Vendor-documented |
| Generic VISA / SCPI instruments | [Hizuki1030/visa-mcp](https://github.com/Hizuki1030/visa-mcp) | Community | Unassessed | Source available; VISA backend/instrument required | Source-inspected |
| QCoDeS instrument setups | [caidish/instrMCP](https://github.com/caidish/instrMCP) | Community | Unassessed | Source available; safe mode by default; instruments required | Source-inspected |
| VISA / SSH / REST / serial equipment | [techmanual-ai/lablink-mcp](https://github.com/techmanual-ai/lablink-mcp) | Community | Unassessed | Source available; equipment required | Source-inspected |

## Adjacent and enabling engineering tools

These projects support power-engineering workflows but are not all power-domain-specific.

### SCADA / PLC / industrial automation and protocols

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| WinCC OA | [winccoa/winccoa-ae-js-mcpserver](https://github.com/winccoa/winccoa-ae-js-mcpserver) | First-party · Siemens / ETM | Available | Source available; WinCC OA required | Source-inspected and Vendor-documented |
| Ignition | [Ignition MCP Module](https://forum.inductiveautomation.com/t/mcp-module-early-access/113966/22) | First-party · Inductive Automation | Early Access; full release planned for February 2027 | Commercial infrastructure module; no first-party primitives | Vendor-documented |
| Ignition Gateway API | [WhiskeyHouse/ignition-mcp](https://github.com/WhiskeyHouse/ignition-mcp) | Community | Unassessed | Source available; Ignition required | Source-inspected |
| OPC UA | [kukapay/opcua-mcp](https://github.com/kukapay/opcua-mcp) | Community | Unassessed | Source available; OPC UA endpoint required | Source-inspected |
| Modbus TCP/RTU master and slave | [alejoseb/ModbusMCP](https://github.com/alejoseb/ModbusMCP) | Community | Unassessed | Source available; endpoint required | Source-inspected |
| Siemens TIA Portal | [feelautom/tia-copilot-genai-bridge](https://github.com/feelautom/tia-copilot-genai-bridge) | Community · feelautom | Available | Commercial; public blueprint with proprietary driver | Source-inspected; proprietary core not validated |
| Siemens WinCC Unified | [vogler75/winccua-mcp-server](https://github.com/vogler75/winccua-mcp-server) | Community | Unassessed | Source available; WinCC Unified required | Source-inspected |
| B&R Automation Studio | [AndrewMusser/br-automation-mcp](https://github.com/AndrewMusser/br-automation-mcp) | Community | Unassessed | Source available; Automation Studio required | Source-inspected |

### Multiphysics / CAE / FEA

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Ansys Mechanical APDL | [ansys/pymapdl-mcp](https://github.com/ansys/pymapdl-mcp) | First-party · Ansys | Available | Source available; MAPDL required | Source-inspected and Vendor-documented |
| Ansys AEDT: Maxwell / HFSS / Q3D / Icepak | [ansys/pyaedt-mcp](https://github.com/ansys/pyaedt-mcp) | First-party · Ansys | Alpha (v0.1.0) | Source available; AEDT required | Source-inspected |
| Ansys AEDT: Maxwell / HFSS / Q3D / Icepak | [LaplaceYoung/ansys-aedt-mcp](https://github.com/LaplaceYoung/ansys-aedt-mcp) | Community | Unassessed | Source available; AEDT required | Source-inspected |
| Ansys Fluent | [ansys/pyfluent-mcp](https://github.com/ansys/pyfluent-mcp) | First-party · Ansys | Alpha (v0.1.0) | Source available; Fluent required | Source-inspected |
| Ansys Fluent | [knewnothing-git/ansys-mcp-server](https://github.com/knewnothing-git/ansys-mcp-server) | Community | Unassessed | Source available; Fluent required | Source-inspected |
| Ansys Mechanical | [ansys/pymechanical-mcp](https://github.com/ansys/pymechanical-mcp) | First-party · Ansys | Alpha (v0.1.1) | Source available; Mechanical required | Source-inspected |
| Ansys Mechanical | [codersag/mechanical-mcp](https://github.com/codersag/mechanical-mcp) | Community | Unassessed | Source available; Mechanical required | Source-inspected |
| COMSOL Multiphysics | [wjc9011/COMSOL_Multiphysics_MCP](https://github.com/wjc9011/COMSOL_Multiphysics_MCP) | Community | Unassessed | Source available; COMSOL required | Source-inspected |
| OpenFOAM | [webworn/openfoam-mcp-server](https://github.com/webworn/openfoam-mcp-server) | Community | Experimental | Source available | Source-inspected; project reports partial and incomplete solver coverage |
| CST Studio Suite | [RFingAdam/mcp-cst-studio](https://github.com/RFingAdam/mcp-cst-studio) | Community | Unassessed | Source available; CST required | Source-inspected |
| Abaqus/CAE | [jianzhichun/abaqus-mcp-server](https://github.com/jianzhichun/abaqus-mcp-server) | Community | Unassessed | Source available; Abaqus required | Source-inspected |
| FreeCAD FEM / CalculiX | [neka-nat/freecad-mcp](https://github.com/neka-nat/freecad-mcp) | Community | Unassessed | Source available | Source-inspected |

### Electromagnetic / antenna / photonics

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| openEMS FDTD | [RFingAdam/mcp-openems](https://github.com/RFingAdam/mcp-openems) | Community | Unassessed | Source available | Source-inspected |
| NEC2 wire-antenna MoM | [RFingAdam/mcp-nec2-antenna](https://github.com/RFingAdam/mcp-nec2-antenna) | Community | Unassessed | Source available | Source-inspected |
| Ansys Lumerical FDTD / MODE / INTERCONNECT | [ansys/pylumerical-mcp](https://github.com/ansys/pylumerical-mcp) | First-party · Ansys | Alpha (v0.1.0) | Source available; Lumerical required | Source-inspected |
| Ansys Lumerical FDTD / MODE / INTERCONNECT | [leisymqaz/lumerical-mcp](https://github.com/leisymqaz/lumerical-mcp) | Community | Experimental | Source available; Lumerical required | Source-inspected |

### PCB / ECAD

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| KiCad | [lamaalrajih/kicad-mcp](https://github.com/lamaalrajih/kicad-mcp) | Community | Unassessed | Source available | Source-inspected |
| EasyEDA / JLCPCB | [oaslananka/easyeda-mcp-pro](https://github.com/oaslananka/easyeda-mcp-pro) | Community | Unassessed | Source available; external services may be required | Source-inspected |
| Altium Designer | [salitronic/eda-agent](https://github.com/salitronic/eda-agent) | Community | Experimental | Source available; Altium required | Source-inspected; no independent runtime validation |
| Altium Designer | [coffeenmusic/altium-mcp](https://github.com/coffeenmusic/altium-mcp) | Community | Unassessed | Source available; Altium required | Source-inspected |

### IC / ASIC EDA

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| OpenROAD / OpenROAD-flow-scripts | [The-OpenROAD-Project/OpenROAD-MCP](https://github.com/The-OpenROAD-Project/OpenROAD-MCP) | Project steward · OpenROAD Project | Available | Source available | Source-inspected |
| Yosys / OpenROAD workflows | [NellyW8/MCP4EDA](https://github.com/NellyW8/MCP4EDA) | Community | Unassessed | Source available | Source-inspected |
| Cadence Virtuoso | [michelebergo/virtuoso-schematic-mcp](https://github.com/michelebergo/virtuoso-schematic-mcp) | Community | Unassessed | Source available; Virtuoso required | Source-inspected |

### FPGA / HDL verification

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| AMD Vivado / RapidWright | [Xilinx/fpl26_optimization_contest](https://github.com/Xilinx/fpl26_optimization_contest) | First-party · AMD/Xilinx | Reference | Source available contest example; tool licenses may be required | Source-inspected |
| AMD Vivado | [coreyhahn/vivado_mcp](https://github.com/coreyhahn/vivado_mcp) | Community | Unassessed | Source available; Vivado required | Source-inspected |
| Intel / Altera Quartus | [abbbe/fpga-mcp-servers](https://github.com/abbbe/fpga-mcp-servers) | Community | Unassessed | Source available; Quartus required | Source-inspected |
| Yosys / Verible / GTKWave and related tools | [ssql2014/mcp4eda](https://github.com/ssql2014/mcp4eda) | Community | Unassessed | Source available | Source-inspected |
| SystemVerilog static analysis via pyslang | [ariklapid/pyslang-mcp](https://github.com/ariklapid/pyslang-mcp) | Community | Unassessed | Source available | Source-inspected |
| Cadence Xcelium | [hslee-cmyk/xcelium-mcp](https://github.com/hslee-cmyk/xcelium-mcp) | Community | Experimental | Source available; Xcelium required | Source-inspected |

### Embedded controller toolchains

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| CCStudio project and debug servers | [TI MCP documentation](https://software-dl.ti.com/ccs/esd/documents/application_notes/appnote-ccs_ai_code_assistant.html) | First-party · Texas Instruments | Available (CCStudio 20.5.x+) | Bundled | Vendor-documented |
| ESP-IDF build / flash / target tools | [ESP-IDF Tools Local MCP Server](https://developer.espressif.com/blog/2026/04/esp-idf-tools-mcp-server/) | First-party · Espressif | Available (ESP-IDF 6.0+) | Bundled; opt-in `mcp` feature selected at install (EIM 0.8.1+) | Vendor-documented |
| ESP-IDF | [horw/esp-mcp](https://github.com/horw/esp-mcp) | Community | Unassessed | Source available; ESP-IDF required | Source-inspected |
| ARM Cortex-M / RISC-V debugging via probe-rs | [adancurusul/embedded-debugger-mcp](https://github.com/adancurusul/embedded-debugger-mcp) | Community | Unassessed | Source available; target hardware optional | Source-inspected |
| STM32 via arm-gcc and OpenOCD/SWD | [shieldyguy/stm32-mcp](https://github.com/shieldyguy/stm32-mcp) | Community | Unassessed | Source available; target/toolchain required | Source-inspected |
| PlatformIO | [jl-codes/platformio-mcp](https://github.com/jl-codes/platformio-mcp) | Community | Unassessed | Source available | Source-inspected |
| GNU GDB | [pansila/mcp_server_gdb](https://github.com/pansila/mcp_server_gdb) | Community | Unassessed | Source available | Source-inspected |
| Serial / UART I/O | [Adancurusul/serial-mcp-server](https://github.com/Adancurusul/serial-mcp-server) | Community | Unassessed | Source available; device required | Source-inspected |

### Bus / network simulation and test

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Vector CANoe configuration, CAPL, measurement and tests | [VectorCANoe/CANoe-mcp](https://github.com/VectorCANoe/CANoe-mcp) | Community | Unassessed | Source available; CANoe required | Source-inspected; no hardware validation recorded here |

### Digital twin / virtual commissioning

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| realvirtual.io / Unity | [Python MCP server](https://github.com/game4automation/realvirtual-MCP) · [Unity package](https://github.com/game4automation/io.realvirtual.mcp) | First-party · realvirtual GmbH | Available | Source available; Unity/realvirtual environment required | Source-inspected |

### Engineering data / component selection

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Microchip device selection and supply-chain data | [Microchip MCP Server](https://www.microchip.com/en-us/resources/model-context-protocol-server) | First-party · Microchip | Available | Public hosted endpoint (`api.microchip.com/mcp/resources`) | Vendor-documented |

### Building / energy-system modeling

| Software | MCP server | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| EnergyPlus building-energy simulation | [LBNL-ETA/EnergyPlus-MCP](https://github.com/LBNL-ETA/EnergyPlus-MCP) | Institutional · LBNL research team | Unassessed (package version 0.1.0) | Source available | Source-inspected |

## Public implementation gaps

The documented public search did not find a qualifying, publicly accessible, tool-specific MCP for
the items below as of **2026-07-16**. This is a search result, not proof that no implementation
exists. Generic protocol bridges, indirect control paths, documentation-only servers, and
unimplemented scaffolds are not counted as direct tool integrations. Two items graduated from this
section on 2026-07-16: dSPACE VEOS ([dspace-group/VeosMCP](https://github.com/dspace-group/VeosMCP))
and PSIM ([zongseung/psim-mcp](https://github.com/zongseung/psim-mcp)).

- **Direct real-time / HIL integrations:** OPAL-RT / RT-LAB / HYPERSIM, Typhoon HIL, dSPACE
  SCALEXIO / ControlDesk, RTDS / RSCAD FX, NI VeriStand, Speedgoat, Plexim RT Box, and imperix.
  dSPACE VEOS — the PC-based, non-real-time member of this family — is now covered (see
  [Real-time / HIL simulation](#real-time--hil-simulation)); every real-time target remains open.
  Some tools may be reachable indirectly through MATLAB, OPC UA, or another general integration.
- **Substation protocols and protection devices:** IEC 61850 / GOOSE / MMS, DNP3, and device-family
  integrations for SEL, ABB Relion, Siemens SIPROTEC, and GE Multilin.
- **Wide-area measurement:** PMU / synchrophasor workflows, IEEE C37.118, and openPDC.
- **Motor and magnetics FEA:** Ansys Motor-CAD, JMAG-Designer, Altair Flux / FluxMotor, FEMM, and
  Pyleecan.
- **Additional offline circuit tools:** Saber, SIMetrix / SIMPLIS, and GeckoCIRCUITS. (PSIM is now
  covered — see [Power electronics / circuit / SPICE](#power-electronics--circuit--spice).)
- **Thermal and power-device engineering:** Flotherm / FloEFD, Ansys Sherlock, and dedicated SiC /
  GaN device-modeling workflows.
- **Additional FPGA / DSP toolchains:** Lattice Radiant / Diamond, Microchip Libero and MPLAB,
  NXP MCUXpresso, ADI CrossCore / SHARC, and target-aware LabVIEW FPGA compilation.
- **Additional grid tools:** GridLAB-D, VeraGrid (formerly GridCal), MATPOWER, PowerModels.jl,
  EMTP-RV, ETAP, and DPsim.

Want to propose an implementation or correct a gap? [Open an issue in this repository](https://github.com/Yuz2023/Awesome-MCP-for-Power-Engineering/issues/new)
with a public source and the validation level you can substantiate.

## Contributing

Contributions are welcome. Please read the [contribution guidelines](contributing.md) first. Add an
entry to the appropriate domain, provide a working public source, and report publisher,
availability, access, and validation separately. Source inspection does not count as licensed
software, simulator-runtime, instrument, target, or hardware validation.

## Citation

If this list is useful in your research or work, please cite it:

> Yuzhuo Li. *Awesome MCP for Power Engineering.* 2026.
> https://github.com/Yuz2023/Awesome-MCP-for-Power-Engineering

```bibtex
@misc{li2026awesomemcppe,
  author       = {Li, Yuzhuo},
  title        = {Awesome MCP for Power Engineering},
  year         = {2026},
  howpublished = {\url{https://github.com/Yuz2023/Awesome-MCP-for-Power-Engineering}}
}
```

## License

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

© 2026 Yuzhuo Li and contributors. This list is licensed under [CC BY 4.0](LICENSE) — you are free to
share and adapt it, including commercially, as long as you give appropriate credit (see
[Citation](#citation)).
