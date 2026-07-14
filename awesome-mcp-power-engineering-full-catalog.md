# Extended MCP Catalog for Power Engineering

> This supplement records a broader set of publicly accessible MCP implementations relevant to power
> engineering and adjacent engineering workflows. Return to the [curated main list](./README.md).

Entries are classified from public repositories, first-party documentation, or official
announcements. `Repository-checked` means that the public endpoint and repository description were
reviewed; it does not imply successful installation, simulator execution, licensed-software
validation, instrument/target access, or hardware validation. `Unassessed` means that maturity was
not re-established during the latest review.

*Last reviewed: 2026-07-14.*

Field values are intentionally conservative: `First-party`, `Project steward`,
`Institutional`, and `Community` describe provenance; availability is reported separately;
`Source available` describes access, not maturity. See the [main list](./README.md#how-to-read-the-tables)
for the validation vocabulary.


## Power Systems / Grid

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| DIgSILENT PowerFactory | https://github.com/Diptargha/mcp-powerfactory | Community | Unassessed | Source available | Repository-checked |
| DIgSILENT PowerFactory | https://github.com/ShuailongDai/Initial-PowerFactory-MCP-automation | Community | Unassessed | Source available | Repository-checked |
| OpenDSS | https://github.com/ahmedelshazly27/opendss-mcp-server | Community | Unassessed | Source available | Repository-checked |

## Power Electronics / Circuit

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| LTspice | https://github.com/xuio/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/daviditkin/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/HarshyChoc/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/BrosnanYuen/ltspice_mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/Janadasroor/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| SPICE via spicelib | https://github.com/lucasgerads/spicelib-mcp | Community | Unassessed | Source available | Repository-checked |
| PLECS | https://github.com/yingriyanlong/plecs-mcp | Community | Unassessed | Source available | Repository-checked |
| PLECS | https://github.com/haitangccy/plecs-mcp | Community | Unassessed | Source available | Mock-tested; no live PLECS evidence recorded here |

## System-Level / Modelica / FMI

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| MWORKS.Sysplorer | https://github.com/ACupOfHim/mworks-mcp-server | Community | Unassessed | Source available | Repository-checked |
| FMU / FMI | https://github.com/Novia-RDI-Seafaring/mcp-fmi | Community | Unassessed | Source available | Repository-checked |
| Modelica / ODE IDE | https://github.com/Orthogonalpub/modelica_simulation_mcp_server | First-party | Available | Hosted service; source available | Repository-checked |
| OpenModelica / OMEdit | https://github.com/OpenModelica/OpenModelica/blob/master/OMEdit/OMEditLIB/MCP/README.md | Project steward | Experimental (1.27.0; disabled by default) | Bundled | Source-inspected and Vendor-documented |

## Electromagnetic / Antenna

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| openEMS | https://github.com/RFingAdam/mcp-openems | Community | Unassessed | Source available | Repository-checked |
| NEC2 | https://github.com/RFingAdam/mcp-nec2-antenna | Community | Unassessed | Source available | Repository-checked |
| Ansys Lumerical | https://github.com/leisymqaz/lumerical-mcp | Community | Unassessed | Source available | Repository-checked |

## Multiphysics / FEA

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Abaqus/CAE | https://github.com/jianzhichun/abaqus-mcp-server | Community | Unassessed | Source available | Repository-checked |
| FreeCAD FEM Workbench + CalculiX | https://github.com/sandraschi/freecad-mcp | Community | Unassessed | Source available | Repository-checked |
| FreeCAD FEM + CalculiX | https://github.com/neka-nat/freecad-mcp | Community | Unassessed | Source available | Repository-checked |
| MOOSE | https://github.com/sukritimanna/AutoMOOSE | Community | Reference | Source available | Repository-checked |

## Battery / Storage / PV

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Alpha ESS | https://github.com/michaelkrasa/alpha-ess-mcp-server | Community | Unassessed | Source available | Repository-checked |
| EG4 solar inverters + battery monitoring | https://github.com/matt-dreyer/EG4_MCP_server | Community | Unassessed | Source available | Repository-checked |
| NREL PVWatts v8 | https://github.com/hoodsy/solar-data-mcp | Community | Unassessed | Source available | Repository-checked |
| NREL PVWatts v8 + NREL Solar Resource API | https://github.com/ianherzog/solar-mcp | Community | Unassessed | Source available | Repository-checked |
| NREL PVWatts v8 | https://github.com/cwoodcox/pvwatts-mcp | Community | Unassessed | Source available | Repository-checked |
| Batterytwin-mcp | https://github.com/BinuShefieldShifani/Batterytwin-mcp | Community | Unassessed | Source available | Repository-checked |
| hil-for-bms | https://github.com/nidhi1902-source/hil-for-bms | Community | Unassessed | Source available | Repository-checked |
| Victron ESS | https://github.com/lubosstrejcek/victron-tcp | Community | Unassessed | Source available | Repository-checked |

## Wind

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| QBlade | https://github.com/JakubRasken/qblade-mcp-server | Community | Experimental | Source available | Repository-checked |

## PCB / ECAD

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Altium Designer | https://github.com/coffeenmusic/altium-mcp | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/10xgenomicsEng/altium-mcp-unified | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/embedded-society/altium-designer-mcp | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/flaco-source/altium-mcp | Community | Unassessed | Source available | Repository-checked |
| Cadence Allegro / Altium Designer / KiCad | https://github.com/IntelligentElectron/universal-netlist | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/salitronic/eda-agent | Community | Experimental | Source available | Repository-checked; no independent runtime validation |

## IC / ASIC EDA

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Cadence Virtuoso | https://github.com/michelebergo/virtuoso-schematic-mcp | Community | Unassessed | Source available | Repository-checked |
| OpenROAD / OpenROAD-flow-scripts | https://github.com/The-OpenROAD-Project/OpenROAD-MCP | Project steward | Available | Source available | Repository-checked |

## FPGA / HDL Verification

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| AMD/Xilinx Vivado | https://github.com/coreyhahn/vivado_mcp | Community | Unassessed | Source available | Repository-checked |
| Verilator | https://github.com/ssql2014/verilator-mcp | Community | Unassessed | Source available | Repository-checked |
| Open-source EDA suite | https://github.com/ssql2014/mcp4eda | Community | Unassessed | Source available | Repository-checked |
| Verilog/SystemVerilog static analysis | https://github.com/ariklapid/pyslang-mcp | Community | Unassessed | Source available | Repository-checked |
| Cadence Xcelium | https://github.com/hslee-cmyk/xcelium-mcp | Community | Unassessed | Source available | Repository-checked |

## Embedded / MCU Toolchains

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| STMicroelectronics STM32 | https://github.com/shieldyguy/stm32-mcp | Community | Unassessed | Source available | Repository-checked |
| Espressif ESP-IDF | https://github.com/horw/esp-mcp | Community | Unassessed | Source available | Repository-checked |
| PlatformIO | https://github.com/jl-codes/platformio-mcp | Community | Unassessed | Source available | Repository-checked |
| Zephyr RTOS / west workspace | https://github.com/leog25/zephyr-west-mcp | Community | Unassessed | Source available | Repository-checked |
| GNU GDB | https://github.com/Ipiano/gdb-mcp | Community | Unassessed | Source available | Repository-checked |
| Arduino CLI | https://github.com/hardware-mcp/arduino-mcp-server | Community | Unassessed | Source available | Repository-checked |
| Serial/UART instrumentation | https://github.com/Adancurusul/serial-mcp-server | Community | Unassessed | Source available | Repository-checked |
| QEMU | https://github.com/nagy/qemu-mcp-server | Community | Unassessed | Source available | Repository-checked |
| Espressif ESP-IDF | https://developer.espressif.com/blog/2026/04/esp-idf-tools-mcp-server/ | First-party | Available (6.0+) | Bundled | Vendor-documented |

## Instrumentation / T&M

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| QCoDeS lab instruments | https://github.com/caidish/instrMCP | Community | Unassessed | Source available | Repository-checked |
| Generic VISA/SCPI instruments | https://github.com/Hizuki1030/visa-mcp | Community | Unassessed | Source available | Repository-checked |
| Multi-protocol lab equipment | https://github.com/techmanual-ai/lablink-mcp | Community | Unassessed | Source available | Repository-checked |
| Siglent SDS oscilloscopes | https://github.com/magnusjohansson/siglent-sds-mcp | Community | Unassessed | Source available | Repository-checked |
| Keysight EDUX1052G oscilloscope | https://github.com/AnterCreeper/keyscope-mcp | Community | Unassessed | Source available | Repository-checked |
| RIGOL DS1000Z-series oscilloscopes | https://github.com/masahiro-999/oscilloscope-mcp | Community | Unassessed | Source available | Repository-checked |
| RIGOL DHO824 oscilloscope | https://github.com/aimoda/rigol-dho824-mcp | Community | Unassessed | Source available | Repository-checked |
| LabVIEW | https://github.com/CalmyJane/labview_assistant | Community | Unassessed | Source available | Repository-checked |
| Rohde & Schwarz T&M instruments | https://rsinstrument.readthedocs.io/en/latest/StepByStepGuide.html#mcp-server | First-party | Available (RsInstrument 1.120.0+) | Source available | Source-inspected and Vendor-documented |

## SCADA / PLC / Industrial Automation and Protocols

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Ignition | https://github.com/WhiskeyHouse/ignition-mcp | Community | Unassessed | Source available | Repository-checked |
| SIMATIC WinCC Unified | https://github.com/vogler75/winccua-mcp-server | Community | Unassessed | Source available | Repository-checked |
| OPC UA industrial systems | https://github.com/kukapay/opcua-mcp | Community | Unassessed | Source available | Repository-checked |
| OPC UA industrial data server | https://github.com/kmanditereza/mcp-server-for-industrial-data | Community | Unassessed | Source available | Repository-checked |
| Modbus | https://github.com/kukapay/modbus-mcp | Community | Unassessed | Source available | Repository-checked |
| Modbus | https://github.com/ezhuk/modbus-mcp | Community | Unassessed | Source available | Repository-checked |
| Modbus | https://github.com/midhunxavier/MODBUS-MCP | Community | Unassessed | Source available | Repository-checked |
| Modbus RTU/TCP master + slave | https://github.com/alejoseb/ModbusMCP | Community | Unassessed | Source available | Repository-checked |
| OPC UA industrial systems | https://github.com/midhunxavier/OPCUA-MCP | Community | Unassessed | Source available | Repository-checked |
| OPC UA industrial systems | https://github.com/intigration/mcp-uaserver | Community | Unassessed | Source available | Repository-checked |
| B&R Automation Studio | https://github.com/AndrewMusser/br-automation-mcp | Community | Unassessed | Source available | Repository-checked |
| Siemens TIA Portal | https://github.com/feelautom/tia-copilot-genai-bridge | Community · feelautom | Available | Commercial; public blueprint with proprietary driver | Repository-checked; proprietary core not validated |
| Ignition | https://forum.inductiveautomation.com/t/mcp-module-early-access/113966/22 | First-party | Early Access; full release planned for February 2027 | Commercial infrastructure module; no first-party primitives | Vendor-documented |
| SIMATIC WinCC OA | https://github.com/winccoa/winccoa-ae-js-mcpserver | First-party | Available | Source available; WinCC OA required | Repository-checked and Vendor-documented |

## Bus / Network Simulation and Test

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Vector CANoe | https://github.com/VectorCANoe/CANoe-mcp | Community | Unassessed | Source available | Repository-checked |
| Vector CANoe | https://github.com/rye00940094/canoe-mcp-debugger | Community | Unassessed | Source available | Repository-checked |

## Digital Twin / Virtual Commissioning

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| realvirtual.io Python MCP server | https://github.com/game4automation/realvirtual-MCP | First-party | Available | Source available; realvirtual/Unity environment required | Repository-checked |
| realvirtual.io Unity package | https://github.com/game4automation/io.realvirtual.mcp | First-party | Available | Source available; realvirtual/Unity environment required | Repository-checked |

## Machines / Condition Monitoring and Diagnostics

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Motor-current-signature-analysis fault diagnosis | https://github.com/LGDiMaggio/mcp-motor-current-signature-analysis | Community | Unassessed | Source available | Repository-checked |

## Engineering Data / Component Sourcing

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Electronic-parts search and BOM processing | https://github.com/SourceParts/parts-mcp | Community | Unassessed | Source available | Repository-checked |
| PCB component sourcing | https://github.com/Averyy/pcbparts-mcp | Community | Unassessed | Source available | Repository-checked |

## Building / Energy-System Modeling

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| EnergyPlus | https://github.com/LBNL-ETA/EnergyPlus-MCP | Institutional · LBNL research team | Unassessed (package version 0.1.0) | Source available | Repository-checked |

## Documentation-Only MCPs

These servers expose documentation or source-code lookup rather than operational simulator control.

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| PyBaMM documentation and source lookup | https://github.com/AUrbanec/pybamm_mcp | Community | Documentation-only | Source available | Repository-checked |
| Simulator documentation lookup | https://github.com/xupeiwust/simdoc-mcp | Community | Documentation-only | Source available / hosted endpoint | Repository-checked |

## Adjacent Network Testing

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Keysight CyPerf CE network-performance testing | https://github.com/ashwinjo/cyperf-ce-mcp-rest | Community | Unassessed | Source available; CyPerf environment required | Repository-checked |
