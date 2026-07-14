# awesome-mcp-for-power-engineering — Full Verified Catalog (Supplement)

> Complete list of every MCP server verified real in the 2026-07 two-round sweep (88 entries). The **curated pick (most-mature 1–2 + official per tool)** lives in the [main list](./awesome-mcp-for-power-engineering.md); this file is the exhaustive reference including all alternatives. `off` = vendor first-party, `comm` = community, `ref` = reference/example.


## Power Systems / Grid

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| DIgSILENT PowerFactory | comm | https://github.com/Diptargha/mcp-powerfactory | 0 stars, MIT license, ~6 commits; personal re | Confirmed via WebFetch of the GitHub repo. Genuine MCP server (FastMCP >=2.0), main script MCP_PowerFactory.py, exposes tools like run_simulation, run_loadflow, run_short_circuit,  |
| DIgSILENT PowerFactory | comm | https://github.com/ShuailongDai/Initial-PowerFactory-MCP-automation | 0 stars, 0 forks, single author, MIT, pushed  | Repo exists and is a genuine MCP server. Source confirms `from mcp.server.fastmcp import FastMCP`, `mcp = FastMCP(\"powerfactory\")`, ~11 `@mcp.tool()`-decorated functions, and `mc |
| OpenDSS | comm | https://github.com/ahmedelshazly27/opendss-mcp-server | 1 star; created 2025-10-12, last push 2025-10 | Genuine MCP server, verified from source (src/opendss_mcp/server.py): imports `from mcp.server.fastmcp import FastMCP`, instantiates `mcp = FastMCP(name="opendss-mcp-server")`, and |
| Keysight CyPerf CE | comm | https://github.com/ashwinjo/cyperf-ce-mcp-rest | Public repo, MIT license, single author (ashw | README confirms a genuine MCP server (stdio + SSE + streamable HTTP) layered over a FastAPI app that drives Keysight CyPerf CE client/server tests over SSH. Exposes 7 MCP tools: st |
| pandapower | comm | https://smithery.ai/server/@Semagram-Energy/pandapower_mcp | Smithery listing shows "Deployed" status + "v | Confirmed: live Smithery-hosted MCP server (Smithery is MCP-only). Documented MCP tools drive pandapower directly — create empty network, load network from file, run power flow (Ne |

## Power Electronics / Circuit

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| LTspice | comm | https://github.com/xuio/ltspice-mcp | ~67 commits on main; updated ~2026-05; single | WebFetch of the repo confirms it is a genuine MCP server that drives the LTspice GUI on macOS (UI automation + ScreenCaptureKit screenshots), not a batch/Wine wrapper or plain API. |
| LTspice | comm | https://github.com/daviditkin/ltspice-mcp | ~5 stars, Python 100%, small/educational proj | Repo exists and is public. Genuine MCP server (Python) exposing 8+ MCP tools that drive LTspice, not a plain API wrapper or chatbot: list_schematics, read_schematic, read_parameter |
| LTspice | comm | https://github.com/HarshyChoc/ltspice-mcp | 0 stars, 0 forks, 1 commit — brand-new, near- | Repo exists and is public. Genuine Python MCP server driving LTspice, not a plain API wrapper or chatbot. Exposes ~14 MCP tools: simulate, write_netlist, parse_schematic, patch_sch |
| LTspice | comm | https://github.com/BrosnanYuen/ltspice_mcp | ~1 star, 36 commits on main, updated 2026-07- | Public GitHub repo confirmed live. README: "Asynchronous MCP server for LTspice + PyLTSpice built with fastmcp." Genuinely an MCP server (built on fastmcp) that drives LTspice via  |
| LTspice | comm | https://github.com/Janadasroor/ltspice-mcp | 0 stars, single author (Janada Sroor), 1 comm | Genuine MCP server. src/ltspice_mcp/server.py imports `from mcp.server.fastmcp import FastMCP`, instantiates `mcp = FastMCP("LTspice-MCP")`, and registers ~21 tools via `@mcp.tool( |
| SPICE via spicelib | comm | https://github.com/lucasgerads/spicelib-mcp | 6 stars, GPL-3.0, Python, 5 releases; pushedA | Repo exists and is a genuine MCP server. Source confirms `from mcp.server.fastmcp import FastMCP` in server.py plus multiple `@mcp.tool()` decorators — not a plain API wrapper or c |
| PLECS | comm | https://github.com/yingriyanlong/plecs-mcp | 0 stars; created 2026-06-30, pushed 2026-07-0 | Verified adversarially via GitHub API (not just fetch-model). Repo exists: full_name yingriyanlong/plecs-mcp, MIT, Python, 0 stars, fork=false, created 2026-06-30, pushed 2026-07-0 |
| PLECS | comm | https://github.com/haitangccy/plecs-mcp | ~6 stars, Python 100%, 49 unit tests | Fetched the GitHub repo directly — it resolves and returns real content. It is a genuine MCP server (server.py + plecs_client.py) that drives PLECS 4.7 Standalone over its XML-RPC  |

## System-Level / Modelica / FMI

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| MWORKS.Sysplorer | comm | https://github.com/ACupOfHim/mworks-mcp-server | 0 stars, 0 forks, ~1 commit, Python, last pus | Verified via gh API + raw source. server.py (1108 lines) uses `from mcp.server.fastmcp import FastMCP`, `mcp = FastMCP(...)`, and ~18 `@mcp.tool()` functions. Imports `from mworks. |
| FMU / FMI | comm | https://github.com/Novia-RDI-Seafaring/mcp-fmi | ~12 stars, 5 forks, 82 commits, 100% Python,  | Live repo confirmed via WebFetch. Genuine MCP server wrapping the FMPy package to run FMU (Functional Mock-up Unit) co-simulation/model-exchange simulations from an LLM agent. Expo |
| Modelica / ODE IDE | **off** | https://github.com/Orthogonalpub/modelica_simulation_mcp_server | 20 stars, 6 forks, MIT, actively maintained b | Repo exists and is a genuine MCP server ("lightweight Model Context Protocol server for simulating Modelica models"). Exposes real MCP tools: modelica_simulate() (end-to-end Modeli |
| OpenModelica | **off** | https://github.com/OpenModelica/OpenModelica/issues/15385 | Issue closed, assigned to milestone 1.27.0, a | Issue #15385 "Implement MCP server for OMEdit interaction with chatbots" confirmed via WebFetch. It is genuinely an MCP server (not an API wrapper or chatbot): built into the OMEdi |

## Electromagnetic / Antenna

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| openEMS | comm | https://github.com/RFingAdam/mcp-openems | ~3 stars, Python 100%, AGPL-3.0-or-later, lat | Verified via WebFetch of the GitHub repo plus WebSearch (Glama, mcpmarket listings). Genuine MCP server exposing openEMS-driving tools: openems_create_patch, openems_create_dipole, |
| NEC2 | comm | https://github.com/RFingAdam/mcp-nec2-antenna | ~1 star, 0 forks, 2 releases (latest v0.2.0 M | Repo exists and is active. README explicitly describes a Model Context Protocol server exposing 9 tools that wrap the canonical nec2c C binary (NEC2 method-of-moments solver). Supp |
| Ansys Lumerical | comm | https://github.com/leisymqaz/lumerical-mcp | ~6 stars, 2 commits, actively-developed demo; | Repo confirmed live. Genuine MCP server exposing tools around Lumerical's bundled lumapi.py: session mgmt (open/close/list), script execution + variable retrieval, project file han |

## Multiphysics / FEA

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| Abaqus/CAE | comm | https://github.com/jianzhichun/abaqus-mcp-server | ~95 stars, 14 forks; MIT; Python 100%; 2 comm | Verified via WebFetch of the GitHub repo + WebSearch. It is a real FastMCP-based MCP server (author Zao Zhang / 简直蠢丶, handle jianzhichun). Drives an ALREADY-RUNNING Abaqus/CAE GUI  |
| FreeCAD FEM Workbench + CalculiX | comm | https://github.com/sandraschi/freecad-mcp | ~9 stars, 0 forks; Python 55.6% / TypeScript  | WebFetch of github.com/sandraschi/freecad-mcp confirms the repo exists and self-describes as a "FastMCP 3.2 MCP server + webapp for FreeCAD 3D CAD and FluidX3D/OpenFOAM CFD extensi |
| FreeCAD FEM + CalculiX | comm | https://github.com/neka-nat/freecad-mcp | ~1.3k stars | Confirmed via WebFetch of the GitHub repo. Genuine MCP server ("control FreeCAD from Claude Desktop") using an addon + server architecture. Exposes real MCP tools: create_document, |
| MOOSE | ref | https://github.com/sukritimanna/AutoMOOSE | arXiv 2603.20986 (Mar 2026) paper-backed; act | Repo confirmed to exist and to contain a real MCP server at automoose/mcp_server.py exposing exactly ten tools (health_check, list_plugins, generate_input, run_simulation, run_swee |

## Battery / Storage / PV

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| Alpha ESS | comm | https://github.com/michaelkrasa/alpha-ess-mcp-server | ~0 GitHub stars, MIT license; low maturity si | Genuine Python MCP server wrapping the official Alpha ESS Open API via the alphaess-openAPI library. Exposes MCP tools: authenticate_alphaess, get_ess_list, get_alpha_ess_data, get |
| EG4 solar inverters + battery monitoring | comm | https://github.com/matt-dreyer/EG4_MCP_server | GitHub 0 stars, ~22 commits, Python 98%; also | GitHub repo https://github.com/matt-dreyer/EG4_MCP_server exists and is a real MCP server (Python, FastMCP-style) exposing ~8 tools: Fetch_Configuration, Get_System_Details, Get_Cu |
| NREL PVWatts v8 | comm | https://github.com/hoodsy/solar-data-mcp | Community repo by GitHub user hoodsy; distrib | Confirmed via WebFetch of github.com/hoodsy/solar-data-mcp. README: 'US solar data, agent-accessible'. It is an MCP server, distributed as uvx solar-data-mcp, requiring user-suppli |
| NREL PVWatts v8 + NREL Solar Resource AP | comm | https://github.com/ianherzog/solar-mcp | 0 stars; created & last pushed 2026-03-27 (sa | Genuine FastMCP server. server.py imports `from fastmcp import FastMCP` and registers four tools via `mcp.tool()`: lookup_ahj, lookup_ahj_requirements, lookup_pvwatts, lookup_solar |
| NREL PVWatts v8 | comm | https://github.com/cwoodcox/pvwatts-mcp | 0 stars, public, TypeScript, last pushed 2026 | Public repo confirmed via `gh repo view` and WebFetch. Genuine MCP server: src/mcp.ts defines a PVWattsMCP class extending McpAgent<Env>, instantiates `new McpServer()` (name "pvwa |
| Batterytwin-mcp | comm | https://github.com/BinuShefieldShifani/Batterytwin-mcp | Python 97.8%, MIT, ~10 commits on main; indep | Verified two ways. (1) Repo root README exists: "physics-based lithium-ion digital twin (PyBaMM) exposed over MCP." (2) Source file src/battery_twin/servers/twin_server.py exists a |
| hil-for-bms | comm | https://github.com/nidhi1902-source/hil-for-bms | 0 stars, 0 forks, 3 commits; pushed 2026-06;  | Confirmed by direct source read of BMS Agent/bms_mcp_server.py (not just README). Uses `from mcp.server.fastmcp import FastMCP`, registers MCP tools via @mcp.tool(), runs stdio JSO |
| pybamm_mcp | comm | https://github.com/AUrbanec/pybamm_mcp | 1 star, pushed ~2026-02, independent author A | Repo exists and is a genuine MCP stdio server. Exposes three tools: search_pybamm_docs(query), read_doc_page(filepath), read_pybamm_source_code(module_path). All are documentation/ |
| simdoc-mcp | ref | https://github.com/xupeiwust/simdoc-mcp | Listed on Glama (@jiweiqi/simdoc-mcp), playbo | EXISTS and IS a genuine MCP server: exposes two MCP tools, resolve-simulator-id and get-simulator-docs, over a hosted SSE endpoint https://simdoc.subspace-lab.com/sse. HOWEVER it i |

## Wind

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| QBlade | comm | https://github.com/JakubRasken/qblade-mcp-server | 0 stars, no description; single-author repo c | Repo EXISTS and is a genuine MCP server. package.json depends on @modelcontextprotocol/sdk ^1.0.1, type=module, entry index.js. index.js imports { Server } from @modelcontextprotoc |

## EDA / PCB / IC

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| Altium Designer | comm | https://github.com/coffeenmusic/altium-mcp | ~111 stars, 32 forks; Pascal 64.5% + Python 3 | Confirmed via WebFetch of the GitHub repo. README states it is a Model Context Protocol (MCP) server that interfaces with Altium Designer via Python. Genuinely drives the tool thro |
| Altium Designer | comm | https://github.com/10xgenomicsEng/altium-mcp-unified | ~1 star, 1 fork; created 2026-03-19, single-d | Repo exists at 10xgenomicsEng/altium-mcp-unified (default branch: master, not main — README on /main 404s). Genuine FastMCP server, not a plan or wrapper. server/main.py instantiat |
| Altium Designer | comm | https://github.com/embedded-society/altium-designer-mcp | ~27 stars, 8 forks, 849 commits, active dev,  | Genuine Rust MCP server exposing ~34 MCP tools that read/write Altium .PcbLib/.SchLib OLE compound files directly (no live Altium install required). Third-party org "The Embedded S |
| Altium Designer | comm | https://github.com/flaco-source/altium-mcp | flaco-source fork ~8 stars, MIT; upstream cof | Confirmed via WebFetch of both repos. flaco-source/altium-mcp is a genuine MCP server (Windows) bridging MCP clients (Cursor/Claude) to Altium Designer 22+ via DelphiScript automat |
| Cadence Virtuoso | comm | https://github.com/michelebergo/virtuoso-schematic-mcp | ~1 star, 0 forks, single-commit master branch | Confirmed via WebFetch of the GitHub repo. It is a genuine Python MCP server that drives a live Cadence Virtuoso session over SkillBridge (Python-to-SKILL bridge). Exposes real MCP |
| OpenROAD / OpenROAD-Flow-Scripts | comm | https://github.com/luarss/openroad-mcp | ~11 stars, 9 forks, 127 commits, 24 open issu | Repo exists and is active. Genuine MCP server built on FastMCP (uvx/fastmcp). Exposes 9 MCP tools matching the claim: interactive_openroad, create/list/terminate/inspect_interactiv |
| Multi-EDA | comm | https://github.com/SourceParts/parts-mcp | ~1 star, 0 forks; 121 commits, 11 releases (l | Repo exists and is a real MCP server. Exposes MCP tools: search_parts, get_part_details, get_part_pricing, check_availability, find_alternatives, process_bom, match_components, fin |
| AMD/Xilinx Vivado | comm | https://github.com/coreyhahn/vivado_mcp | 53 stars, Python 100%, pushed ~2026-02 | WebFetch of the repo confirms a real MCP server. Holds a persistent Vivado process in TCL mode via pexpect (waits on the Vivado prompt) to avoid ~30s restart per command. Exposes c |
| Verilator | comm | https://github.com/ssql2014/verilator-mcp | 4 stars, TypeScript, v0.2.0 released 2025-06- | Repo exists and is a genuine MCP server (not a plain API wrapper/chatbot). Exposes 4 MCP tools that drive Verilator: verilator_compile (Verilog/SV to C++), verilator_simulate (RTL  |
| Open-source EDA suite | comm | https://github.com/ssql2014/mcp4eda | 40 stars, TypeScript (57.8%)/Python/JS, last  | WebFetch confirms existence and MCP nature. Self-described as "A comprehensive collection of Model Context Protocol (MCP) servers designed to enhance EDA workflows in Claude Deskto |
| Verilog/SystemVerilog static analysis | comm | https://github.com/ariklapid/pyslang-mcp | 19 stars, 84 commits, Apache-2.0, pushed 2026 | Repo exists and is a genuine read-only MCP server built on pyslang (Python bindings to the slang SystemVerilog compiler frontend). Exposes 14 MCP tools that drive the compiler: pys |
| Cadence Xcelium | comm | https://github.com/hslee-cmyk/xcelium-mcp | 1 star, MIT-ish (no license file), Python, pu | Repo verified via gh (public, Python, pushedAt 2026-07-08, 1 star) and WebFetch of the README. Genuine MCP server: Python FastMCP backend that drives a live Xcelium/SimVision sessi |
| Cadence Allegro / Altium Designer / KiCa | comm | https://github.com/IntelligentElectron/universal-netlist | 25 stars, 2 forks, updated 2026-07-13, pushed | Repo exists and is genuinely an MCP server. src/server.ts plus a src/service/tools/ directory register discrete MCP tools: list_designs, list_components, list_nets, query_component |
| Altium Designer | comm | https://github.com/salitronic/eda-agent | ~88 stars; active; Python 65.6% / Pascal (Del | WebFetch of the repo confirms it. eda-agent is an open-source MCP server that lets MCP-compatible clients drive a LIVE Altium Designer session. Architecture is genuine MCP: MCP cli |
| PCB component sourcing | comm | https://github.com/Averyy/pcbparts-mcp | ~79 stars, 248 commits, actively maintained;  | Genuine MCP server (Python, MCP protocol/HTTP transport) exposing 14 tools: jlc_search, jlc_stock_check, jlc_get_part, jlc_get_pinout, jlc_find_alternatives, jlc_search_help, mouse |

## Embedded / MCU Toolchains

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| STMicroelectronics STM32 | comm | https://github.com/shieldyguy/stm32-mcp | 16 stars, Python, created 2026-02-27, last pu | Verified via GitHub API + source inspection. pyproject.toml declares dependency "mcp>=1.0.0" (official MCP Python SDK) and console entry point stm32_mcp.server:main. server.py impo |
| Espressif ESP-IDF | comm | https://github.com/horw/esp-mcp | 154 stars, 19 forks, Python 100%, self-descri | WebFetch of the canonical GitHub page confirms a real, genuine MCP server (not an API wrapper or chatbot). It exposes 7 MCP tools that shell out to the ESP-IDF toolchain: run_esp_i |
| PlatformIO | comm | https://github.com/jl-codes/platformio-mcp | 40 stars, TypeScript, last push ~2026-05/06 ( | WebFetch of the repo confirms it exists and is a genuine MCP server (not a plain API wrapper or chatbot). README: "PlatformIO MCP is the open-source, agent-first hardware execution |
| Zephyr RTOS / west workspace | comm | https://github.com/leog25/zephyr-west-mcp | JavaScript, 1 star, created 2025-09-04, last  | Genuine MCP server: src/index.js instantiates an MCP server via @modelcontextprotocol/sdk with StdioServerTransport and ListTools/CallTool handlers (server name 'mcp-zephyr'). Expo |
| GNU GDB | comm | https://github.com/Ipiano/gdb-mcp | Ipiano/gdb-mcp: Python, 39 stars, MIT. pansil | Confirmed both repos exist and are genuine MCP servers driving GDB over the GDB/MI machine interface (not API wrappers or chatbots). Ipiano/gdb-mcp (Python, MIT, 39 stars) exposes  |
| Arduino CLI | comm | https://github.com/hardware-mcp/arduino-mcp-server | 14 stars; v0.2.8 released 2026-03-08; publish | Repo hardware-mcp/arduino-mcp-server confirmed live. Genuine MCP server (JS/TS, ~72% JS) wrapping arduino-cli — exposes 20+ MCP tools: detect_hardware, list_connected_boards, compi |
| Serial/UART instrumentation | comm | https://github.com/Adancurusul/serial-mcp-server | 75 stars, 22 forks, v0.3.0 released 2026-06-2 | Rust MCP stdio server exposing genuine serial-port MCP tools: list_ports, open, write, read, close, set_control_lines (RTS/DTR), plus a JSON macro DSL for repeatable timed workflow |
| QEMU | comm | https://github.com/nagy/qemu-mcp-server | 3 stars, Rust, last push 2025-08-18, 2 commit | Verified via gh API + source read of qemu_mcp_server.rs. Genuine MCP server: built on the official Rust MCP SDK (rmcp) with ServerHandler, enable_tools, stdio transport, and #[tool |
| Multi-protocol lab equipment | comm | https://github.com/techmanual-ai/lablink-mcp | GitHub ~2 stars, v0.1.0 released 2026-05-30,  | Verified via PyPI JSON API (pypi.org/pypi/lablink-mcp/json) and the GitHub repo. Genuinely an MCP server: exposes concrete MCP tools — lifecycle (connect, disconnect, list_devices, |
| Modbus | comm | https://github.com/ezhuk/modbus-mcp | GitHub ~2 stars/2 forks; PyPI v0.3.2 released | Genuine FastMCP 2.0 MCP server by community author @ezhuk. Exposes real MCP tools: Read Registers and Write Registers (holding registers/coils), plus interactive prompts. Serves St |
| Modbus | comm | https://github.com/midhunxavier/MODBUS-MCP | Small community repo; dual Python + Node/TS i | WebFetch of live GitHub repo confirms a genuine MCP server. README: "A Model Context Protocol (MCP) server for Modbus that lets AI agents and MCP-compatible apps read and write Mod |
| Espressif ESP-IDF | **off** | https://developer.espressif.com/blog/2026/04/esp-idf-tools-mcp-server/ | Vendor-official feature shipped in ESP-IDF v6 | Genuine stdio-based MCP server built into idf.py, launched via `idf.py mcp-server` (from an activated ESP-IDF project dir) or via ESP-IDF Installation Manager (EIM 0.8.1+, `eim run |

## Instrumentation / T&M

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| QCoDeS lab instruments | comm | https://github.com/caidish/instrMCP | ~27 stars, 4 forks, 241 commits, actively mai | Repo confirmed live at github.com/caidish/instrMCP (author caidish / Jiaqi Cai). Genuinely an MCP server: exposes MCP tools + resources over the Model Context Protocol, advertised  |
| Generic VISA/SCPI instruments | comm | https://github.com/Hizuki1030/visa-mcp | ~4 stars, 1 fork, 9 commits, no releases — ea | Repo confirmed live. src/server.py uses FastMCP (`mcp = FastMCP("VISASender")`) and exposes two real MCP tools: send_visa_command (writes/queries SCPI over TCPIP/socket/GPIB/USB vi |
| Siglent SDS oscilloscopes | comm | https://github.com/magnusjohansson/siglent-sds-mcp | ~4 stars, 1 fork, ~12 commits — small/new but | WebFetch confirms the repo is a real MCP server. It drives Siglent SDS scopes via SCPI over TCP port 5025 (no VISA/NI-MAX). Exposes ~12-13 MCP tools across 6 categories: Connection |
| Keysight EDUX1052G oscilloscope | comm | https://github.com/AnterCreeper/keyscope-mcp | 0 stars; created & last pushed 2026-05-27 (si | Verified via gh API (WebFetch of README subpaths 404'd but repo root fetched fine). Repo: name "keyscope-mcp", description "Keysight Oscilloscope MCP Server" / "MCP service for con |
| RIGOL DS1000Z-series oscilloscopes | comm | https://github.com/masahiro-999/oscilloscope-mcp | 0 stars, 0 forks, single-commit repo, MIT lic | Repo exists at masahiro-999/oscilloscope-mcp. Genuine MCP server: Python, FastMCP-based (src/oscilloscope_mcp/server.py, tool registration + dispatch), runs as local stdio MCP serv |
| RIGOL DHO824 oscilloscope | comm | https://github.com/aimoda/rigol-dho824-mcp | Listed on PulseMCP, Glama, LobeHub, MCPKit, m | Genuine MCP server (Python, ~96% Python), not a plain API wrapper or chatbot. Uses the MCP framework and communicates with hardware over VISA (RIGOL_RESOURCE, e.g. TCPIP0::IP::inst |
| RIGOL DS1000Z oscilloscopes | comm | https://github.com/masahiro-999/oscilloscope-mcp | GitHub repo exists, 0 stars, ~1 commit (very  | Confirmed via WebFetch of both the Glama listing and the GitHub repo. It is a genuine FastMCP server (server.py registers/dispatches tools) exposing ~13 MCP tools: scope_query (raw |
| Electric motor fault diagnosis via Motor | comm | https://github.com/LGDiMaggio/mcp-motor-current-signature-analysis | GitHub ~8 stars, Python 99.9%, 19 commits, la | Verified via both the Glama listing and the underlying GitHub repo (LGDiMaggio/mcp-motor-current-signature-analysis, aka mcp-server-mcsa). Genuine MCP server built on the official  |
| LabVIEW | comm | https://github.com/CalmyJane/labview_assistant | ~18 stars, 7 forks, 13 open issues; Python 98 | Confirmed via WebFetch of the GitHub repo. It is genuinely an MCP server (README: "MCP server implementation" that lets LLMs like ChatGPT/Claude Desktop control LabVIEW; installed  |
| Rohde & Schwarz T&M instruments | **off** | https://github.com/Rohde-Schwarz/RsInstrument | ~106 GitHub stars, 26 forks, MIT; PyPI v1.124 | Verified via WebFetch of both the GitHub repo and the PyPI page. RsInstrument is R&S's official Python remote-control module for SCPI-based T&M instruments (oscilloscopes, spectrum |

## SCADA / Industrial Protocols

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| Ignition | comm | https://github.com/WhiskeyHouse/ignition-mcp | Active repo; also published on PyPI (ignition | Genuine MCP server built on FastMCP exposing ~37 hand-crafted tools (some sources say 45+ auto-generated from the OpenAPI spec) that drive Inductive Automation Ignition's Gateway R |
| SIMATIC WinCC Unified | comm | https://github.com/vogler75/winccua-mcp-server | ~13 stars, 5 forks, 7 commits on main; JavaSc | Repo vogler75/winccua-mcp-server confirmed via WebFetch. Genuine MCP server (not a plain API wrapper): exposes 8 MCP tools — login-user, browse-objects, get-tag-values, get-logged- |
| OPC UA industrial systems | comm | https://github.com/kukapay/opcua-mcp | ~28 stars, 13 commits, Python 100% (kukapay o | WebFetch of canonical GitHub page confirms a genuine MCP server (not an API wrapper or chatbot). Exposes concrete MCP tools: read_opcua_node, write_opcua_node, browse nodes, read-m |
| OPC UA industrial data server | comm | https://github.com/kmanditereza/mcp-server-for-industrial-data | ~5 stars, 1 fork, single-commit main branch;  | Repo exists and is a genuine MCP server built with FastMCP that connects to industrial equipment over OPC UA. It exposes concrete MCP tools (e.g. get_material_availability, get_mac |
| Modbus | comm | https://github.com/kukapay/modbus-mcp | kukapay org — prolific MCP-server author (100 | Repo confirmed live via WebFetch. Genuine MCP server (Python, FastMCP-style) exposing 6 Modbus tools: read_register, write_register, read_coils, write_coil, read_input_registers, r |
| Modbus RTU/TCP master + slave | comm | https://github.com/alejoseb/ModbusMCP | ~1 star; actively maintained (v0.3.0 released | Repo exists and is a genuine MCP server built on FastMCP (>=0.2.0) + PyModbus 3.11.4. Exposes 20+ MCP tools across connection management, read/write ops, server (slave) lifecycle,  |
| OPC UA industrial systems | comm | https://github.com/midhunxavier/OPCUA-MCP | ~16 stars; Python (FastMCP) + TypeScript/Node | Repo exists and is a genuine MCP server (not a plain API wrapper or chatbot). Bridges MCP clients to any OPC UA server. Exposes concrete MCP tools: read/write single node, batch re |
| OPC UA industrial systems | comm | https://github.com/intigration/mcp-uaserver | 0 stars, 9 commits, Python 100%, MIT license  | WebFetch of the URL confirms the repo exists and is a genuine MCP server (Model Context Protocol) bridging AI agents to OPC UA industrial systems. Exposes 5 concrete MCP tools: rea |
| B&R Automation Studio | comm | https://github.com/AndrewMusser/br-automation-mcp | ~12 stars, 4 commits, Python; small/early-sta | WebFetch of the GitHub page confirms the repo exists and is a genuine MCP server (title: "An MCP server that enables AI assistants like Claude to interact with B&R Automation Studi |
| Victron ESS | comm | https://github.com/lubosstrejcek/victron-tcp | GitHub 1 star; active — v1.4.0 released 2026- | EXISTS and is a genuine MCP server (stdio, TypeScript, npm package victron-tcp) exposing 32 MCP tools + 23 prompts + 2 resources, built from the official CCGX Modbus TCP register l |
| Siemens TIA Portal | comm | https://github.com/feelautom/tia-copilot-genai-bridge | Listed on Glama (glama.ai/mcp/servers/feelaut | Repo EXISTS and is genuinely an MCP server. Branded "T-IA Connect" by feelautom (FeelAutom). Exposes 120+/126 MCP tools to drive TIA Portal via Siemens Openness API: explore projec |
| Ignition | **off** | https://inductiveautomation.com/news/inductive-automation-announces-mcp-module-during-2025-ignition-community-conference | Vendor press release dated 2025-09-17; ICC 20 | Vendor page confirmed to exist and load. Genuinely an MCP module, not a plain API wrapper or chatbot: it lets Ignition and its modules contribute MCP tools, resources, and prompts  |
| SIMATIC WinCC OA | **off** | https://github.com/winccoa/winccoa-ae-js-mcpserver | ~21 stars, 10 forks, 15 releases, latest v1.4 | Repo exists under the vendor's own winccoa GitHub org. Genuine MCP server exposing MCP tools: datapoints (read/write), OPC UA, MQTT, dashboards/widgets, alarms/archives, process ma |
| realvirtual.io | **off** | https://github.com/game4automation/io.realvirtual.mcp | ~12 stars; 100% C#; MIT; owned by game4automa | Repo confirmed public. Genuine MCP server (Unity Editor package, C#) exposing 60+ tools: simulation play/stop/pause, scene hierarchy, GameObject/component/transform manipulation, m |

## Digital Twin / Virtual Commissioning

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| Vector CANoe | comm | https://github.com/VectorCANoe/CANoe-mcp | ~2 stars, v1.0.0, last public activity 2026-0 | Repo exists and is public. Built on FastMCP + py-canoe + Windows COM to drive Vector CANoe; exposes 32 MCP tools across connection/config, CAPL compilation, measurement start/stop, |
| Vector CANoe | comm | https://github.com/rye00940094/canoe-mcp-debugger | Small/new public repo (created ~2026-06-09);  | WebFetch of the GitHub page confirms a genuine MCP server that drives CANoe via COM, exposing ~15 canoe_* MCP tools (canoe_status, canoe_open_configuration, canoe_compile_capl, can |

## Other

| Software | off/comm | MCP | Signal | Note |
|---|---|---|---|---|
| EnergyPlus | **off** | https://github.com/LBNL-ETA/EnergyPlus-MCP | GitHub ~103 stars, 22 forks, 15 commits, v0.1 | Canonical URL casing is LBNL-ETA/EnergyPlus-MCP (claimed lowercase resolves via GitHub case-insensitivity). Owned by Lawrence Berkeley National Lab Energy Technologies Area (github |