# Repolex Knowledge Graph of jaraco/jaraco.packaging

RDF knowledge graph data for [jaraco/jaraco.packaging](https://github.com/jaraco/jaraco.packaging), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.packaging
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d38bddb85c6894f0e4f78b33e13e50afa4f5b6ed
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d38bddb85c6894f0e4f78b33e13e50afa4f5b6ed
│           └── chunk-001.nq.gz
├── blob
│   ├── 171e30a5530ce62b94a4aa5a2713ff17d20139f5.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 2a103ecea544d5d07f8271ea7e18afda0431adef.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 2e65a8f237433c0b0e630153a277174262a46943.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 353408347b41336c37d9db4b19ed42a7cdfa101b.nq.gz
│   ├── 4c9b67f6c151abd10faff59d33e5d92483e8dcd5.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 62129192cb3188828ba45537bdcf4c5be32bd712.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 70259983fd07aaec97e76be68d26f671d44c5aff.nq.gz
│   ├── 71e8e21819706548e76037a619ebfb48e595203c.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── a2f73238068025c179acc906b1d2fe7cdee92228.nq.gz
│   ├── ce1d418995c229f23b3a7f32f14f367edc2dd0a8.nq.gz
│   ├── d012c9a9e57f71a84bb6e75ddd6a36ff763d8dd1.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f32caecc40db646f00198d787119e34718536bef.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d38bddb85c6894f0e4f78b33e13e50afa4f5b6ed.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[jaraco/jaraco.packaging](https://github.com/jaraco/jaraco.packaging)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
