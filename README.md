# Repolex Knowledge Graph of google/python-subprocess32

RDF knowledge graph data for [google/python-subprocess32](https://github.com/google/python-subprocess32), parsed by [repolex](https://repolex.ai).

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
rlex download google/python-subprocess32
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b63954f56166eca312afb70b6d3a4af1128f81f3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b63954f56166eca312afb70b6d3a4af1128f81f3
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d336624f4dbc167a7e89acf5cab7b0daaf451a0.nq.gz
│   ├── 17a1696e98fcb1633e623f3a690be2697fe0fc9c.nq.gz
│   ├── 1dc3191ad183f751b4631462fbf3cb97b8c7de52.nq.gz
│   ├── 429a9a57b32ca165ba454c4d3e75d455eac9a24e.nq.gz
│   ├── 57a5b27e674cd5d23044d01afbb5ec382c0bd879.nq.gz
│   ├── 630ede1461ecdd2e29de173c2e1a7a86666d4f63.nq.gz
│   ├── 66a7a60ef928f7e20041b471eefe2e6886c61d3f.nq.gz
│   ├── 67fb41c0af894c8437a05ed394eaf2b2c9238afc.nq.gz
│   ├── 69906379a9b3876285dff230a528cad150d343ca.nq.gz
│   ├── 6bdc9bef88f163208e082e323fbe4d3ab3751bd2.nq.gz
│   ├── 6d7e32ed909a8eaf1bd36bdac0c21ce38b19356f.nq.gz
│   ├── 73f6b6c05acc670a6551785c6c2fc6c4f2ab08e8.nq.gz
│   ├── 751239d237a5ff0251b118af25713e6cf12b66b1.nq.gz
│   ├── 7db7d8465e2186f9498e4d9ac01341d2926efb3d.nq.gz
│   ├── 80dfc335170b9c042c94962aea1679cae41ee444.nq.gz
│   ├── 8927b5b8d349b2b526d212a1d685b2604d6bdfc9.nq.gz
│   ├── 8ab9b14fd0f81b1dc80b4e95ebb845c603fd4c8e.nq.gz
│   ├── a7971ae7dc4d96f23a54339df0b5af272e643b5e.nq.gz
│   ├── a8960352f75ddcd6bf720eae6ac799d02e90049e.nq.gz
│   ├── b19f9cd1bd0bfaaf2e55b0d8343416c0cc05c7df.nq.gz
│   ├── ba5ccf2cf01ce852a704d662e2ed5e0db587471b.nq.gz
│   ├── c6d7cb500eda390fdd68c20ad9fe74a8d15613ac.nq.gz
│   ├── cc855d40bd885141b49006d820a9bd7544f136a1.nq.gz
│   └── fe6f9db25c97014c59948f1643c09f4afaaa2513.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b63954f56166eca312afb70b6d3a4af1128f81f3.nq.gz
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

[google/python-subprocess32](https://github.com/google/python-subprocess32)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
