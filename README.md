# Repolex Knowledge Graph of timmywil/grunt-npmcopy

RDF knowledge graph data for [timmywil/grunt-npmcopy](https://github.com/timmywil/grunt-npmcopy), parsed by [repolex](https://repolex.ai).

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
rlex download timmywil/grunt-npmcopy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4ce5588f86f48c7fd16db770a6e68d475babdb0a
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 4ce5588f86f48c7fd16db770a6e68d475babdb0a.nq.gz
│   └── repolex
│       └── 4ce5588f86f48c7fd16db770a6e68d475babdb0a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ae1c1d41c80630d33592c99f8f9e9fdb848e3c6.nq.gz
│   ├── 1c1e9c804aa88cebb45716dfd815683fb8ebbea9.nq.gz
│   ├── 269d3fef7b46409b82e16d029f25ecac7ad5d907.nq.gz
│   ├── 4254a681f967230e41384421d22d4fdc16fae22c.nq.gz
│   ├── 4741f16ed77a4a348cd0e01f95a19620528d8e83.nq.gz
│   ├── 7d66797fc4ec7761557dfa8a4180af9f6905e30b.nq.gz
│   ├── 86e27a6b57e1878dd3fb5db65b86a471e6273342.nq.gz
│   ├── 910ae433c615024c35f84a6b2bc7aa168340876b.nq.gz
│   ├── b1f2cdfa7e0091e96999c410073c120b58249357.nq.gz
│   ├── bd3c7e04dd03b2676b5551b34be1c2a5ca581570.nq.gz
│   ├── d7a00409f3f59b8329a5e8034136e2ca3292a6ef.nq.gz
│   ├── eddce05bfd4f13a3c3829925723b293f47dc4acf.nq.gz
│   └── f9852e933dbe52d839888e2948374ad3272a9b3d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 4ce5588f86f48c7fd16db770a6e68d475babdb0a.nq.gz
├── filetree
│   └── 4ce5588f86f48c7fd16db770a6e68d475babdb0a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 23 files
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

[timmywil/grunt-npmcopy](https://github.com/timmywil/grunt-npmcopy)

---
*Parsed on 2026-11-21 by [repolex](https://repolex.ai)*
