# Repolex Knowledge Graph of matplotlib/cycler

RDF knowledge graph data for [matplotlib/cycler](https://github.com/matplotlib/cycler), parsed by [repolex](https://repolex.ai).

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
rlex download matplotlib/cycler
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d1737eb0a42bd451e8770cef245ebe60ebb36bfc
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d1737eb0a42bd451e8770cef245ebe60ebb36bfc
│           └── chunk-001.nq.gz
├── blob
│   ├── 024c8d95ac9241e8affc8ff226e2bbfab1297463.nq.gz
│   ├── 0a5552a7721c765421ea12f35c519baf8e2a2bdb.nq.gz
│   ├── 126de4b2e3800d8ca9bb9bf145d9d5c9b6c6ef45.nq.gz
│   ├── 18712c973b1474022aff87c57d3beee9dcfb474c.nq.gz
│   ├── 1eccac3a6bb8fa516ffcfa42c71da6e731824e8e.nq.gz
│   ├── 20908de9bf2d533a508f726fb387379ab76e1d3e.nq.gz
│   ├── 384bc8e4ff8a4380c80d76be5f56e2ff2e1f86c4.nq.gz
│   ├── 407d80210a7dfe679ee33dc783aeb1de4737ac9b.nq.gz
│   ├── 57ca08c675744dd94038f4271fd58929c31c14af.nq.gz
│   ├── 6a5c91084a255642339d35396064a8335ca7f3b9.nq.gz
│   ├── 807c007edc628a4ef98101b72165cb449b2e173b.nq.gz
│   ├── 851259b60f9520d6736563d8e235fbb1efc04dc2.nq.gz
│   ├── 906a7822e8f9b86796c57f2df7f4f23548ed2ed4.nq.gz
│   ├── 98ceb87e9ed106c9510441c86bd5cf82d56c3b03.nq.gz
│   ├── b134e782506b34ae3cb141c0e01c93b4a0e943da.nq.gz
│   ├── c7c79cb1e6299a014f4d085b6183f560685e92bb.nq.gz
│   ├── ce955776815ada07d789584b2735dcbc3bd6dca9.nq.gz
│   ├── d41d808995af2d59db2496a3ae772ca3d849cab2.nq.gz
│   ├── db476b81085d4c9af3267919eb24c240432a8cbf.nq.gz
│   ├── dbcb44a367be1ce386d777669893bfea2f974cb5.nq.gz
│   ├── dc1b4c81c529fdfa42012a26b2b12f5b8a1538c4.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d1737eb0a42bd451e8770cef245ebe60ebb36bfc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[matplotlib/cycler](https://github.com/matplotlib/cycler)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
