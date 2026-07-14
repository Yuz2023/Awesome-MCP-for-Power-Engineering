# Awesome MCP for Power Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of [Model Context Protocol (MCP)](https://modelcontextprotocol.io) servers for
> power engineering — power electronics, power systems and the grid, real-time / HIL simulation,
> multiphysics / EM / thermal, motor and machine design, battery / storage / renewables, EDA,
> FPGA / DSP / embedded control, instrumentation, and SCADA / industrial protocols.

MCP lets AI agents (Claude, Codex, Copilot, …) drive the specialized tools engineers already use —
circuit and EMT simulators, FEA solvers, HIL rigs, EDA suites, lab instruments — instead of
re-implementing them. This list tracks what's actually available today.

This page is the **curated pick**: for each tool, the most mature one or two servers plus any
vendor-official one. Every server verified real in the sweep — including all the alternatives we
didn't feature here — is in the **[full verified catalog →](./awesome-mcp-power-engineering-full-catalog.md)**.

*Last verified: 2026-07. Entries checked to exist and to genuinely drive the tool (not doc-only
RAG). The ecosystem moves fast — open a PR (with a source link) if something is out of date.*

## Contents

- [Official](#official) — published or bundled by the software vendor
- [Community](#community)
  - [Power Systems / Grid / EMT](#power-systems--grid--emt)
  - [Power Electronics / Circuit / SPICE](#power-electronics--circuit--spice)
  - [System-Level / Modelica / FMI](#system-level--modelica--fmi)
  - [Electromagnetic / Antenna](#electromagnetic--antenna)
  - [Multiphysics / CAE / FEA](#multiphysics--cae--fea)
  - [Motor / Machines](#motor--machines)
  - [Battery / Storage / PV](#battery--storage--pv)
  - [Wind](#wind)
  - [EDA / PCB / IC](#eda--pcb--ic)
  - [FPGA / HDL Verification](#fpga--hdl-verification)
  - [Embedded / MCU Toolchains](#embedded--mcu-toolchains)
  - [Instrumentation / Test & Measurement](#instrumentation--test--measurement)
  - [SCADA / Industrial Protocols](#scada--industrial-protocols)
  - [Digital Twin / Virtual Commissioning](#digital-twin--virtual-commissioning)
- [APIs available, no MCP yet](#apis-available-no-mcp-yet)
- [Contributing](#contributing)
- [License](#license)

## Official

Published or bundled by the software vendor.

| Software | Vendor | MCP Server |
|---|---|---|
| MATLAB / Simulink (incl. Embedded/HDL Coder) | MathWorks | [matlab/matlab-mcp-server](https://github.com/matlab/matlab-mcp-server) |
| Ansys MAPDL | Ansys | [ansys/pymapdl-mcp](https://github.com/ansys/pymapdl-mcp) |
| Code Composer Studio (C2000 DSP/DSC) | Texas Instruments | Built into CCS IDE (20.5+) |
| SIMBA (power-electronics circuit sim) | AESIM.Tech | [SIMBA Assistant](https://simba.io/news) |
| Device product data (part selection) | Microchip | [Microchip MCP](https://www.microchip.com/en-us/resources/model-context-protocol-server) |
| Test & measurement instruments (SCPI) | Rohde & Schwarz | [Rohde-Schwarz/RsInstrument](https://github.com/Rohde-Schwarz/RsInstrument) |
| ESP-IDF (build/flash/target) | Espressif | [esp-idf-tools MCP (built-in, v6+)](https://developer.espressif.com/blog/2026/04/esp-idf-tools-mcp-server/) |
| WinCC OA (SCADA) | Siemens / ETM | [winccoa/winccoa-ae-js-mcpserver](https://github.com/winccoa/winccoa-ae-js-mcpserver) |
| Ignition (SCADA/MES/HMI) | Inductive Automation | [Ignition MCP Module](https://inductiveautomation.com/news/inductive-automation-announces-mcp-module-during-2025-ignition-community-conference) (EA, GA 2026) |
| EnergyPlus (building energy) | LBNL | [LBNL-ETA/EnergyPlus-MCP](https://github.com/LBNL-ETA/EnergyPlus-MCP) |
| ODE (Modelica IDE) | Orthogonal | [Orthogonalpub/modelica_simulation_mcp_server](https://github.com/Orthogonalpub/modelica_simulation_mcp_server) |
| OpenModelica (OMEdit) | OpenModelica | [in-progress, issue #15385](https://github.com/OpenModelica/OpenModelica/issues/15385) |
| realvirtual.io (Unity virtual commissioning) | realvirtual GmbH | [game4automation/io.realvirtual.mcp](https://github.com/game4automation/io.realvirtual.mcp) |

## Community

Third-party servers, each verified to exist and to drive the tool. Where several exist for one tool,
the most mature one or two are shown; the rest are in the [full catalog](./awesome-mcp-power-engineering-full-catalog.md).

### Power Systems / Grid / EMT

Much of the grid/EMT stack is aggregated in [Power-Agent/PowerMCP](https://github.com/Power-Agent/PowerMCP).

| Software | MCP Server |
|---|---|
| PSS/E · PowerWorld · PowerFactory · PSLF · ANDES · OpenDSS · pandapower | [Power-Agent/PowerMCP](https://github.com/Power-Agent/PowerMCP) |
| PSCAD / EMTDC | [ll0pez20/pscad-mcp](https://github.com/ll0pez20/pscad-mcp) |
| PyPSA | [open-energy-transition/pypsa-mcp](https://github.com/open-energy-transition/pypsa-mcp) |
| OpenDSS (standalone, on PyPI) | [ahmedelshazly27/opendss-mcp-server](https://github.com/ahmedelshazly27/opendss-mcp-server) |

<sub>Also verified: standalone PowerFactory ([Diptargha](https://github.com/Diptargha/mcp-powerfactory)) and pandapower ([Semagram-Energy](https://smithery.ai/server/@Semagram-Energy/pandapower_mcp)) servers — see full catalog.</sub>

### Power Electronics / Circuit / SPICE

| Software | MCP Server |
|---|---|
| LTspice | [Cognitohazard/ltspice-mcp](https://github.com/Cognitohazard/ltspice-mcp) · [xuio/ltspice-mcp](https://github.com/xuio/ltspice-mcp) (macOS GUI + screenshots) |
| ngspice | [gtnoble/ngspice-mcp](https://github.com/gtnoble/ngspice-mcp) |
| QSPICE | [HAbedini/qspice-mcp](https://github.com/kh6570/HAbedini-qspice-mcp) |
| Multi-engine (LTspice/ngspice/QSPICE via spicelib) | [lucasgerads/spicelib-mcp](https://github.com/lucasgerads/spicelib-mcp) |
| PLECS | [haitangccy/plecs-mcp](https://github.com/haitangccy/plecs-mcp) (XML-RPC, 49 tests) |

<sub>Four more LTspice servers + PySpice + a second PLECS server are in the full catalog.</sub>

### System-Level / Modelica / FMI

| Software | MCP Server |
|---|---|
| FMU / FMI (via FMPy) | [Novia-RDI-Seafaring/mcp-fmi](https://github.com/Novia-RDI-Seafaring/mcp-fmi) |
| MWORKS.Sysplorer | [ACupOfHim/mworks-mcp-server](https://github.com/ACupOfHim/mworks-mcp-server) |

<sub>Vendor-official Modelica servers (ODE, OpenModelica) are under [Official](#official).</sub>

### Electromagnetic / Antenna

| Software | MCP Server |
|---|---|
| openEMS (FDTD) | [RFingAdam/mcp-openems](https://github.com/RFingAdam/mcp-openems) |
| NEC2 (wire-antenna MoM) | [RFingAdam/mcp-nec2-antenna](https://github.com/RFingAdam/mcp-nec2-antenna) |
| Ansys Lumerical (FDTD/MODE/INTERCONNECT) | [leisymqaz/lumerical-mcp](https://github.com/leisymqaz/lumerical-mcp) |

### Multiphysics / CAE / FEA

| Software | MCP Server |
|---|---|
| Ansys AEDT (Maxwell/HFSS/Q3D/Icepak) | [LaplaceYoung/ansys-aedt-mcp](https://github.com/LaplaceYoung/ansys-aedt-mcp) |
| Ansys Fluent | [knewnothing/ansys-mcp-server](https://github.com/knewnothing-git/ansys-mcp-server) |
| Ansys Mechanical | [codersag/mechanical-mcp](https://github.com/codersag/mechanical-mcp) |
| COMSOL Multiphysics | [wjc9011/COMSOL_Multiphysics_MCP](https://github.com/wjc9011/COMSOL_Multiphysics_MCP) |
| OpenFOAM | [webworn/openfoam-mcp-server](https://github.com/webworn/openfoam-mcp-server) |
| CST Studio Suite | [RFingAdam/mcp-cst-studio](https://github.com/RFingAdam/mcp-cst-studio) |
| Abaqus/CAE | [jianzhichun/abaqus-mcp-server](https://github.com/jianzhichun/abaqus-mcp-server) |
| FreeCAD FEM + CalculiX | [neka-nat/freecad-mcp](https://github.com/neka-nat/freecad-mcp) |

### Motor / Machines

| Software | MCP Server |
|---|---|
| Motor-current-signature-analysis fault diagnosis | [LGDiMaggio/mcp-motor-current-signature-analysis](https://github.com/LGDiMaggio/mcp-motor-current-signature-analysis) |

<sub>Motor FEA (Motor-CAD, JMAG, Flux, Pyleecan) has no MCP yet — see [gaps](#apis-available-no-mcp-yet).</sub>

### Battery / Storage / PV

| Software | MCP Server |
|---|---|
| Battery electrochemical simulation (PyBaMM) | [BinuShefieldShifani/Batterytwin-mcp](https://github.com/BinuShefieldShifani/Batterytwin-mcp) |
| NREL PVWatts v8 (PV production) | [hoodsy/solar-data-mcp](https://github.com/hoodsy/solar-data-mcp) |
| Residential ESS + inverter (telemetry + charge control) | [michaelkrasa/alpha-ess-mcp-server](https://github.com/michaelkrasa/alpha-ess-mcp-server) |

<sub>More: EG4, Victron, two more PVWatts servers — full catalog. These are device/telemetry-level, not cell design.</sub>

### Wind

| Software | MCP Server |
|---|---|
| QBlade (aeroelastic / BEM / LLFVW) | [JakubRasken/qblade-mcp-server](https://github.com/JakubRasken/qblade-mcp-server) |

### EDA / PCB / IC

| Software | MCP Server |
|---|---|
| KiCad | [lamaalrajih/kicad-mcp](https://github.com/lamaalrajih/kicad-mcp) |
| EasyEDA / JLCPCB | [oaslananka/easyeda-mcp-pro](https://github.com/oaslananka/easyeda-mcp-pro) |
| Altium Designer | [salitronic/eda-agent](https://github.com/salitronic/eda-agent) (290+ tools) · [coffeenmusic/altium-mcp](https://github.com/coffeenmusic/altium-mcp) |
| Yosys / OpenROAD (RTL-to-GDS) | [NellyW8/MCP4EDA](https://github.com/NellyW8/MCP4EDA) · [luarss/openroad-mcp](https://github.com/luarss/openroad-mcp) |
| Cadence Virtuoso | [michelebergo/virtuoso-schematic-mcp](https://github.com/michelebergo/virtuoso-schematic-mcp) |

<sub>Three more Altium servers + a multi-EDA netlist parser are in the full catalog.</sub>

### FPGA / HDL Verification

Toolchains for FPGA-based power controllers and firmware.

| Software | MCP Server |
|---|---|
| AMD Vivado / RapidWright | [Xilinx/fpl26_optimization_contest](https://github.com/Xilinx/fpl26_optimization_contest) (reference example) · [coreyhahn/vivado_mcp](https://github.com/coreyhahn/vivado_mcp) |
| Intel / Altera Quartus | [abbbe/fpga-mcp-servers](https://github.com/abbbe/fpga-mcp-servers) (DE10-Nano) |
| Open-source EDA suite (Yosys/Verible/GTKWave/…) | [ssql2014/mcp4eda](https://github.com/ssql2014/mcp4eda) |
| SystemVerilog static analysis (pyslang) | [ariklapid/pyslang-mcp](https://github.com/ariklapid/pyslang-mcp) |
| Cadence Xcelium | [hslee-cmyk/xcelium-mcp](https://github.com/hslee-cmyk/xcelium-mcp) |

### Embedded / MCU Toolchains

| Software | MCP Server |
|---|---|
| ARM Cortex-M / RISC-V debug (probe-rs) | [adancurusul/embedded-debugger-mcp](https://github.com/adancurusul/embedded-debugger-mcp) |
| STM32 (arm-gcc + OpenOCD/SWD) | [shieldyguy/stm32-mcp](https://github.com/shieldyguy/stm32-mcp) |
| ESP-IDF (community) | [horw/esp-mcp](https://github.com/horw/esp-mcp) |
| PlatformIO (multi-board) | [jl-codes/platformio-mcp](https://github.com/jl-codes/platformio-mcp) |
| GNU GDB (embedded/remote) | [pansila/mcp_server_gdb](https://github.com/pansila/mcp_server_gdb) |
| Serial / UART I/O | [Adancurusul/serial-mcp-server](https://github.com/Adancurusul/serial-mcp-server) |

<sub>Arduino CLI, QEMU, Zephyr/west servers are in the full catalog.</sub>

### Instrumentation / Test & Measurement

| Software | MCP Server |
|---|---|
| Generic VISA / SCPI instruments | [Hizuki1030/visa-mcp](https://github.com/Hizuki1030/visa-mcp) |
| QCoDeS lab-instrument setups | [caidish/instrMCP](https://github.com/caidish/instrMCP) |
| Multi-protocol lab equipment (VISA/SSH/REST/serial) | [techmanual-ai/lablink-mcp](https://github.com/techmanual-ai/lablink-mcp) |

<sub>Vendor-official R&S is under [Official](#official). Dedicated Siglent / Keysight / RIGOL oscilloscope servers are in the full catalog.</sub>

### SCADA / Industrial Protocols

Adjacent to power engineering — substation, plant, and DER field-device access.

| Software | MCP Server |
|---|---|
| OPC UA | [kukapay/opcua-mcp](https://github.com/kukapay/opcua-mcp) |
| Modbus (TCP/RTU, master + slave) | [alejoseb/ModbusMCP](https://github.com/alejoseb/ModbusMCP) |
| Ignition (community) | [WhiskeyHouse/ignition-mcp](https://github.com/WhiskeyHouse/ignition-mcp) |
| Siemens TIA Portal | [feelautom/tia-copilot-genai-bridge](https://github.com/feelautom/tia-copilot-genai-bridge) (commercial) |
| Siemens WinCC Unified | [vogler75/winccua-mcp-server](https://github.com/vogler75/winccua-mcp-server) |
| B&R Automation Studio | [AndrewMusser/br-automation-mcp](https://github.com/AndrewMusser/br-automation-mcp) |

<sub>Three more OPC UA and three more Modbus servers are in the full catalog.</sub>

### Digital Twin / Virtual Commissioning

| Software | MCP Server |
|---|---|
| Vector CANoe (bus simulation / HIL-adjacent) | [VectorCANoe/CANoe-mcp](https://github.com/VectorCANoe/CANoe-mcp) |

<sub>Vendor-official realvirtual.io (Unity) is under [Official](#official).</sub>

## APIs available, no MCP yet

Tools with a documented automation API (Python/COM/Tcl/scripting) but **no known MCP server** —
**open for you to claim**. Want to build one? Open an issue at
[Yuz2023/PE-MCP](https://github.com/Yuz2023/PE-MCP/issues) to call dibs and coordinate, so two people
don't build the same server twice. When it's live, send a PR to move it up into the list.

- **Real-time / HIL** (an entirely blank class — high-value): OPAL-RT / RT-LAB / HYPERSIM, Typhoon HIL, dSPACE (SCALEXIO/VEOS), RTDS / RSCAD FX, NI VeriStand, Speedgoat, Plexim RT Box, imperix
- **Substation & protection** (confirmed zero MCP): IEC 61850 / GOOSE / MMS, DNP3, protection relays / IEDs (SEL, ABB Relion, Siemens SIPROTEC, GE Multilin)
- **Wide-area measurement** (confirmed zero MCP): PMU / synchrophasor, C37.118, openPDC
- **Motor / magnetics FEA:** Ansys Motor-CAD (PyMotorCAD), JMAG-Designer, Altair Flux/FluxMotor (PyFlux), FEMM (pyFEMM), Pyleecan
- **Offline circuit:** PLECS *(has community servers above; no official)*, PSIM, Saber, SIMetrix/SIMPLIS, GeckoCIRCUITS
- **Thermal / power-device** (no *driving* MCP — Cantera only has docs-RAG): Flotherm/FloEFD, Ansys Sherlock, SiC/GaN device modeling
- **FPGA / DSP toolchains (CLI-scriptable):** Lattice Radiant/Diamond, Microchip Libero, Microchip MPLAB (native build/debug), NXP MCUXpresso, ADI CrossCore/SHARC (CCES), NI LabVIEW FPGA (target-aware compile)
- **Grid (additional):** GridLAB-D, GridCal, MATPOWER, PowerModels.jl, EMTP-RV, ETAP, DPsim

## Contributing

Contributions welcome! Please open a PR that:

1. Adds the entry to the right section, keeping tables tidy.
2. Includes a **working link** to the MCP server (repo or vendor page).
3. Notes whether it is **official** (vendor-published) or **community**.
4. Confirms it genuinely drives the tool over MCP (not a docs-only / RAG server).

Entries that can't be verified, or that are pure API wrappers / doc-retrieval with no tool-driving
MCP surface, belong in the [full catalog](./awesome-mcp-power-engineering-full-catalog.md) with a note, not here.

**Want to build a server for one of the gaps?** Open an issue at
[Yuz2023/PE-MCP](https://github.com/Yuz2023/PE-MCP/issues) to claim it first — it keeps two people
from building the same thing, and you'll get a hand from others working on the same class of tool.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, contributors have waived all copyright and related rights to this
work.
