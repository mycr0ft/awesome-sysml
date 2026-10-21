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
- [SysML v1 to v2 Migration](#sysml-v1-to-v2-migration)
- [Product Data & Digital Thread](#product-data--digital-thread)
- [Project Templates & Scaffolding](#project-templates--scaffolding)
- [Validation & Analysis](#validation--analysis)
- [Syntax Highlighting & Grammar Files](#syntax-highlighting--grammar-files)
- [Samples, Examples & Training](#samples-examples--training)
- [Commercial Tools](#commercial-tools)
- [Containerized / Docker Images](#containerized--docker-images)
- [Other Resources](#other-resources)
- [Maintainer's Projects](#maintainers-projects)

---

## Documentation & Standards

- [sysml-v2-docs](https://github.com/voidaliot/sysml-v2-docs) - Pure markdown knowledge base extracted from OMG SysML v2.0 / KerML 1.0 / API & Services 1.0 specs. Covers the full language (overview, grammar, keywords, definition vs usage, structural/behavioral/requirements modeling, analysis, packages, standard libraries, graphical notation), AI agent guidance, validation checklists, and example `.sysml` files (flashlight, vehicle skeleton). Designed for both developers and AI coding agents.
- [SysML v2 API Cookbook](https://github.com/Systems-Modeling/SysML-v2-API-Cookbook) - Official recipes for using the SysML v2 REST API — project/commit navigation, element queries, and common client workflows.
- [SysML v2 AADL Library](https://github.com/Systems-Modeling/SysML-v2-AADL-Release) - OMG release repository for the SysML v2 library for AADL — architecture-exchange vocabulary for AADL models.
- [OMG SysML v2 specification](https://www.omg.org/spec/SysML/2.0/) - The normative language specification, KerML, and the Systems Modeling API & Services specification.

## Reference & Pilot Implementations

- [SysML v2 Pilot Implementation](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation) - OMG's reference implementation — Java/Xtext-based parser, validator, textual editor, and PlantUML visualization. **Memory-heavy JVM runtime — 16 GB host RAM recommended.** LGPL-3.0.
- [SysML v2 API Services](https://github.com/Systems-Modeling/SysML-v2-API-Services) - Reference REST API server (Spring Boot) implementing the OMG SysML v2 API & Services specification. **Spring Boot JVM — 16 GB host RAM recommended.**
- [sysmlpy-api-services](https://github.com/mycr0ft/sysmlpy-api-services) - Python implementation of the same specification on Flask-RESTX + sysmlpy — spec-canonical `/projects/{pid}/commits/{cid}` route space, EJSON element shape, commit-scoped versioning, branches, tags, queries, and DataVersion change records. 36 spec-alignment tests with a published gap list. MIT.
- [OpenSysML](https://github.com/Open-MBEE/OpenSysML) - Open-source SysML v2 implementation in Go from Open-MBEE. Apache-2.0.
- [SysML v2 Release](https://github.com/Systems-Modeling/SysML-v2-Release) - Official OMG release repo — spec documents, example models, model library, and installer instructions.

## Language Servers & VS Code Extensions

- [sysml-v2-lsp](https://github.com/daltskin/sysml-v2-lsp) - Full LSP in TypeScript/ANTLR4 — diagnostics, completions, goto-def, references, rename, code actions, semantic tokens, folding, Mermaid preview (6 diagram types), MCP server. Clients: VS Code, Web SPA, Python/Jupyter. MIT. `npm install sysml-v2-lsp`.
- [VSCode SysML Extension](https://github.com/daltskin/VSCode_SysML_Extension) - Rich VS Code extension — 10 diagram views (General, IBD, Activity, State, Sequence, Package, etc.), Model Explorer, Feature Explorer, Feature Inspector, 29 snippets, model dashboard, inlay hints, PNG/SVG export.
- [sysmlv2-language-server](https://github.com/vpathai-git/sysmlv2-language-server) - Langium-based LSP with 210+ validation rules, TextMate grammar, EMF compatibility shim.
- [spec42](https://github.com/elan8/spec42) - SysML v2 language server and VS Code extension. MIT.
- [sysand](https://github.com/sensmetry/sysand) - Package manager for SysML v2 and KerML projects — dependency resolution and project packaging.

## Formatters, Linters & Style Checkers

- [sysml-style](https://github.com/mycr0ft/sysml-style) - SysML v2 style checker and formatter built on sysmlpy — 30+ rule codes across naming, structure, imports, documentation and idioms, with auto-fix for the mechanical ones. `pip install sysml-style`. MPL-2.0.

## Parser Libraries & CLI Tools

- [sysml2 CLI](https://github.com/zbigniewsobiecki/sysml2) - Swiss-army-knife CLI — parse, validate, query (`--select`), modify (`--delete`/`--set`), JSON/SysML output. PEG parser with Clang-style diagnostics.
- [gosysml](https://github.com/mycr0ft/gosysml) - Go parser for the SysML v2 textual notation — the ANTLR4 grammar compiled to Go, a typed grammar tree (~240 structs) with round-trip text emission, and opt-in partial-parse recovery. MPL-2.0.
- [MontiCore SysML v2](https://github.com/MontiCore/sysmlv2) - MontiCore implementation of the SysML v2 textual notation — grammar modules and generated tooling from RWTH Aachen.
- [sysml-v2-parser](https://github.com/elan8/sysml-v2-parser) - Rust crate (`sysml-v2-parser`) for parsing SysML v2/KerML textual syntax into AST. Resilient editor mode returns partial AST + diagnostics.
- [sysml-reactflow](https://github.com/Hollando78/SysML-reactflow) - Pure SysML v2.0 building blocks for React Flow — 60+ element types, 30+ edge types, viewpoint system, elkjs layout. TypeScript/React.
- [Tessera](https://github.com/jackhale98/Tessera) - CLI + Tauri desktop app — tolerance analysis, BOM management, SysML v2 import/export round-trip. Rust/Svelte. [Site](https://tessera-engineering.com).

## Python Tools

- [sysmlpy](https://github.com/mycr0ft/sysmlpy) - Pure-Python toolkit for SysML v2 — ANTLR4 parser generated from the OMG BNF (123/123 XPect conformance), semantic analyzer with 31 rule codes (name resolution, type/unit checking via Pint, dimension derivation, OCL well-formedness), stable content-derived element identities with rename reconciliation, 17 PlantUML views plus Java-free boxes rendering, model diff, CI gate, ReqIF import/export, and NetworkX/Kùzu/Cayley graph backends. `pip install sysmlpy`. MIT.
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
- [daltskin LSP Python client](https://github.com/daltskin/sysml-v2-lsp/tree/main/clients/python) - Zero-dep Python LSP client + Jupyter notebook — drives sysml-v2-lsp over stdio JSON-RPC.
- [sysml-obfuscate](https://github.com/mycr0ft/sysml-obfuscate) - Strips or abstracts confidential content from SysML v2 models so they can be shared, reviewed, or published.

## .NET Tools

- [SysML2.NET](https://github.com/STARIONGROUP/SysML2.NET) - C# SDK — core model, JSON/XMI/MessagePack serializers, REST/DAL clients, Docker image, live demo viewer. [Viewer](https://viewer.sysml2.net).

## Graphical Editors & Viewers

- [Eclipse SysON](https://github.com/eclipse-syson/syson) - Open-source web-based graphical modeler built on Sirius Web. Drives Papyrus SysMLv2 & Capella co-design. [Docs](https://doc.mbse-syson.org).
- [Open-MBEE sysmlv2-web-modeler](https://github.com/Open-MBEE/sysmlv2-web-modeler) - Standalone Java web service — graphical rendering + textual editing against any SysML v2 API backend. Dockerized.
- [sysmlv2-gui](https://github.com/DeciSym/sysmlv2-gui) - Native desktop + WebAssembly web graphical viewer — Rust/egui, reads `.sysml` files, renders OMG-specified graphical notation.
- [SysMD](https://github.com/tukcps/SysMD) - Notebook-style SysML v2/KerML modelling tool with an interactive, cell-based model editor. Kotlin. Apache-2.0.
- [sysml_canvas](https://github.com/mycr0ft/sysml_canvas) - Desktop diagram editor for SysML v2 built on gaphas and sysmlpy — an interactive canvas over the sysmlpy model, still early. Apache-2.0.
- [diagramboxes](https://github.com/mycr0ft/diagramboxes) - UML/SysML block diagrams as Unicode braille in a terminal or as SVG — layered layout (Brandes/Kozen/ELK) with no Java dependency; the renderer behind sysmlpy's boxes views. MPL-2.0.
- [Tom Sawyer SysML v2 Viewer](https://www.omg.org/sysml/sysmlv2/sysml-tool) - Model visualization — auto-layout, interactive navigation, integrates with any SysML v2 API repo.

## SysML v1 to v2 Migration

- [umlmeta](https://github.com/mycr0ft/umlmeta) - Clean-room UML 2.5.1 metamodel generated from the OMG XMI (242 metaclasses, 449 OCL constraints), with SysML v1, StandardProfile, and UAF 1.2/1.3 profiles. Reads XMI 2.1 and MagicDraw/Cameo `.mdzip` projects without vendor tooling, and emits SysML v2 anchored to the OMG v1→v2 transformation — refusing constructs that have no normative mapping rather than guessing. MPL-2.0.

## Product Data & Digital Thread

- [step242](https://github.com/mycr0ft/step242) - Pure-Python STEP (ISO 10303) reader — Part 21 parser, EXPRESS schema graph, AP242 parse/schema gate with CI exit codes, product structure as OSLC JSON-LD/Turtle, ISO/TS 10303-400 UUID bridge, and content-addressed configuration baselines. Validated against the 28-file NIST AP242 PMI corpus. MPL-2.0.
- [pyoslc](https://github.com/mycr0ft/pyoslc) - OSLC Core 3.0 server SDK in Python (BSD-3-Clause, extends CONTACT Software's SDK) with a SysML v2 domain, a STEP product domain, bidirectional SysML↔STEP "Vee" links keyed on qualified name + stable id, and configuration baselines that pin model and geometry together.

## Project Templates & Scaffolding

- [sysml-copier](https://github.com/mycr0ft/sysml-copier) - Copier template for SysML v2 projects — layout, CI, and tooling defaults.

## Validation & Analysis

- [Refinery Validation Pipeline](https://zenodo.org/records/19297800) - Pattern-based validation — connects to the SysML v2 API, transforms the model into a Refinery graph solver, and runs user-defined patterns. Docker Compose showcase. (Also listed under Python Tools for its client.)
- [SYSMOD MCP Server](https://github.com/Open-MBEE/sysmod-sysmlv2-api/blob/main/sysmod_mcp_server.py) - 17 MCP tools for querying SYSMOD artifacts — quality checks, atlas, feature trees, AI suggestions.
- [cameo-mcp-bridge](https://github.com/ajhcs/cameo-mcp-bridge) - MCP server bridging AI assistants to CATIA Magic/Cameo — 37 tools for query, create, modify, diagram operations on SysML/UML models.

## Syntax Highlighting & Grammar Files

- [daltskin/sysml-v2-grammar](https://github.com/daltskin/sysml-v2-grammar) - ANTLR4 grammar files for SysML v2 and KerML, generated from the OMG BNF.
- [tree-sitter-sysml](https://gitlab.com/nomograph/tree-sitter-sysml) - Tree-sitter grammar for SysML v2 — editor integration for any tree-sitter host.
- [vpathai TextMate grammar](https://github.com/vpathai-git/sysmlv2-language-server/tree/main/sysml_resources) - TextMate grammar bundled in the sysmlv2-language-server (`sysml_resources/`).
- [Pilot Xtext grammar](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation/tree/master/org.omg.sysml.xtext) - Reference grammar in the Pilot Implementation (Eclipse Xtext `.xtext` files).
- [pygments-sysml](https://github.com/mycr0ft/pygments-sysml) - SysML lexer for syntax highlighting with Pygments. Python.
- [sysml-vim](https://github.com/mycr0ft/sysml-vim) - Vim syntax highlighting for SysML v2 textual notation. Vim Script.

## Samples, Examples & Training

- [SysML v2 Release examples](https://github.com/Systems-Modeling/SysML-v2-Release/tree/master/sysml) - Official OMG example models (KerML and SysML v2) — the canonical starting point (`kerml/`, `sysml/`).
- [SysML v2 Standard Library](https://github.com/Systems-Modeling/SysML-v2-Release/tree/master/sysml.library) - Normative model libraries (Kernel, Domain, Systems libraries) (`sysml.library/`).
- [SysML v2 Intro Presentations](https://github.com/Systems-Modeling/SysML-v2-Release/tree/master/doc) - Official OMG intro PDFs for both textual and graphical notation (`doc/`).
- [SysML v2 Pilot examples](https://github.com/Systems-Modeling/SysML-v2-Pilot-Implementation/tree/master/sysml/src/examples) - Example and training models shipped with the Pilot Implementation (`sysml/src/examples`, `sysml/src/training`).
- [GfSE SysML v2 Models](https://github.com/GfSE/SysML-v2-Models) - GfSE-curated collection of high-quality SysML v2 models — validated in CI via the Pilot Implementation parser. Covers SE models, EveOnline mining frigate, family model, SOS, and more. BSD-3-Clause.
- [Airbus Apollo 11 SysML v2](https://github.com/airbus/apollo-11-sysml-v2) - Comprehensive SysML v2 model of the Apollo 11 mission by Airbus Central R&T. Uses the 5-layer CoSMA framework (Purpose/Operational/Functional/Logical/Technical) with full requirements traceability, analysis calculations, state machines, and mission execution modeling. Research artifact with accompanying INCOSE paper.
- [AMS GRA SysML v2 model](https://github.com/mycr0ft/ams-gra-sysml) - SysML v2 model of the AMS GRA v14.0 government reference architecture for Open Mission Systems — mission processing units, mission system, cyber-security roles, and a 72-requirement VCRM, built with the sysmlpy toolchain.
- [SYSMOD for SysML v2](https://github.com/MBSE4U/sysmod-sysmlv2) - SYSMOD language extension and worked examples for SysML v2, from the SYSMOD authors. Apache-2.0.
- [Don't Panic Batmobile](https://github.com/MBSE4U/dont-panic-batmobile) - Batmobile SysML v2 example from the book "Don't Panic - The Absolute Beginners Guide to SysML v2" by Tim Weilkiens and Christian Muggeo. Includes `.sysml` textual notation and Jupyter notebook. Apache-2.0.
- [Flashlight Starter Model](https://www.omgwiki.org/MBSE/doku.php?id=mbse:sysml_v2_transition:sysml_v2_starter_model) - OMG starter model by Sanford Friedenthal — simple flashlight in Jupyter + PlantUML. Updated for the SysML v2 2025-04 spec release. Model organization (Requirements, Actions, Parts, Requirements Allocation), requirements tree, action tree, parts tree, on/off states. ([.sysml](https://de-bok.org/asset/39898415908a48350628209d59522add76acdfd1) · [.ipynb](https://de-bok.org/asset/4b8e819b5446ad999551e7d68c625e7d75f83f9f) · [Overview](https://www.de-bok.org/asset/45a09d62209810afce38cfa49a5a95d01d2fc2e7)).
- [SysON Flashlight Tutorial](https://docs.obeosoft.com/syson/v2025.6.0/user-manual/hands-on/tutorials/flashlight.html) - Obeo's beginner-friendly step-by-step SysML v2 tutorial (Flashlight model).
- [SysML v2 Learning Club](https://clubs.oose.com/courses/sysmlv2/) - OOSE's 107-lesson microlearning course — bite-sized units with exercises and quizzes.
- [Advent of SysML v2](https://github.com/sensmetry/advent-of-sysml-v2) - Sensmetry's 24-lesson video course with YouTube playlist, blog posts, and example models. ([YouTube](https://www.youtube.com/playlist?list=PLuceG5piNwHG7KBdo02RDPAkJ-ErbzHe0)).
- [SysML Cheatsheet](https://sensmetry.com/sysml-cheatsheet/) - Sensmetry's quick-reference cheat sheet for SysML v2 syntax.
- [SysML Syntax Explorer](https://cst.syside.app/) - Interactive browser-based concrete syntax tree (CST) visualizer. ([Docs](https://docs.sensmetry.com/automator/tree-sitter-playground/)).
- [Visual Paradigm 8-View Guide](https://sysml.visual-paradigm.com/docs/sysml-v2-studio-kick-start-guide/cohesive-system-model-in-8-views/overview/) - 9-part tutorial series building a Smart Home Climate System end-to-end.
- [Visual Paradigm Tutorials](https://sysml.visual-paradigm.com/docs/tutorials/part-1-the-basics-your-first-model/creating-your-first-sysml-v2-project/) - Getting started, parts & ports, industry examples (EV Charging Station, Turbojet, Camera).
- [Visual Paradigm Examples](https://sysml.visual-paradigm.com/) - 500+ professional example files (satellite, automotive, camera, turbojet) with AI explanations.
- [sysml-v2-lsp examples](https://github.com/daltskin/sysml-v2-lsp/tree/main/examples) - 20+ example `.sysml` files including bike, smart-home, DFA coverage, multiplicity.
- [Armstrong Process Group Tutorial](https://aprocessgroup.com/sysml-v2-tutorial/) - Half-day SysML v2 overview — language architecture, structure, behavior, requirements.
- [Caltech CTME Training](https://ctme.caltech.edu/transitioning-models-to-sysml-v2-with-mbse.html) - 3-day professional transition training from SysML v1 to v2 with Cameo.
- [Webel IT Australia Workshop](https://webel.com.au/node/4399) - 5-day full SysML v2 workshop with Cameo/CATIA Magic, Balls & Boxes sample problem.

## Commercial Tools

- [CATIA SysML v2 (Magic/Cameo)](https://3ds.com/products/catia/catia-magic/sysmlv2) - Dassault Systèmes. 100% spec-conformant, bidirectional text↔diagram sync, Teamwork Cloud, REST API, Community Edition free.
- [Systems Modeler with SysMLv2](https://www.siemens.com/en-us/products/teamcenter/) - Siemens. Web-based collaborative, Teamcenter PLM integration, REST/OSLC/API.
- [Simcenter Studio](https://www.siemens.com/en-us/products/simcenter/) - Siemens. Architecture generation + evaluation, Python, ML-based trade studies.
- [Ansys SysML v2 (SAM)](https://www.ansys.com/products/connect/ansys-system-architecture-modeler) - Ansys / Synopsys. Cloud-native, real-time collab, config mgmt, time-dynamic execution.
- [Davinci](https://celedon.solutions/davinci/) - Celedon. SysML v2 + CAD generation + document authoring + code synthesis.
- [Syndeia](https://intercax.com/products/syndeia) - InterCAX. Digital thread platform — connect SysML v2 to requirements, SW, HW, V&V, manufacturing.
- [SysML v2 Studio](https://www.visual-paradigm.com/features/sysml-v2-studio/) - Visual Paradigm. Web-based, AI-powered code gen, 500+ examples, real-time diagram sync.
- [PTC Modeler](https://www.ptc.com/en/products/ptc-modeler) - PTC. UML/UAF/SysML 1&2, Codebeamer/Windchill integrations, variability mgmt.
- [SysGit](https://www.sysgit.io/) - Git-based infrastructure, textual + graphical editing, DevOps integration for SysML v2 models.
- [TEAMS Toolset](https://www.teamqsi.com/products/) - Qualtech Systems (QSI). Import SysML v2 for FMEA/FMECA/FTA, diagnostics/prognostics, digital twin.
- [Violet Labs Integration](https://www.violetlabs.com/) - Violet Labs. Digital thread between SysML v2 and CAD/PLM/ERP/hardware tools.
- [Mgnite](https://www.mgnite.com/) - JupyterLab + Python environment integrating SysML v2 with Excel, PowerPoint, MATLAB/Simulink, DOORS Next.
- [Syside Modeler](https://sensmetry.com/syside/) - Sensmetry. Premium SysML v2 modeling environment.
- [Syside Automator](https://docs.sensmetry.com/automator/) - Sensmetry. Python library for analysis, optimization, and workflow automation.

## Containerized / Docker Images

> **⚠️ Memory note:** Images based on the SysML v2 Pilot / API Services (`gorenje/sysmlv2-jupyter`, `josh-kaplan/sysml-v2-docker`, `jaydeanmartin/sysmlv2`, `mbsemashup/sysmlv2-api.pilotimpl`, `mycr0ft/sysmlv2-jupyter-container`, `Open-MBEE sysmlv2-web-modeler`, `Refinery Validation Showcase`) bundle a JVM and often a Spring Boot server alongside JupyterLab/Eclipse. Combined overhead routinely exceeds 8 GB — run them on hosts with ≥ 16 GB RAM (preferably more when also running PostgreSQL). Containerizing is a good way to keep host deps clean, but plan host memory accordingly.

- [mbsemashup/sysmlv2-api.pilotimpl](https://hub.docker.com/r/mbsemashup/sysmlv2-api.pilotimpl) - Containerized SysML v2 API Services pilot implementation.
- [gorenje/sysmlv2-jupyter](https://hub.docker.com/r/gorenje/sysmlv2-jupyter) - Jupyter + SysML v2 kernel + API server Docker setup (image only; source repo no longer published).
- [jaydeanmartin/sysmlv2](https://github.com/jaydeanmartin/sysmlv2) - Docker Compose for Jupyter + API server + PostgreSQL.
- [Open-MBEE sysmlv2-web-modeler](https://github.com/Open-MBEE/sysmlv2-web-modeler/blob/main/Dockerfile) - Dockerfile + Dockerfile.openmbee — Java service with Pilot JARs, Graphviz, Python bundled.
- [Refinery Validation Showcase](https://zenodo.org/records/19297800#files) - Docker Compose configuration — Web UI + Jupyter + API + PostgreSQL (in the record files).
- [SysML2.NET](https://hub.docker.com/r/stariongroup/sysml2.net.viewer) - Docker Hub image — reference web-application viewer. ([Viewer](https://viewer.sysml2.net)).
- [mycr0ft/sysmlv2-jupyter-container](https://github.com/mycr0ft/sysmlv2-jupyter-container) - Docker container for SysML v2 Jupyter + API + PostgreSQL.
- [mycr0ft/SysON_podman_compose](https://github.com/mycr0ft/SysON_podman_compose) - Podman Compose setup for Eclipse SysON.

## Other Resources

- [daltskin/SysML-v2-Resources](https://github.com/daltskin/SysML-v2-Resources) - Curated resources for learning and working with SysML v2 — docs, videos, courses, tools.

## Maintainer's Projects

This list is maintained by Jon Fox ([github.com/mycr0ft](https://github.com/mycr0ft)). Projects of his indexed above: **sysmlpy**, **sysmlpy-api-services**, **gosysml**, **umlmeta**, **step242**, **pyoslc**, **sysml-style**, **diagramboxes**, **sysml_canvas**, **sysmlcad**, **sysml-obfuscate**, **sysml-copier**, **pygments-sysml**, **sysml-vim**, **ams-gra-sysml**, **sysmlv2-jupyter-container**, and **SysON_podman_compose**.

---

## Contributing

Submit a PR or open an issue at [github.com/mycr0ft/awesome-sysml](https://github.com/mycr0ft/awesome-sysml). Entries should be SysML v2-specific, actively maintained, and publicly accessible; note the licence where it is known. See [contributing.md](contributing.md).
