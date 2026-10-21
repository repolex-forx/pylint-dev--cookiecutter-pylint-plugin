# Repolex Knowledge Graph of pylint-dev/cookiecutter-pylint-plugin

RDF knowledge graph data for [pylint-dev/cookiecutter-pylint-plugin](https://github.com/pylint-dev/cookiecutter-pylint-plugin), parsed by [repolex](https://repolex.ai).

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
rlex download pylint-dev/cookiecutter-pylint-plugin
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 803422363dc1cf00665f75bfe2782abcb41833cf
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 803422363dc1cf00665f75bfe2782abcb41833cf
│           └── chunk-001.nq.gz
├── blob
│   ├── 372f0b330a07332a4669a5d4982abb51bbe5eae2.nq.gz
│   ├── 39fd931892552eeb59b42ac18621d980d7a83c4f.nq.gz
│   ├── 43f562bd86d8f2ff0187d3cec28442e760a7c026.nq.gz
│   ├── 5632b1300769da89986fa229cf604d278b9e50d7.nq.gz
│   ├── 5773c29c22fa76ef10b944588605897e8b85dc5f.nq.gz
│   ├── 57ff26f1d1dbde637f682095b4cf1f046b02d6d2.nq.gz
│   ├── 64e1c49de837bc326e877cbceec2105e7b76b148.nq.gz
│   ├── 68a2f481f75cac16812c9fa040a97c7364737e86.nq.gz
│   ├── 75f5e11980803d9b2c89e8aad063d4d4069e9aa8.nq.gz
│   ├── 8aecf069185121b34d508536fa45578fdeaf9996.nq.gz
│   ├── 95bfd8f5d689ebfb61e9279bfe7cc2a6497be881.nq.gz
│   ├── 9d6ca021f3f13a4394e60ca667d6d0ed3a758efe.nq.gz
│   ├── 9f73efdaea628387f192e507780bfcde5553deac.nq.gz
│   ├── ab7467e8a44b6d5143f7ab3e586ba674303c2660.nq.gz
│   ├── c41a790e1189c13b84c24ee1753a557e20127b95.nq.gz
│   ├── c59cd6f06bf5cad6d635e7a97337b6c308cc985a.nq.gz
│   ├── c7f8f75ad96c44050c2862bc4029ce2b19d25f8b.nq.gz
│   ├── c8e505e14e4c1ac3ec3203bb99703dace3638f01.nq.gz
│   ├── db1741e4e746dde2e909bfe4aa60aa013a5fdc95.nq.gz
│   ├── f0113583457bfa51a1a87fca22ef943e8d3b35b9.nq.gz
│   ├── f39785f8964c59f6a52f560d18dfae69af61a923.nq.gz
│   └── f5cc5eca2aaf88eb74127a8aef7f2019f64cfac0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 803422363dc1cf00665f75bfe2782abcb41833cf.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 29 files
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

[pylint-dev/cookiecutter-pylint-plugin](https://github.com/pylint-dev/cookiecutter-pylint-plugin)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
