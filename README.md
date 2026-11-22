# Repolex Knowledge Graph of ruuda/thread-id

RDF knowledge graph data for [ruuda/thread-id](https://github.com/ruuda/thread-id), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download ruuda/thread-id
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d748920c9547d5fa35143813aa9f40f13446ca83
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── d748920c9547d5fa35143813aa9f40f13446ca83.nq.gz
│   └── repolex
│       └── d748920c9547d5fa35143813aa9f40f13446ca83
│           └── chunk-001.nq.gz
├── blob
│   ├── 21b6333b92208b0c333787528a17eadda83b1cf0.nq.gz
│   ├── 2d6e4805152eba3833325555f12c4fdfd32b96b0.nq.gz
│   ├── 61413eeec22eb2165f72a248fb25da89f7141a0a.nq.gz
│   ├── 880b5358a248ea5856cc80051da877eb8d2446dd.nq.gz
│   ├── 91d3aa967f42ec7e3c600d27344d8e730c8a5740.nq.gz
│   ├── 9a5cf3016deaf5b50e463c679449fec38afb3232.nq.gz
│   ├── b1547d964015362d2ecd870305421335b4883781.nq.gz
│   ├── be6492af5b9d106e6358f12fdfcec4f5224d3d26.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e9908ac20cff62272c4fa030842621e6eba67d8c.nq.gz
│   ├── f49be8d92102e9f105909826db3f424123e7986d.nq.gz
│   └── f814c20dd591d805d8f2c20fca2db32963395cfa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── d748920c9547d5fa35143813aa9f40f13446ca83.nq.gz
├── filetree
│   └── d748920c9547d5fa35143813aa9f40f13446ca83.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 22 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[ruuda/thread-id](https://github.com/ruuda/thread-id)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
