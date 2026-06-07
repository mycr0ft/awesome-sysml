# Awesome SysML v2

A curated list of SysML v2 language tools, implementations, samples, syntax highlighters, editors, commercial tools, and containerized versions.

## Contents

- [Reference & Pilot Implementations](#reference--pilot-implementations)
- [Language Servers & VS Code Extensions](#language-servers--vs-code-extensions)
- [Formatters, Linters & Style Checkers](#formatters-linters--style-checkers)
- [Parser Libraries & CLI Tools](#parser-libraries--cli-tools)
- [Python Tools](#python-tools)
- [.NET Tools](#net-tools)
- [Graphical Editors & Viewers](#graphical-editors--viewers)
- [Validation & Analysis](#validation--analysis)
- [Syntax Highlighting & Grammar Files](#syntax-highlighting--grammar-files)
- [Samples & Examples](#samples--examples)
- [Commercial Tools](#commercial-tools)
- [Containerized / Docker Images](#containerized--docker-images)
- [Tools by mycr0ft](#tools-by-mycr0ft)

---

## Reference & Pilot Implementations

| Tool | Description | Links |
|------|-------------|-------|
| **SysML v2 Pilot Implementation** | OMG's reference implementation — Java/Xtext-based parser, validator, textual editor, and PlantUML visualization. LGPL-3.0. | [github.com/Systems-Modeling/SysML-v2-Pilot-Implementation](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation) |
| **SysML v2 API Services** | Reference REST API server (Spring Boot) implementing the OMG SysML v2 API & Services specification. | [github.com/Systems-Modeling/SysML-v2-API-Services](https://github.com/Systems-Modeling/SysML-v2-API-Services) |
| **SysML v2 Release** | Official OMG release repo — spec documents, example models, model library, and installer instructions. | [github.com/Systems-Modeling/SysML-v2-Release](https://github.com/Systems-Modeling/SysML-v2-Release) |

## Language Servers & VS Code Extensions

| Tool | Author | Description | Links |
|------|--------|-------------|-------|
| **sysml-v2-lsp** | daltskin | Full LSP in TypeScript/ANTLR4 — diagnostics, completions, goto-def, references, rename, code actions, semantic tokens, folding, Mermaid preview (6 diagram types), MCP server. Clients: VS Code, Web SPA, Python/Jupyter. MIT. | [github.com/daltskin/sysml-v2-lsp](https://github.com/daltskin/sysml-v2-lsp) — `npm install sysml-v2-lsp` |
| **VSCode SysML Extension** | daltskin | Rich VS Code extension — 10 diagram views (General, IBD, Activity, State, Sequence, Package, etc.), Model Explorer, Feature Explorer, Feature Inspector, 29 snippets, model dashboard, inlay hints, PNG/SVG export. | [github.com/daltskin/VSCode_SysML_Extension](https://github.com/daltskin/VSCode_SysML_Extension) |
| **SysIDE Editor Legacy** | Sensmetry | Free LSP-based VS Code extension — semantic highlighting, autocompletion, validation, formatting, navigation, folding, rename, hover docs. Also: **Sysand** (open-source package manager), **Syside Modeler** (premium), **Syside Automator** (Python). | [github.com/sensmetry/sysml-2ls](https://github.com/sensmetry/sysml-2ls) — [syside.sensmetry.com](https://syside.sensmetry.com) |
| **sysmlv2-language-server** | vpathai | Langium-based LSP with 210+ validation rules, TextMate grammar, EMF compatibility shim. Built with Langium. | [github.com/vpathai-git/sysmlv2-language-server](https://github.com/vpathai-git/sysmlv2-language-server) |

## Formatters, Linters & Style Checkers

| Tool | Author | Description | Links |
|------|--------|-------------|-------|
| **sysml-style** | mycr0ft | SysML style checker and formatter based on sysmlpy. Enforces consistent code style on `.sysml` files. Python. | [github.com/mycr0ft/sysml-style](https://github.com/mycr0ft/sysml-style) |

## Parser Libraries & CLI Tools

| Tool | Language | Description | Links |
|------|----------|-------------|-------|
| **sysml-v2-parser** | Rust | Rust crate for parsing SysML v2/KerML textual syntax into AST. Resilient editor mode returns partial AST + diagnostics. | [crates.io/crates/sysml-v2-parser](https://crates.io/crates/sysml-v2-parser) |
| **sysml2 CLI** | C | Swiss-army-knife CLI — parse, validate, query (`--select`), modify (`--delete`/`--set`), JSON/SysML output. PEG parser with Clang-style diagnostics. | [github.com/zbigniewsobiecki/sysml2](https://github.com/zbigniewsobiecki/sysml2) |
| **sysml-reactflow** | TypeScript/React | Pure SysML v2.0 building blocks for React Flow — 60+ element types, 30+ edge types, viewpoint system, elkjs layout. | [github.com/Hollando78/SysML-reactflow](https://github.com/Hollando78/SysML-reactflow) |
| **Tessera** | Rust/Svelte | CLI + Tauri desktop app — tolerance analysis, BOM management, SysML v2 import/export round-trip. | [github.com/jackhale98/Tessera](https://github.com/jackhale98/Tessera) — [tessera-engineering.com](https://tessera-engineering.com) |

## Python Tools

| Tool | Author | Description | Install / Links |
|------|--------|-------------|-----------------|
| **sysmlpy** | mycr0ft | Pure Python ANTLR4-based parser — Pint units, NetworkX/Kuzu graph backends, in-memory/graph storage abstraction, 123/123 conformance. | `pip install sysmlpy` — [github.com/mycr0ft/sysmlpy](https://github.com/mycr0ft/sysmlpy) |
| **Windseeker** | Westfall-io | CLI for dependency analysis, Jupyter notebook generation/execution, SVG/PNG view extraction from `.sysml` files. | `pip install sysml-windseeker` — [github.com/Westfall-io/windseeker](https://github.com/Westfall-io/windseeker) |
| **sysmlcad** | mycr0ft | Embedding 3D CAD in SysML v2 for parametric models of physical objects. Python. | [github.com/mycr0ft/sysmlcad](https://github.com/mycr0ft/sysmlcad) |
| **sysml2py** | Westfall-io | Original textX-based Python parser (predecessor to sysmlpy). | `pip install sysml2py` — [github.com/Westfall-io/sysml2py](https://github.com/Westfall-io/sysml2py) |
| **Open-MBEE Python Client** | Open-MBEE | Client library for SysML v2 REST API (Flexo) — CRUD on projects, commits, branches, elements, tags. | [github.com/Open-MBEE/sysmlv2-python-client](https://github.com/Open-MBEE/sysmlv2-python-client) |
| **SYSMOD SysML v2 API + MCP** | Open-MBEE | Flask REST API + MCP server for SYSMOD models — problem statements, system ideas, contexts, stakeholders, requirements, use cases, feature trees, quality checks, AI wizard. | [github.com/Open-MBEE/sysmod-sysmlv2-api](https://github.com/Open-MBEE/sysmod-sysmlv2-api) |
| **Syside Automator** | Sensmetry | Commercial Python library — load/query/create/modify SysML v2 models, type hierarchies, JSON import/export, ReqIF export, Markdown docs. | `pip install syside` |
| **PySAM SysML2** | Ansys | Python scripting interface for SysML v2 models via Ansys SAM — browse, edit, sync back. MIT. | [github.com/ansys/pysam-sysml2](https://github.com/ansys/pysam-sysml2) — [sysml2.docs.pyansys.com](https://sysml2.docs.pyansys.com/) |
| **PySysML2** | DAF DTO | ANTLR4 Python parser — export to Pandas DataFrames, Excel, Graphviz, NumPy. Apache-2.0. | [github.com/nakane1chome/PySysML2](https://github.com/nakane1chome/PySysML2) |
| **mbse4u-sysml-helpers** | MBSE4U | Python helper library for SysML v2 API — element queries, caching, metadata. | `pip install mbse4u-sysml-helpers` |
| **sysml-v2-code-generator** | fcp89 | Flask web GUI for code generation from SysML v2 models. | `pip install fcp89-sysml-v2-code-generator-web-gui` |
| **sysmlv2-python-cookiecutter** | smp4 | Cookiecutter template — Hatch + VS Code + SysIDE + Jupyter kernel project scaffolding. | [github.com/smp4/sysmlv2-python-cookiecutter](https://github.com/smp4/sysmlv2-python-cookiecutter) |
| **daltskin LSP Python client** | daltskin | Zero-dep Python LSP client + Jupyter notebook — drives sysml-v2-lsp over stdio JSON-RPC. Ships with: | [github.com/daltskin/sysml-v2-lsp](https://github.com/daltskin/sysml-v2-lsp) (`clients/python/`) |
| **Refinery Validation Pipeline** | Zenodo | Pattern-based validation — Python pipeline fetching from SysML v2 API, transforming to Refinery graph solver, returning human-readable issues. | [zenodo.org/records/19297800](https://zenodo.org/records/19297800) |
| **Mgnite** | Mgnite Inc. | Commercial — JupyterLab + Python environment integrating SysML v2 with Excel, PowerPoint, MATLAB/Simulink, DOORS Next. | [omg.org/sysml/sysmlv2/sysml-tool](https://www.omg.org/sysml/sysmlv2/sysml-tool) |

## .NET Tools

| Tool | Description | Links |
|------|-------------|-------|
| **SysML2.NET** | C# SDK — core model, JSON/XMI/MessagePack serializers, REST/DAL clients, Docker image, live demo viewer. | [github.com/STARIONGROUP/SysML2.NET](https://github.com/STARIONGROUP/SysML2.NET) — [viewer.sysml2.net](http://viewer.sysml2.net) |

## Graphical Editors & Viewers

| Tool | Author | Description | Links |
|------|--------|-------------|-------|
| **Eclipse SysON** | Obeo / CEA | Open-source web-based graphical modeler built on Sirius Web. Drives Papyrus SysMLv2 & Capella co-design. | [github.com/eclipse-syson/syson](https://github.com/eclipse-syson/syson) — [doc.mbse-syson.org](https://doc.mbse-syson.org) |
| **Open-MBEE sysmlv2-web-modeler** | Open-MBEE | Standalone Java web service — graphical rendering + textual editing against any SysML v2 API backend. Dockerized. | [github.com/Open-MBEE/sysmlv2-web-modeler](https://github.com/Open-MBEE/sysmlv2-web-modeler) |
| **sysmlv2-gui** | DeciSym | Native desktop + WASM web graphical viewer — Rust/egui, reads `.sysml` files, renders OMG-specified graphical notation. | [github.com/DeciSym/sysmlv2-gui](https://github.com/DeciSym/sysmlv2-gui) |
| **Tom Sawyer SysML v2 Viewer** | Tom Sawyer | Model visualization — auto-layout, interactive navigation, integrates with any SysML v2 API repo. | [omg.org/sysml/sysmlv2/sysml-tool](https://www.omg.org/sysml/sysmlv2/sysml-tool) |

## Validation & Analysis

| Tool | Author | Description | Links |
|------|--------|-------------|-------|
| **Refinery Validation Pipeline** | Zenodo | Pattern-based validation — connects to SysML v2 API, transforms to Refinery graph solver, runs user-defined patterns. Docker Compose showcase. | [zenodo.org/records/19297800](https://zenodo.org/records/19297800) |
| **SYSMOD MCP Server** | Open-MBEE | 17 MCP tools for querying SYSMOD artifacts — quality checks, atlas, feature trees, AI suggestions. | [github.com/Open-MBEE/sysmod-sysmlv2-api](https://github.com/Open-MBEE/sysmod-sysmlv2-api) |
| **cameo-mcp-bridge** | ajhcs | MCP server bridging AI assistants to CATIA Magic/Cameo — 37 tools for query, create, modify, diagram operations on SysML/UML models. | [github.com/ajhcs/cameo-mcp-bridge](https://github.com/ajhcs/cameo-mcp-bridge) |

## Syntax Highlighting & Grammar Files

| Resource | Description | Links |
|----------|-------------|-------|
| **daltskin/sysml-v2-grammar** | ANTLR4 grammar files for SysML v2 and KerML. | [github.com/daltskin/sysml-v2-grammar](https://github.com/daltskin/sysml-v2-grammar) |
| **vpathai TextMate grammar** | TextMate grammar bundled in the sysmlv2-language-server. | [github.com/vpathai-git/sysmlv2-language-server](https://github.com/vpathai-git/sysmlv2-language-server) (`sysml_resources/`) |
| **Pilot Xtext grammar** | Reference grammar in the Pilot Implementation (Eclipse Xtext `.xtext` files). | [Systems-Modeling/SysML-v2-Pilot-Implementation](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation) |
| **pygments-sysml** | SysML lexer for syntax highlighting with Pygments. Python. | [github.com/mycr0ft/pygments-sysml](https://github.com/mycr0ft/pygments-sysml) |
| **sysml-vim** | Vim syntax highlighting for SysML v2 textual notation. Vim Script. | [github.com/mycr0ft/sysml-vim](https://github.com/mycr0ft/sysml-vim) |

## Samples & Examples

| Resource | Description | Links |
|----------|-------------|-------|
| **SysML v2 Release examples** | Official OMG example models (KerML and SysML v2). | [github.com/Systems-Modeling/SysML-v2-Release](https://github.com/Systems-Modeling/SysML-v2-Release) (`kerml/`, `sysml/`) |
| **sysml-v2-lsp examples** | 20+ example `.sysml` files including bike, smart-home, DFA coverage, multiplicity. | [github.com/daltskin/sysml-v2-lsp/tree/main/examples](https://github.com/daltskin/sysml-v2-lsp/tree/main/examples) |
| **sysml2 CLI examples** | Example models for the Swiss-army-knife CLI. | [github.com/zbigniewsobiecki/sysml2](https://github.com/zbigniewsobiecki/sysml2) |
| **SysML v2 Pilot examples** | Example projects shipped with the Pilot Implementation. | [Systems-Modeling/SysML-v2-Pilot-Implementation](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation) |
| **SysML v2 Standard Library** | Normative model libraries (Kernel, Domain, Systems libraries). | [github.com/Systems-Modeling/SysML-v2-Release](https://github.com/Systems-Modeling/SysML-v2-Release) (`sysml.library/`) |
| **Visual Paradigm examples** | 500+ professional example files (satellite, automotive, camera, turbojet). | [sysml.visual-paradigm.com](https://sysml.visual-paradigm.com/) |

## Commercial Tools

| Tool | Vendor | Notes |
|------|--------|-------|
| **CATIA SysML v2** (Magic/Cameo) | Dassault Systèmes | 100% spec-conformant, bidirectional text↔diagram sync, Teamwork Cloud, REST API, Community Edition free. |
| **Systems Modeler with SysMLv2** | Siemens | Web-based collaborative, Teamcenter PLM integration, REST/OSLC/API. |
| **Simcenter Studio** | Siemens | Architecture generation + evaluation, Python, ML-based trade studies. |
| **Ansys SysML v2** (SAM) | Ansys / Synopsys | Cloud-native, real-time collab, config mgmt, time-dynamic execution. |
| **Davinci** | Celedon | SysML v2 + CAD generation + document authoring + code synthesis. |
| **Syndeia** | InterCAX | Digital thread platform — connect SysML v2 to requirements, SW, HW, V&V, manufacturing. |
| **SysML v2 Studio** | Visual Paradigm | Web-based, AI-powered code gen, 500+ examples, real-time diagram sync. |
| **PTC Modeler** | PTC | UML/UAF/SysML 1&2, Codebeamer/Windchill integrations, variability mgmt. |
| **SysGit** | SysGit | Git-based infrastructure, textual + graphical editing, DevOps integration. |
| **TEAMS Toolset** | QSI | Import SysML v2 for FMEA/FMECA/FTA, diagnostics/prognostics, digital twin. |
| **Violet Labs Integration** | Violet Labs | Digital thread between SysML v2 and CAD/PLM/ERP/hardware tools. |
| **Mgnite** | Mgnite Inc. | JupyterLab + Python integration with Excel, PowerPoint, MATLAB/Simulink, DOORS Next. |
| **Syside Modeler** | Sensmetry | Premium SysML v2 modeling environment. |
| **Syside Automator** | Sensmetry | Python library for analysis, optimization, and workflow automation. |

## Containerized / Docker Images

| Image | Description |
|-------|-------------|
| `mbsemashup/sysmlv2-api.pilotimpl` | Containerized SysML v2 API Services pilot implementation. |
| `gorenje/sysmlv2-jupyter` | Jupyter + SysML v2 kernel + API server Docker setup. |
| `jaydeanmartin/sysmlv2` | Docker Compose for Jupyter + API server + PostgreSQL. |
| `kenji-miyake/sysml-v2-docker/eclipse` | Eclipse with SysML v2 Pilot (Xtext editor) — containerized desktop. |
| `josh-kaplan/sysml-v2-docker` | Docker Compose for SysML 2.0 lab (Jupyter). |
| **Open-MBEE sysmlv2-web-modeler** | Dockerfile + Dockerfile.openmbee — Java service with Pilot JARs, Graphviz, Python bundled. |
| **DeciSym sysmlv2-gui** | Dockerfile — WASM frontend + Java validator bundled. |
| **Refinery Validation Showcase** | docker-compose.yml — Web UI + Jupyter + API + PostgreSQL. |
| **SysML2.NET** | Docker Hub image — reference web-application at viewer.sysml2.net. |
| **mycr0ft/sysmlv2-jupyter-container** | Docker container for SysML v2 Jupyter + API + PostgreSQL. |
| **mycr0ft/SysON_podman_compose** | Podman Compose setup for Eclipse SysON. |

## Tools by mycr0ft

Jon Fox ([github.com/mycr0ft](https://github.com/mycr0ft)) maintains these SysML v2 projects:

| Repo | Description |
|------|-------------|
| **sysmlpy** | Pure Python SysML v2 parser — ANTLR4 grammar, Pint units, NetworkX/Kuzu graph backends, 123/123 conformance. PyPI: `pip install sysmlpy`. |
| **sysmlcad** | Embedding 3D CAD in SysML v2 for parametric models of physical objects. Python. |
| **sysml-style** | SysML style checker and formatter based on sysmlpy. Enforces consistent code style on `.sysml` files. |
| **pygments-sysml** | SysML lexer for syntax highlighting with Pygments. |
| **sysml-vim** | Vim syntax highlighting for SysML v2 textual notation. |
| **sysmlv2-jupyter-container** | Docker container for SysML v2 Jupyter + API server + PostgreSQL — Docker Compose based. |
| **SysON_podman_compose** | Podman Compose setup for Eclipse SysON web-based graphical modeler. |

Contributions also in: **Windseeker** ([Westfall-io/windseeker](https://github.com/Westfall-io/windseeker)) — CLI for dependency analysis and view extraction.

---

## Contributing

Submit a PR or open an issue at [github.com/mycr0ft/awesome-sysml](https://github.com/mycr0ft/awesome-sysml).
