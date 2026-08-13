# Awesome SysML V2 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of SysML v2 language tools, implementations, samples, syntax highlighters, editors, commercial tools, and containerized versions.

## Contents

- [Documentation & Standards](#documentation--standards)
- [Reference & Pilot Implementations](#reference--pilot-implementations)
- [Language Servers & VS Code Extensions](#language-servers--vs-code-extensions)
- [Formatters, Linters & Style Checkers](#formatters-linters--style-checkers)
- [Parser Libraries & CLI Tools](#parser-libraries--cli-tools)
- [Python Tools](#python-tools)
- [.NET Tools](#net-tools)
- [Graphical Editors & Viewers](#graphical-editors--viewers)
- [Validation & Analysis](#validation--analysis)
- [Syntax Highlighting & Grammar Files](#syntax-highlighting--grammar-files)
- [Samples, Examples & Training](#samples-examples--training)
- [Commercial Tools](#commercial-tools)
- [Containerized / Docker Images](#containerized--docker-images)
- [Tools by mycr0ft](#tools-by-mycr0ft)

---

## Documentation & Standards

- [sysml-v2-docs](https://github.com/voidaliot/sysml-v2-docs) - Pure markdown knowledge base extracted from OMG SysML v2.0 / KerML 1.0 / API & Services 1.0 specs. Covers the full language (overview, grammar, keywords, definition vs usage, structural/behavioral/requirements modeling, analysis, packages, standard libraries, graphical notation), AI agent guidance, validation checklists, and example `.sysml` files (flashlight, vehicle skeleton). Designed for both developers and AI coding agents.

## Reference & Pilot Implementations

- [SysML v2 Pilot Implementation](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation) - OMG's reference implementation — Java/Xtext-based parser, validator, textual editor, and PlantUML visualization. **Memory-heavy JVM runtime — 16 GB host RAM recommended.** LGPL-3.0.
- [SysML v2 API Services](https://github.com/Systems-Modeling/SysML-v2-API-Services) - Reference REST API server (Spring Boot) implementing the OMG SysML v2 API & Services specification. **Spring Boot JVM — 16 GB host RAM recommended.**
- [SysML v2 Release](https://github.com/Systems-Modeling/SysML-v2-Release) - Official OMG release repo — spec documents, example models, model library, and installer instructions.

## Language Servers & VS Code Extensions

- [sysml-v2-lsp](https://github.com/daltskin/sysml-v2-lsp) - Full LSP in TypeScript/ANTLR4 — diagnostics, completions, goto-def, references, rename, code actions, semantic tokens, folding, Mermaid preview (6 diagram types), MCP server. Clients: VS Code, Web SPA, Python/Jupyter. MIT. `npm install sysml-v2-lsp`.
- [VSCode SysML Extension](https://github.com/daltskin/VSCode_SysML_Extension) - Rich VS Code extension — 10 diagram views (General, IBD, Activity, State, Sequence, Package, etc.), Model Explorer, Feature Explorer, Feature Inspector, 29 snippets, model dashboard, inlay hints, PNG/SVG export.
- [SysIDE Editor Legacy](https://github.com/sensmetry/sysml-2ls) - Free LSP-based VS Code extension — semantic highlighting, autocompletion, validation, formatting, navigation, folding, rename, hover docs. Also: **Sysand** (open-source package manager), **Syside Modeler** (premium), **Syside Automator** (Python). [Site](https://syside.sensmetry.com).
- [sysmlv2-language-server](https://github.com/vpathai-git/sysmlv2-language-server) - Langium-based LSP with 210+ validation rules, TextMate grammar, EMF compatibility shim. Built with Langium.

## Formatters, Linters & Style Checkers

- [sysml-style](https://github.com/mycr0ft/sysml-style) - SysML style checker and formatter based on sysmlpy. Enforces consistent code style on `.sysml` files. Python.

## Parser Libraries & CLI Tools

- [sysml-v2-parser](https://crates.io/crates/sysml-v2-parser) - Rust crate for parsing SysML v2/KerML textual syntax into AST. Resilient editor mode returns partial AST + diagnostics.
- [sysml2 CLI](https://github.com/zbigniewsobiecki/sysml2) - Swiss-army-knife CLI — parse, validate, query (`--select`), modify (`--delete`/`--set`), JSON/SysML output. PEG parser with Clang-style diagnostics.
- [sysml-reactflow](https://github.com/Hollando78/SysML-reactflow) - Pure SysML v2.0 building blocks for React Flow — 60+ element types, 30+ edge types, viewpoint system, elkjs layout. TypeScript/React.
- [Tessera](https://github.com/jackhale98/Tessera) - CLI + Tauri desktop app — tolerance analysis, BOM management, SysML v2 import/export round-trip. Rust/Svelte. [Site](https://tessera-engineering.com).

## Python Tools

- [sysmlpy](https://github.com/mycr0ft/sysmlpy) - Pure Python ANTLR4-based parser — Pint units, NetworkX/Kuzu graph backends, in-memory/graph storage abstraction, 123/123 conformance. `pip install sysmlpy`.
- [Windseeker](https://github.com/Westfall-io/windseeker) - CLI for dependency analysis, Jupyter notebook generation/execution, SVG/PNG view extraction from `.sysml` files. `pip install sysml-windseeker`.
- [SysML v2 Visualizer](https://github.com/redasasin4/SysML_Python_Visualizer) - Python CLI driving the official `jupyter-sysml-kernel` to render authentic SVG diagrams (Tree, Interconnection, Action, State, Sequence, Case, MIXED) from `.sysml` files. Auto-discovers kernel; ships Python API, `--diagnose`, and GitHub Actions integration. UV-managed. **Drives the in-process SysML kernel JVM — same ≥ 16 GB host RAM guidance applies.**
- [sysmlcad](https://github.com/mycr0ft/sysmlcad) - Embedding 3D CAD in SysML v2 for parametric models of physical objects. Python.
- [sysml2py](https://github.com/Westfall-io/sysml2py) - Original textX-based Python parser (predecessor to sysmlpy). `pip install sysml2py`.
- [Open-MBEE Python Client](https://github.com/Open-MBEE/sysmlv2-python-client) - Client library for SysML v2 REST API (Flexo) — CRUD on projects, commits, branches, elements, tags.
- [SYSMOD SysML v2 API + MCP](https://github.com/Open-MBEE/sysmod-sysmlv2-api) - Flask REST API + MCP server for SYSMOD models — problem statements, system ideas, contexts, stakeholders, requirements, use cases, feature trees, quality checks, AI wizard.
- [Syside Automator](https://pypi.org/project/syside/) - Commercial Python library — load/query/create/modify SysML v2 models, type hierarchies, JSON import/export, ReqIF export, Markdown docs. `pip install syside`.
- [PySAM SysML2](https://github.com/ansys/pysam-sysml2) - Python scripting interface for SysML v2 models via Ansys SAM — browse, edit, sync back. MIT. [Docs](https://sysml2.docs.pyansys.com/).
- [PySysML2](https://github.com/nakane1chome/PySysML2) - ANTLR4 Python parser — export to Pandas DataFrames, Excel, Graphviz, NumPy. Apache-2.0.
- [mbse4u-sysml-helpers](https://pypi.org/project/mbse4u-sysml-helpers/) - Python helper library for SysML v2 API — element queries, caching, metadata. `pip install mbse4u-sysml-helpers`.
- [sysml-v2-code-generator](https://pypi.org/project/fcp89-sysml-v2-code-generator-web-gui/) - Flask web GUI for code generation from SysML v2 models. `pip install fcp89-sysml-v2-code-generator-web-gui`.
- [sysmlv2-python-cookiecutter](https://github.com/smp4/sysmlv2-python-cookiecutter) - Cookiecutter template — Hatch + VS Code + SysIDE + Jupyter kernel project scaffolding.
- [daltskin LSP Python client](https://github.com/daltskin/sysml-v2-lsp/tree/main/clients/python) - Zero-dep Python LSP client + Jupyter notebook — drives sysml-v2-lsp over stdio JSON-RPC.
- [Refinery Validation Pipeline](https://zenodo.org/records/19297800#files) - Pattern-based validation — Python pipeline fetching from SysML v2 API, transforming to Refinery graph solver, returning human-readable issues.

## .NET Tools

- [SysML2.NET](https://github.com/STARIONGROUP/SysML2.NET) - C# SDK — core model, JSON/XMI/MessagePack serializers, REST/DAL clients, Docker image, live demo viewer. [Viewer](http://viewer.sysml2.net).

## Graphical Editors & Viewers

- [Eclipse SysON](https://github.com/eclipse-syson/syson) - Open-source web-based graphical modeler built on Sirius Web. Drives Papyrus SysMLv2 & Capella co-design. [Docs](https://doc.mbse-syson.org).
- [Open-MBEE sysmlv2-web-modeler](https://github.com/Open-MBEE/sysmlv2-web-modeler) - Standalone Java web service — graphical rendering + textual editing against any SysML v2 API backend. Dockerized.
- [sysmlv2-gui](https://github.com/DeciSym/sysmlv2-gui) - Native desktop + WebAssembly web graphical viewer — Rust/egui, reads `.sysml` files, renders OMG-specified graphical notation.
- [Tom Sawyer SysML v2 Viewer](https://www.omg.org/sysml/sysmlv2/sysml-tool) - Model visualization — auto-layout, interactive navigation, integrates with any SysML v2 API repo.

## Validation & Analysis

- [Refinery Validation Pipeline](https://zenodo.org/records/19297800) - Pattern-based validation — connects to SysML v2 API, transforms to Refinery graph solver, runs user-defined patterns. Docker Compose showcase.
- [SYSMOD MCP Server](https://github.com/Open-MBEE/sysmod-sysmlv2-api/tree/main/mcp) - 17 MCP tools for querying SYSMOD artifacts — quality checks, atlas, feature trees, AI suggestions.
- [cameo-mcp-bridge](https://github.com/ajhcs/cameo-mcp-bridge) - MCP server bridging AI assistants to CATIA Magic/Cameo — 37 tools for query, create, modify, diagram operations on SysML/UML models.

## Syntax Highlighting & Grammar Files

- [daltskin/sysml-v2-grammar](https://github.com/daltskin/sysml-v2-grammar) - ANTLR4 grammar files for SysML v2 and KerML.
- [vpathai TextMate grammar](https://github.com/vpathai-git/sysmlv2-language-server/tree/main/sysml_resources) - TextMate grammar bundled in the sysmlv2-language-server (`sysml_resources/`).
- [Pilot Xtext grammar](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation/tree/main/releng/org.omg.sysml.xtext) - Reference grammar in the Pilot Implementation (Eclipse Xtext `.xtext` files).
- [pygments-sysml](https://github.com/mycr0ft/pygments-sysml) - SysML lexer for syntax highlighting with Pygments. Python.
- [sysml-vim](https://github.com/mycr0ft/sysml-vim) - Vim syntax highlighting for SysML v2 textual notation. Vim Script.

## Samples, Examples & Training

- [SysML v2 Release examples](https://github.com/Systems-Modeling/SysML-v2-Release/tree/main/sysml) - Official OMG example models (KerML and SysML v2) — the canonical starting point (`kerml/`, `sysml/`).
- [GfSE SysML v2 Models](https://github.com/GfSE/SysML-v2-Models) - GfSE-curated collection of high-quality SysML v2 models — validated in CI via the Pilot Implementation parser. Covers SE models, EveOnline mining frigate, family model, SOS, and more. BSD-3-Clause.
- [Airbus Apollo 11 SysML v2](https://github.com/airbus/apollo-11-sysml-v2) - Comprehensive SysML v2 model of the Apollo 11 mission by Airbus Central R&T. Uses the 5-layer CoSMA framework (Purpose/Operational/Functional/Logical/Technical) with full requirements traceability, analysis calculations, state machines, and mission execution modeling. Research artifact with accompanying INCOSE paper.
- [Don't Panic Batmobile](https://github.com/MBSE4U/dont-panic-batmobile) - Batmobile SysML v2 example from the book "Don't Panic - The Absolute Beginners Guide to SysML v2" by Tim Weilkiens and Christian Muggeo. Includes `.sysml` textual notation and Jupyter notebook. Apache-2.0.
- [SysML v2 Standard Library](https://github.com/Systems-Modeling/SysML-v2-Release/tree/main/sysml.library) - Normative model libraries (Kernel, Domain, Systems libraries) (`sysml.library/`).
- [SysML v2 Intro Presentations](https://github.com/Systems-Modeling/SysML-v2-Release/tree/main/doc) - Official OMG intro PDFs for both textual and graphical notation (`doc/`).
- [Flashlight Starter Model](https://www.omgwiki.org/MBSE/doku.php?id=mbse:sysml_v2_transition:sysml_v2_starter_model) - OMG starter model by Sanford Friedenthal — simple flashlight in Jupyter + PlantUML. Updated for the SysML v2 2025-04 spec release. Model organization (Requirements, Actions, Parts, Requirements Allocation), requirements tree, action tree, parts tree, on/off states. ([.sysml](https://de-bok.org/asset/39898415908a48350628209d59522add76acdfd1) · [.ipynb](https://de-bok.org/asset/4b8e819b5446ad999551e7d68c625e7d75f83f9f) · [Overview](https://www.de-bok.org/asset/45a09d62209810afce38cfa49a5a95d01d2fc2e7)).
- [SysON Flashlight Tutorial](https://docs.obeosoft.com/syson/v2025.6.0/user-manual/hands-on/tutorials/flashlight.html) - Obeo's beginner-friendly step-by-step SysML v2 tutorial (Flashlight model).
- [SysML v2 Learning Club](https://clubs.oose.com/courses/sysmlv2/) - OOSE's 107-lesson microlearning course — bite-sized units with exercises and quizzes.
- [Advent of SysML v2](https://github.com/sensmetry/advent-of-sysml-v2) - Sensmetry's 24-lesson video course with YouTube playlist, blog posts, and example models. ([YouTube](https://www.youtube.com/playlist?list=PLuceG5piNwHG7KBdo02RDPAkJ-ErbzHe0)).
- [SysML Cheatsheet](https://sensmetry.com/sysml-cheatsheet/) - Sensmetry's quick-reference cheat sheet for SysML v2 syntax.
- [SysML Syntax Explorer](https://cst.syside.app/) - Interactive browser-based concrete syntax tree (CST) visualizer. ([Docs](https://docs.sensmetry.com/automator/tree-sitter-playground.html)).
- [Visual Paradigm 8-View Guide](https://sysml.visual-paradigm.com/docs/sysml-v2-studio-kick-start-guide/cohesive-system-model-in-8-views/overview/) - 9-part tutorial series building a Smart Home Climate System end-to-end.
- [Visual Paradigm Tutorials](https://sysml.visual-paradigm.com/docs/tutorials/part-1-the-basics-your-first-model/creating-your-first-sysml-v2-project/) - Getting started, parts & ports, industry examples (EV Charging Station, Turbojet, Camera).
- [Visual Paradigm Examples](https://sysml.visual-paradigm.com/) - 500+ professional example files (satellite, automotive, camera, turbojet) with AI explanations.
- [sysml-v2-lsp examples](https://github.com/daltskin/sysml-v2-lsp/tree/main/examples) - 20+ example `.sysml` files including bike, smart-home, DFA coverage, multiplicity.
- [SysML v2 Pilot examples](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation/tree/main/examples) - Example projects shipped with the Pilot Implementation.
- [sysml2 CLI examples](https://github.com/zbigniewsobiecki/sysml2/tree/main/examples) - Example models for the Swiss-army-knife CLI.
- [Armstrong Process Group Tutorial](https://aprocessgroup.com/sysml-v2-tutorial/) - Half-day SysML v2 overview — language architecture, structure, behavior, requirements.
- [Caltech CTME Training](https://ctme.caltech.edu/transitioning-models-to-sysml-v2-with-mbse.html) - 3-day professional transition training from SysML v1 to v2 with Cameo.
- [Webel IT Australia Workshop](https://webel.com.au/node/4399) - 5-day full SysML v2 workshop with Cameo/CATIA Magic, Balls & Boxes sample problem.

## Commercial Tools

- [CATIA SysML v2 (Magic/Cameo)](https://www.3ds.com/products-services/catia/products/sysml-v2/) - Dassault Systèmes. 100% spec-conformant, bidirectional text↔diagram sync, Teamwork Cloud, REST API, Community Edition free.
- [Systems Modeler with SysMLv2](https://www.siemens.com/en-us/products/teamcenter/) - Siemens. Web-based collaborative, Teamcenter PLM integration, REST/OSLC/API.
- [Simcenter Studio](https://www.siemens.com/en-us/products/simcenter/) - Siemens. Architecture generation + evaluation, Python, ML-based trade studies.
- [Ansys SysML v2 (SAM)](https://www.ansys.com/products/connect/ansys-system-architecture-modeler) - Ansys / Synopsys. Cloud-native, real-time collab, config mgmt, time-dynamic execution.
- [Davinci](https://celedon.solutions/davinci/) - Celedon. SysML v2 + CAD generation + document authoring + code synthesis.
- [Syndeia](https://intercax.com/products/syndeia) - InterCAX. Digital thread platform — connect SysML v2 to requirements, SW, HW, V&V, manufacturing.
- [SysML v2 Studio](https://www.visual-paradigm.com/features/sysml-v2/) - Visual Paradigm. Web-based, AI-powered code gen, 500+ examples, real-time diagram sync.
- [PTC Modeler](https://www.ptc.com/en/products/ptc-modeler) - PTC. UML/UAF/SysML 1&2, Codebeamer/Windchill integrations, variability mgmt.
- [SysGit](https://www.sysgit.io/) - Git-based infrastructure, textual + graphical editing, DevOps integration for SysML v2 models.
- [TEAMS Toolset](https://www.teamqsi.com/products/) - Qualtech Systems (QSI). Import SysML v2 for FMEA/FMECA/FTA, diagnostics/prognostics, digital twin.
- [Violet Labs Integration](https://www.violetlabs.com/) - Violet Labs. Digital thread between SysML v2 and CAD/PLM/ERP/hardware tools.
- [Mgnite](https://www.mgnite.com/) - JupyterLab + Python environment integrating SysML v2 with Excel, PowerPoint, MATLAB/Simulink, DOORS Next.
- [Syside Modeler](https://sensmetry.com/syside/) - Sensmetry. Premium SysML v2 modeling environment.
- [Syside Automator](https://docs.sensmetry.com/automator/) - Sensmetry. Python library for analysis, optimization, and workflow automation.

## Containerized / Docker Images

> **⚠️ Memory note:** Images based on the SysML v2 Pilot / API Services (`gorenje/sysmlv2-jupyter`, `josh-kaplan/sysml-v2-docker`, `jaydeanmartin/sysmlv2`, `mbsemashup/sysmlv2-api.pilotimpl`, `mycr0ft/sysmlv2-jupyter-container`, `kenji-miyuke/sysml-v2-docker/eclipse`, `Open-MBEE sysmlv2-web-modeler`, `DeciSym sysmlv2-gui`, `Refinery Validation Showcase`) bundle a JVM and often a Spring Boot server alongside JupyterLab/Eclipse. Combined overhead routinely exceeds 8 GB — run them on hosts with ≥ 16 GB RAM (preferably more when also running PostgreSQL). Containerizing is a good way to keep host deps clean, but plan host memory accordingly.

- [mbsemashup/sysmlv2-api.pilotimpl](https://hub.docker.com/r/mbsemashup/sysmlv2-api.pilotimpl) - Containerized SysML v2 API Services pilot implementation.
- [gorenje/sysmlv2-jupyter](https://hub.docker.com/r/gorenje/sysmlv2-jupyter) - Jupyter + SysML v2 kernel + API server Docker setup. ([GitHub](https://github.com/gorenje/sysmlv2-jupyter)).
- [jaydeanmartin/sysmlv2](https://github.com/jaydeanmartin/sysmlv2) - Docker Compose for Jupyter + API server + PostgreSQL.
- [kenji-miyuke/sysml-v2-docker/eclipse](https://github.com/kenji-miyake/sysml-v2-docker) - Eclipse with SysML v2 Pilot (Xtext editor) — containerized desktop.
- [josh-kaplan/sysml-v2-docker](https://github.com/josh-kaplan/sysml-v2-docker) - Docker Compose for SysML 2.0 lab (Jupyter).
- [Open-MBEE sysmlv2-web-modeler](https://github.com/Open-MBEE/sysmlv2-web-modeler/blob/main/Dockerfile) - Dockerfile + Dockerfile.openmbee — Java service with Pilot JARs, Graphviz, Python bundled.
- [DeciSym sysmlv2-gui](https://github.com/DeciSym/sysmlv2-gui/blob/main/Dockerfile) - Dockerfile — WebAssembly frontend + Java validator bundled.
- [Refinery Validation Showcase](https://zenodo.org/records/19297800/files/docker-compose.yml) - Docker Compose configuration — Web UI + Jupyter + API + PostgreSQL.
- [SysML2.NET](https://hub.docker.com/r/stariongroup/sysml2.net) - Docker Hub image — reference web-application. ([Viewer](http://viewer.sysml2.net)).
- [mycr0ft/sysmlv2-jupyter-container](https://github.com/mycr0ft/sysmlv2-jupyter-container) - Docker container for SysML v2 Jupyter + API + PostgreSQL.
- [mycr0ft/SysON_podman_compose](https://github.com/mycr0ft/SysON_podman_compose) - Podman Compose setup for Eclipse SysON.

## Tools by mycr0ft

This list's maintainer, Jon Fox ([github.com/mycr0ft](https://github.com/mycr0ft)), maintains the
**sysmlpy**, **sysmlcad**, **sysml-style**, **pygments-sysml**, **sysml-vim**,
**sysmlv2-jupyter-container**, and **SysON_podman_compose** projects indexed above — and also
contributes to the **Windseeker** CLI listed under Python Tools.

---

## Contributing

Submit a PR or open an issue at [github.com/mycr0ft/awesome-sysml](https://github.com/mycr0ft/awesome-sysml).
