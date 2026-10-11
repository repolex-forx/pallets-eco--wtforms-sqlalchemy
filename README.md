# Repolex Knowledge Graph of pallets-eco/wtforms-sqlalchemy

RDF knowledge graph data for [pallets-eco/wtforms-sqlalchemy](https://github.com/pallets-eco/wtforms-sqlalchemy), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/wtforms-sqlalchemy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 29dee4d59b906c3493402e30019be54895dd35a6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 29dee4d59b906c3493402e30019be54895dd35a6
│           └── chunk-001.nq.gz
├── blob
│   ├── 04578617d1a912bc3d1d2377a05f859fcc298736.nq.gz
│   ├── 0936122bb34dd88198cb6402b40a674779ceba33.nq.gz
│   ├── 15fbe39f6583a99ad37f67ce9d5bb01b6ce1d710.nq.gz
│   ├── 1cddf087e93e5cc093920ea73bd2e12edccc3775.nq.gz
│   ├── 23c76ad8de63bc947cb7221d33e719c811d5b2b4.nq.gz
│   ├── 26dc15f20440bb142bf3ed774622c8f1d0aa87a0.nq.gz
│   ├── 2941c22a2311ed5f581a2e600d94241c9a6f95da.nq.gz
│   ├── 33c2f1422b88b43f2b24f59cd1bdb624fe4a1d7f.nq.gz
│   ├── 4c054e00d4bbd05ad07c9484c995137dca9eea2a.nq.gz
│   ├── 4e45e5d76d3aa5d36f169c5686eac7bfe461d01a.nq.gz
│   ├── 5574681de4d21f05d41308c288af6b8b3ca03090.nq.gz
│   ├── 574945cfad2084da925592dcc775627dca1b4c4b.nq.gz
│   ├── 7e001d441418515ae87bdff65dd9c1680595a5c1.nq.gz
│   ├── 7f1101abefdf042be07967427e8ecbdb33811572.nq.gz
│   ├── 88db946c363562bcd26af03fc74293f3b40c97c7.nq.gz
│   ├── 93d2150ef758a0b77a0e61897bdc85985118c0b8.nq.gz
│   ├── 94cf5c38cf8067426696d9db7a11b92df5cc9793.nq.gz
│   ├── 955deaf27bc821a6367e818f36c016892fed3d33.nq.gz
│   ├── a82b8271406f35b291b691c116d8270af6fa1034.nq.gz
│   ├── b23099c5b77ec6bbe7aa42b217ee2257bdc62ea9.nq.gz
│   ├── c012689f40ff048cae88f6ce61ea69b86b62c6e3.nq.gz
│   ├── c275ed9e09dfd438b54bf04ca32331d748364c82.nq.gz
│   ├── c62bb0e18a154fc11cb16ea40cd5704442961f2a.nq.gz
│   ├── df12433297bd70ed2ff5e17e7712120fe499d750.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 29dee4d59b906c3493402e30019be54895dd35a6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[pallets-eco/wtforms-sqlalchemy](https://github.com/pallets-eco/wtforms-sqlalchemy)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
