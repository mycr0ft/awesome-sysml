# Candidates and removed entries

Working scratchpad for items that are not ready for `README.md`, and a record of
entries that were removed and why. Nothing here is published as part of the list.

## Moved / deprecated

| Item | Was | Why it left the README |
|---|---|---|
| `gorenje/sysmlv2-jupyter` source repo | linked from the container entry | GitHub repository returns 404; the Docker Hub image still exists, so the entry now links the image only. |
| DeciSym `sysmlv2-gui` Dockerfile | container entry | The repository has no Dockerfile (Rust/Trunk project); the project remains listed under Graphical Editors & Viewers. |
| `zbigniewsobiecki/sysml2` examples | samples entry | The repository has no `examples/` directory; the CLI itself remains listed. |
| Refinery duplicate | Python Tools + Validation | The same Zenodo record was linked twice; `remark-lint:double-link` rejects that. Kept in Validation & Analysis, and the container entry links the `#files` view. |
| `kenji-miyake/sysml-v2-docker` | container entry | Repository archived (last push 2022-08); Eclipse + Pilot container is superseded. |
| `josh-kaplan/sysml-v2-docker` | container entry | No push since 2024-01; the compose stack predates the current Pilot and API Services. |
| `sensmetry/sysml-2ls` (SysIDE Editor Legacy) | language servers | Repository archived (2025-10) when Sensmetry moved to the closed SysIDE Modeler; the commercial entries remain listed. The `sysand` package manager it mentioned is now listed separately. |
| `smp4/sysmlv2-python-cookiecutter` | templates | Repository archived (2024-10); `sysml-copier` supersedes it. |
| `redsteve/SysML-v2-API-MCP-Server` | validation & analysis | No push since 2025-09 and no releases; kept out of the list until it shows maintenance. |

## Candidates to review

| Item | Note |
|---|---|
| [modelscript/modelscript](https://github.com/modelscript/modelscript) | Web-native incremental modelling; AGPL-3.0 — check licence policy before adding. |
| [redsteve/SysML-v2-API-MCP-Server](https://github.com/redsteve/SysML-v2-API-MCP-Server) | Added 2026-10 to Validation & Analysis; re-check activity in six months. |
| [FlyingCpp/sysmlv2-learning-all-in-one](https://github.com/FlyingCpp/sysmlv2-learning-all-in-one) | Chinese-language learning platform (courses, online modelling, validation). Decide whether non-English resources belong in Samples. |
| `nomograph-sysml`, `kebnf` (crates.io) | Small/new crates; revisit when they have documentation. |
| `MJP-Sys/sysml-v2-modeling-skill` | Agent skill rather than a SysML tool; out of scope unless a skills section is added. |
