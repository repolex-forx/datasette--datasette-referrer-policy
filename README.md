# Repolex Knowledge Graph of datasette/datasette-referrer-policy

RDF knowledge graph data for [datasette/datasette-referrer-policy](https://github.com/datasette/datasette-referrer-policy), parsed by [repolex](https://repolex.ai).

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
rlex download datasette/datasette-referrer-policy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d70d80010b558a545c0c05e93f0bcf137a64e750
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d70d80010b558a545c0c05e93f0bcf137a64e750
│           └── chunk-001.nq.gz
├── blob
│   ├── 031f1eb0e1257b90dcc7ba09ef15c59b5aee05ba.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 3eb871944ba060e652582342cecb018b41f78bda.nq.gz
│   ├── b1768e63265df6ab11e1d79eac37ea55d7cd45d8.nq.gz
│   ├── b1fbe49fcfda348c3e8a756f25ffec08626baaf2.nq.gz
│   ├── d49d309499efb2c0c1d38efdd53056249a7d74d8.nq.gz
│   ├── d9bd62e1ff72656aa1e5bd7540dfc00aecddc883.nq.gz
│   └── eb22e74eaaaf0edc4aa2c0f8900a55750d1660f9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d70d80010b558a545c0c05e93f0bcf137a64e750.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 14 files
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

[datasette/datasette-referrer-policy](https://github.com/datasette/datasette-referrer-policy)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
