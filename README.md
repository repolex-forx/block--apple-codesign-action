# Repolex Knowledge Graph of block/apple-codesign-action

RDF knowledge graph data for [block/apple-codesign-action](https://github.com/block/apple-codesign-action), parsed by [repolex](https://repolex.ai).

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
rlex download block/apple-codesign-action
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 679535d1ab7c5a7c18e6f9afcba3464512cc3dde
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 679535d1ab7c5a7c18e6f9afcba3464512cc3dde.nq.gz
│   └── repolex
│       └── 679535d1ab7c5a7c18e6f9afcba3464512cc3dde
│           └── chunk-001.nq.gz
├── blob
│   ├── 0222afec06ed4d3cb46211affdb1f2ccf2f31ecd.nq.gz
│   ├── 2c299ab1afeabd9badef71da8fc05ce9c322d2ab.nq.gz
│   ├── 6bccf43368fd7c96d9c659562a5142b8b8cb98a1.nq.gz
│   ├── 6d46ac4b3f8aa525e74e65ab9097fedeeb3a1035.nq.gz
│   ├── 862ee3c28647e7a58801a75236855c269c1448ae.nq.gz
│   ├── 918189b59bfb7477813979e4fd07994c401db64b.nq.gz
│   ├── 91c192550c57de20dfd1dbd5ce4963b649f48ff4.nq.gz
│   ├── 9582fc588754f78d9875691a3bd5e674295436b3.nq.gz
│   ├── daa37e807b5c58d06e749479b0aa3973f405a298.nq.gz
│   ├── dd9e767b88b7cbf106420fcf3369c7fdcbf534f1.nq.gz
│   ├── e15e11c514d62cd8206c10c757f10eac2d8d4fe6.nq.gz
│   └── f2a0eb61e1c891230acdc19a5257bc591f9169e7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 679535d1ab7c5a7c18e6f9afcba3464512cc3dde.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[block/apple-codesign-action](https://github.com/block/apple-codesign-action)

---
*Parsed on 2026-10-02 by [repolex](https://repolex.ai)*
