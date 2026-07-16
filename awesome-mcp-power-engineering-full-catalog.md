# Extended MCP Catalog for Power Engineering

> This supplement records a broader set of publicly accessible MCP implementations relevant to power
> engineering and adjacent engineering workflows. It is a superset of the
> [curated main list](./README.md): every curated entry appears here, plus additional alternatives.

Entries are classified from public repositories, first-party documentation, or official
announcements. `Repository-checked` means that the public endpoint and repository description were
reviewed; it does not imply successful installation, simulator execution, licensed-software
validation, instrument/target access, or hardware validation. `Unassessed` means that maturity was
not re-established during the latest review.

*Last reviewed: 2026-07-16.*

Field values are intentionally conservative: `First-party`, `Project steward`,
`Institutional`, and `Community` describe provenance; availability is reported separately;
`Source available` describes access, not maturity. See the [main list](./README.md#how-to-read-the-tables)
for the validation vocabulary.


## Power Systems / Grid

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Multi-engine grid studies: PSS/E, PowerWorld, PowerFactory, PSLF, ANDES, OpenDSS, pandapower, PSCAD, PyPSA, Egret, HOPE, LTspice, surge | https://github.com/Power-Agent/PowerMCP | Community | Alpha | Source available; vendor products may be required | Source-inspected |
| PyPSA | https://github.com/open-energy-transition/pypsa-mcp | Community | Unassessed | Source available | Source-inspected |
| DIgSILENT PowerFactory | https://github.com/Diptargha/mcp-powerfactory | Community | Unassessed | Source available | Repository-checked |
| DIgSILENT PowerFactory | https://github.com/ShuailongDai/Initial-PowerFactory-MCP-automation | Community | Unassessed | Source available | Repository-checked |
| DIgSILENT PowerFactory | https://github.com/bamiboy237/powerfactory-mcp | Community | Unassessed | Source available; PowerFactory required | Repository-checked |
| OpenDSS | https://github.com/ahmedelshazly27/opendss-mcp-server | Community | Unassessed | Source available | Repository-checked |

## Power Electronics / Circuit

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| SIMBA | [SIMBA Assistant (embedded MCP server)](https://doc.simba.io/version_history/26_03/) | First-party | Available (SIMBA 26.03+) | Optional commercial add-on (SIMBA Assistant module) | Vendor-documented |
| LTspice / ngspice | https://github.com/Cognitohazard/ltspice-mcp | Community | Unassessed | Source available | Source-inspected |
| ngspice | https://github.com/gtnoble/ngspice-mcp | Community | Unassessed | Source available | Source-inspected |
| QSPICE | https://github.com/kh6570/HAbedini-qspice-mcp | Community | Unassessed | Source available; QSPICE required | Source-inspected |
| PSIM | https://github.com/zongseung/psim-mcp | Community | Unassessed | Source available; PSIM required (mock adapter for development without PSIM) | Source-inspected |
| LTspice | https://github.com/xuio/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/daviditkin/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/HarshyChoc/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/BrosnanYuen/bltspice_mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/Janadasroor/ltspice-mcp | Community | Unassessed | Source available | Repository-checked |
| LTspice | https://github.com/AbiyuLingga/LTSpice-MCP | Community | Unassessed | Source available; LTspice required | Repository-checked |
| LTspice | https://github.com/bw493/ltspice-mcp-automation | Community | Unassessed | Source available; LTspice required | Repository-checked |
| LTspice (Linux / Wine) | https://github.com/River-jp/ltspice-mcp-for-linux | Community | Unassessed | Source available; LTspice under Wine required | Repository-checked |
| SPICE via spicelib | https://github.com/lucasgerads/spicelib-mcp | Community | Unassessed | Source available | Repository-checked |
| PLECS | https://github.com/yingriyanlong/plecs-mcp | Community | Unassessed | Source available | Repository-checked |
| PLECS | https://github.com/haitangccy/plecs-mcp | Community | Unassessed | Source available | Mock-tested; no live PLECS evidence recorded here |

## System-Level / Modelica / FMI

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| MATLAB | https://github.com/matlab/matlab-mcp-server | First-party | Available | Source available under MathWorks license terms; MATLAB required | Source-inspected and Vendor-documented |
| Simulink (Simulink Agentic Toolkit, used with MATLAB MCP Server) | https://github.com/matlab/simulink-agentic-toolkit | First-party | Available | Source available under MathWorks license terms; required MathWorks products | Source-inspected and Vendor-documented |
| MWORKS.Sysplorer | https://github.com/ACupOfHim/mworks-mcp-server | Community | Unassessed | Source available | Repository-checked |
| FMU / FMI | https://github.com/Novia-RDI-Seafaring/mcp-fmi | Community | Unassessed | Source available | Repository-checked |
| Modelica / ODE IDE | https://github.com/Orthogonalpub/modelica_simulation_mcp_server | First-party | Available | Hosted service; source available | Repository-checked |
| OpenModelica / OMEdit | https://github.com/OpenModelica/OpenModelica/blob/master/OMEdit/OMEditLIB/MCP/README.md | Project steward | Experimental (1.27.0; disabled by default) | Bundled | Source-inspected and Vendor-documented |

## Real-Time / HIL Simulation

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| dSPACE VEOS (PC-based offline / SIL simulation) | https://github.com/dspace-group/VeosMCP | First-party | Alpha (v0.1.0-rc) | Source available; VEOS required | Source-inspected |

## Electromagnetic / Antenna

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Ansys Lumerical | https://github.com/ansys/pylumerical-mcp | First-party | Alpha (v0.1.0) | Source available; Lumerical required | Source-inspected |
| openEMS | https://github.com/RFingAdam/mcp-openems | Community | Unassessed | Source available | Repository-checked |
| NEC2 | https://github.com/RFingAdam/mcp-nec2-antenna | Community | Unassessed | Source available | Repository-checked |
| Ansys Lumerical | https://github.com/leisymqaz/lumerical-mcp | Community | Unassessed | Source available | Repository-checked |
| Ansys HFSS via PyAEDT (antenna + PCB) | https://github.com/gfgf2023/hfss-mcp-server | Community | Unassessed | Source available; HFSS required | Repository-checked |
| Ansys HFSS via PyAEDT (antenna design) | https://github.com/NedaEmami123/hfss-mcp | Community | Unassessed | Source available; HFSS required | Repository-checked |
| Ansys HFSS (natural-language control) | https://github.com/K-13ROBOT/HFSS_MCP | Community | Unassessed | Source available; HFSS required | Repository-checked |

## Multiphysics / FEA

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Ansys Mechanical APDL | https://github.com/ansys/pymapdl-mcp | First-party | Available | Source available; MAPDL required | Source-inspected and Vendor-documented |
| Ansys AEDT: Maxwell / HFSS / Q3D / Icepak | https://github.com/ansys/pyaedt-mcp | First-party | Alpha (v0.1.0) | Source available; AEDT required | Source-inspected |
| Ansys AEDT: Maxwell / HFSS / Q3D / Icepak | https://github.com/LaplaceYoung/ansys-aedt-mcp | Community | Unassessed | Source available; AEDT required | Source-inspected |
| Ansys Fluent | https://github.com/ansys/pyfluent-mcp | First-party | Alpha (v0.1.0) | Source available; Fluent required | Source-inspected |
| Ansys Fluent / MAPDL / Mechanical / Geometry | https://github.com/knewnothing-git/ansys-mcp-server | Community | Unassessed | Source available; Ansys products required | Source-inspected |
| Ansys Mechanical | https://github.com/ansys/pymechanical-mcp | First-party | Alpha (v0.1.1) | Source available; Mechanical required | Source-inspected |
| Ansys Mechanical | https://github.com/codersag/mechanical-mcp | Community | Unassessed | Source available; Mechanical required | Source-inspected |
| COMSOL Multiphysics | https://github.com/wjc9011/COMSOL_Multiphysics_MCP | Community | Unassessed | Source available; COMSOL required | Source-inspected |
| OpenFOAM | https://github.com/webworn/openfoam-mcp-server | Community | Experimental | Source available | Source-inspected; project reports partial and incomplete solver coverage |
| CST Studio Suite | https://github.com/RFingAdam/mcp-cst-studio | Community | Unassessed | Source available; CST required | Source-inspected |
| Abaqus/CAE | https://github.com/jianzhichun/abaqus-mcp-server | Community | Unassessed | Source available | Repository-checked |
| FreeCAD FEM Workbench + CalculiX | https://github.com/sandraschi/freecad-mcp | Community | Unassessed | Source available | Repository-checked |
| FreeCAD FEM + CalculiX | https://github.com/neka-nat/freecad-mcp | Community | Unassessed | Source available | Repository-checked |
| MOOSE | https://github.com/sukritimanna/AutoMOOSE | Community | Reference | Source available | Repository-checked |
| Ansys (CFD / FEA) | https://github.com/vorobjewsen30-max/ansys-mcp-server | Community | Unassessed | Source available; Ansys products required | Repository-checked |
| Ansys Fluent / Mechanical / Geometry (TUI) | https://github.com/Bettertoo2/ansys-mcp-server | Community | Unassessed | Source available; Ansys products required | Repository-checked |
| Abaqus (job submit, log monitor, ODB results) | https://github.com/MOBAI547800/abaqus-mcp-server | Community | Unassessed | Source available; Abaqus required | Repository-checked |
| Abaqus (CAE plugin + IPC) | https://github.com/pureSaviour/abaqus-mcp | Community | Unassessed | Source available; Abaqus required | Repository-checked |

## Battery / Storage / PV

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Alpha ESS | https://github.com/michaelkrasa/alpha-ess-mcp-server | Community | Unassessed | Source available | Repository-checked |
| EG4 solar inverters + battery monitoring | https://github.com/matt-dreyer/EG4_MCP_server | Community | Unassessed | Source available | Repository-checked |
| NREL PVWatts v8 | https://github.com/hoodsy/solar-data-mcp | Community | Unassessed | Source available | Repository-checked |
| NREL PVWatts v8 + NREL Solar Resource API | https://github.com/ianherzog/solar-mcp | Community | Unassessed | Source available | Repository-checked |
| NREL PVWatts v8 | https://github.com/cwoodcox/pvwatts-mcp | Community | Unassessed | Source available | Repository-checked |
| Battery electrochemical simulation via PyBaMM | https://github.com/BinuShefieldShifani/Batterytwin-mcp | Community | Unassessed | Source available | Repository-checked |
| EV BMS safety-rule validation (software-simulated HIL, ontology-driven) | https://github.com/nidhi1902-source/hil-for-bms | Community | Unassessed | Source available; LLM API key required | Source-inspected; the "HIL" is a software simulator, no hardware integration |
| Victron ESS | https://github.com/lubosstrejcek/victron-tcp | Community | Unassessed | Source available | Repository-checked |

## Wind

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| QBlade | https://github.com/JakubRasken/qblade-mcp-server | Community | Experimental | Source available | Repository-checked |

## PCB / ECAD

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| KiCad | https://github.com/lamaalrajih/kicad-mcp | Community | Unassessed | Source available | Source-inspected |
| EasyEDA / JLCPCB | https://github.com/oaslananka/easyeda-mcp-pro | Community | Unassessed | Source available; external services may be required | Source-inspected |
| Altium Designer | https://github.com/coffeenmusic/altium-mcp | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/10xgenomicsEng/altium-mcp-unified | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/embedded-society/altium-designer-mcp | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/flaco-source/altium-mcp | Community | Unassessed | Source available | Repository-checked |
| Cadence Allegro / Altium Designer / KiCad | https://github.com/IntelligentElectron/universal-netlist | Community | Unassessed | Source available | Repository-checked |
| Altium Designer | https://github.com/salitronic/eda-agent | Community | Experimental | Source available | Repository-checked; no independent runtime validation |
| Altium Designer (DelphiScript automation) | https://github.com/rdacomp/altium-mcp | Community | Unassessed | Source available; Altium required | Repository-checked |
| Altium Designer + EasyEDA/JLCPCB part import and auto-placement | https://github.com/Sakuna-Nagodavithana/Altium-MCP-Placement | Community | Unassessed | Source available; Altium required | Repository-checked |
| KiCad 10 (IPC API, headless DRC / export, Windows) | https://github.com/iQreu/kicad-mcp | Community | Unassessed | Source available; KiCad required | Repository-checked |
| KiCad (design-review rules + Freerouting backend) | https://github.com/antonmadto/kicad-mcp | Community | Unassessed | Source available; KiCad required | Repository-checked |
| KiCad (design review + ECAD library import) | https://github.com/kamejoko80/kicad-mcp | Community | Unassessed | Source available; KiCad required | Repository-checked |
| KiCad 9+ (live control via official IPC API) | https://github.com/lmaag182/kicad_mcp_server_ipc | Community | Unassessed | Source available; KiCad required | Repository-checked |
| KiCad (read-only context server) | https://github.com/yigitabi5444/YSM-Kicad-MCP | Community | Unassessed | Source available | Repository-checked |
| KiCad (read-only, Rust) | https://github.com/brechanbech/kicad-mcp-rs | Community | Unassessed | Source available | Repository-checked |
| Schematic / PCB authoring toolkit + KiCad MCP servers | https://github.com/El-Guapo2024/hw-toolkit | Community | Unassessed | Source available; KiCad required | Repository-checked |
| KiCad (token-efficient read-only file reader) | https://github.com/2525-nico/kicad-mcp-server-mugi | Community | Unassessed | Source available | Repository-checked |
| EasyEDA Pro bridge (fast bridge + DRC) | https://github.com/cheewee2000/easyeda-mcp | Community | Unassessed | Source available; EasyEDA Pro required | Repository-checked |
| EasyEDA Pro bridge (bug-fix fork) | https://github.com/sheares/easyeda-mcp-fix | Community | Unassessed | Source available; EasyEDA Pro required | Repository-checked |
| EasyEDA Pro extension + MCP | https://github.com/anwarminarso/a2n-easyeda-mcp | Community | Unassessed | Source available; EasyEDA Pro required | Repository-checked |
| EasyEDA Pro bridge (netlist export) | https://github.com/stephanerosso59-debug/easyeda-mcp-bridge | Community | Unassessed | Source available; EasyEDA Pro required | Repository-checked |
| EasyEDA Pro (Bun, zero-dependency) | https://github.com/hiroki-sawada-a/easy_eda_mcp | Community | Unassessed | Source available; EasyEDA Pro required | Repository-checked |
| EasyEDA Pro automation plugin + MCP | https://github.com/Atmel2005/EasyEDA_MCP | Community | Unassessed | Source available; EasyEDA Pro required | Repository-checked |
| JLC-EDA (嘉立创 EDA) bridge extension | https://github.com/qcz2943/jlceda-mcp | Community | Unassessed | Source available; JLC-EDA required | Repository-checked |
| JLC-EDA (routing / schematic / silkscreen tools) | https://github.com/0xruth1ezz/jlc-eda-mcp | Community | Unassessed | Source available; JLC-EDA required | Repository-checked |

## IC / ASIC EDA

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Cadence Virtuoso | https://github.com/michelebergo/virtuoso-schematic-mcp | Community | Unassessed | Source available | Repository-checked |
| OpenROAD / OpenROAD-flow-scripts | https://github.com/The-OpenROAD-Project/OpenROAD-MCP | Project steward | Available | Source available | Repository-checked |
| Yosys / OpenROAD workflows | https://github.com/NellyW8/MCP4EDA | Community | Unassessed | Source available | Source-inspected |
| Cadence Innovus / Genus / Tempus over SSH | https://github.com/vs34/EDA_MCP | Community | Unassessed | Source available; Cadence tools + SSH environment required | Repository-checked |

## FPGA / HDL Verification

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| AMD Vivado / RapidWright | https://github.com/Xilinx/fpl26_optimization_contest | First-party | Reference | Source available contest example; tool licenses may be required | Source-inspected |
| AMD/Xilinx Vivado | https://github.com/coreyhahn/vivado_mcp | Community | Unassessed | Source available | Repository-checked |
| Intel / Altera Quartus | https://github.com/abbbe/fpga-mcp-servers | Community | Unassessed | Source available; Quartus required | Source-inspected |
| Verilator | https://github.com/ssql2014/verilator-mcp | Community | Archived (repository archived on GitHub) | Source available | Repository-checked |
| Verilog / SystemVerilog RTL semantic analysis (tree-sitter + pyslang) | https://github.com/airry12/verilog-mcp-server | Community | Unassessed | Source available | Repository-checked |
| AMD/Xilinx Vivado (Windows) | https://github.com/Emanuel-Clearfield/Vivado_MCP_Windows | Community | Unassessed | Source available; Vivado required | Repository-checked |
| Open-source EDA suite | https://github.com/ssql2014/mcp4eda | Community | Unassessed | Source available | Repository-checked |
| Verilog/SystemVerilog static analysis | https://github.com/ariklapid/pyslang-mcp | Community | Unassessed | Source available | Repository-checked |
| Cadence Xcelium | https://github.com/hslee-cmyk/xcelium-mcp | Community | Unassessed | Source available | Repository-checked |

## Embedded / MCU Toolchains

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| CCStudio project and debug servers | [TI MCP documentation](https://software-dl.ti.com/ccs/esd/documents/application_notes/appnote-ccs_ai_code_assistant.html) | First-party | Available (CCStudio 20.5.x+) | Bundled | Vendor-documented |
| ARM Cortex-M / RISC-V debugging via probe-rs | https://github.com/adancurusul/embedded-debugger-mcp | Community | Unassessed | Source available; target hardware optional | Source-inspected |
| GNU GDB | https://github.com/pansila/mcp_server_gdb | Community | Unassessed | Source available | Source-inspected |
| STMicroelectronics STM32 | https://github.com/shieldyguy/stm32-mcp | Community | Unassessed | Source available | Repository-checked |
| Espressif ESP-IDF | https://github.com/horw/esp-mcp | Community | Unassessed | Source available | Repository-checked |
| PlatformIO | https://github.com/jl-codes/platformio-mcp | Community | Unassessed | Source available | Repository-checked |
| Zephyr RTOS / west workspace | https://github.com/leog25/zephyr-west-mcp | Community | Unassessed | Source available | Repository-checked |
| GNU GDB | https://github.com/Ipiano/gdb-mcp | Community | Unassessed | Source available | Repository-checked |
| Arduino CLI | https://github.com/hardware-mcp/arduino-mcp-server | Community | Unassessed | Source available | Repository-checked |
| Serial/UART instrumentation | https://github.com/Adancurusul/serial-mcp-server | Community | Unassessed | Source available | Repository-checked |
| QEMU | https://github.com/nagy/qemu-mcp-server | Community | Unassessed | Source available | Repository-checked |
| OpenOCD JTAG / SWD debugging | https://github.com/microhenrio/openocd-mcp | Community | Unassessed | Source available; target hardware required | Repository-checked |
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
| LabVIEW (run VIs, I/O, tests, TDMS) | https://github.com/rbxxswap/labview-mcp | Community | Unassessed | Source available; LabVIEW required | Repository-checked |
| RIGOL DS1000Z / MSO1000Z oscilloscopes (raw SCPI) | https://github.com/DVSProductions/rigol-mcp | Community | Unassessed | Source available; instrument required | Repository-checked |
| Siglent SPD1000X programmable DC supplies (raw SCPI) | https://github.com/DVSProductions/siglent-mcp | Community | Unassessed | Source available; instrument required | Repository-checked |
| Siglent SDS2000X Plus oscilloscopes (TCP/IP SCPI) | https://github.com/lxkang00/oscilloscope-mcp | Community | Unassessed | Source available; instrument required | Repository-checked |
| Keysight MXA / CMW500 / PSU via SCPI | https://github.com/zeng-andrew/instrument-mcp | Community | Unassessed | Source available; instruments required | Repository-checked |
| RIGOL DHO4000 scope + Siglent SDG1000 generator + PSU | https://github.com/Xingwen37/instrument_mcp | Community | Unassessed | Source available; instruments required | Repository-checked |
| USB PC oscilloscopes (multi-backend) | https://github.com/sandraschi/oscilloscope-mcp | Community | Unassessed | Source available; instrument required | Repository-checked |
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
| OPC UA with semantic allowlist + audit sink | https://github.com/kevin-rieck/managed-opcua-mcp | Community | Unassessed | Source available; OPC UA endpoint required | Repository-checked |
| OPC UA / MQTT industrial adapters (Modbus, DNP3, EtherNet/IP, AVEVA adapters are unimplemented stubs) | https://github.com/fieldworks-build/fieldworks-adapters | Community | Unassessed | Source available; endpoints required | Source-inspected; only the OPC UA and MQTT adapters are implemented |
| OPC UA bridge (hexagonal architecture) | https://github.com/Edu-bahamondes/opcua-mcp-bridge | Community | Unassessed | Source available; OPC UA endpoint required | Repository-checked |
| Generic SCADA / ICS | https://github.com/zavora-ai/mcp-scada | Community | Unassessed | Source available | Repository-checked |
| Siemens-style PLC Structured Text generation | https://github.com/SHU996/eigen-plc-mcp | Community | Unassessed | Source available | Repository-checked |
| WAGO PLC | https://github.com/WagoAlex/wago-plc-mcp-server | Community | Unassessed | Source available; WAGO PLC required | Repository-checked |
| Mitsubishi GX Works PLC (FX instruction set) | https://github.com/hendrikelektrik/gx-plc-mcp | Community | Unassessed | Source available; GX Works required | Repository-checked |
| Omron PLC (FINS protocol) | https://github.com/paodanchacon/plc-mcp | Community | Unassessed | Source available; PLC required | Repository-checked |
| CODESYS / Structured Text | https://github.com/uiff/Codesys-MCP-Server | Community | Unassessed | Source available; CODESYS required | Repository-checked |

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
| Microchip device selection and supply-chain data | [Microchip MCP Server](https://www.microchip.com/en-us/resources/model-context-protocol-server) | First-party | Available | Public hosted endpoint (`api.microchip.com/mcp/resources`) | Vendor-documented |
| Electronic-parts search and BOM processing | https://github.com/SourceParts/parts-mcp | Community | Unassessed | Source available | Repository-checked |
| PCB component sourcing | https://github.com/Averyy/pcbparts-mcp | Community | Unassessed | Source available | Repository-checked |
| PCBWay Partner API (quotes, SMT assembly, orders) | https://github.com/nabheet/pcbway-mcp-server | Community | Unassessed | Source available; PCBWay account required | Repository-checked |

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
| Zephyr RTOS docs / Kconfig / Devicetree context | https://github.com/Aarav-J/zephyr-mcp-server | Community | Documentation-only | Source available | Repository-checked |

## Adjacent Network Testing

| Target | MCP | Publisher | Availability | Access | Validation |
|---|---|---|---|---|---|
| Keysight CyPerf CE network-performance testing | https://github.com/ashwinjo/cyperf-ce-mcp-rest | Community | Unassessed | Source available; CyPerf environment required | Repository-checked |
