# Repolex Knowledge Graph of asimov-modules/asimov-x-module

RDF knowledge graph data for [asimov-modules/asimov-x-module](https://github.com/asimov-modules/asimov-x-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-x-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 23df0b9487b354fdb7866e476cf43f71e1db480a
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 23df0b9487b354fdb7866e476cf43f71e1db480a.nq.gz
│   └── repolex
│       └── 23df0b9487b354fdb7866e476cf43f71e1db480a
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 13037365d0bb7397f5c4c5267b7b0f55fd3fc39f.nq.gz
│   ├── 3aa324005a5530c996e0f35566ddbe9056353f56.nq.gz
│   ├── 47e74185a35bae09080d1ab8292a3fbab0e4644d.nq.gz
│   ├── 521ce4a8415a9d8984f10a3fdc673d99ba393e35.nq.gz
│   ├── 62a84431ab56848848618dd6430a0b6078fcf7da.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 7048d58cd3f7dbacae775aa369a83bde574d7919.nq.gz
│   ├── 7179039691ce07a214e7a815893fee97a97b1422.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 7f9620c70113a931d368e1706c32f0053fc24a16.nq.gz
│   ├── 8af737c1b20db0a66b10cc86fef571ceff9503f7.nq.gz
│   ├── 8d5e8364ba51b4878ed04a3f75f9680f8587c6f9.nq.gz
│   ├── 912a2861c506bcf060fedd9748ac9266ec9b749f.nq.gz
│   ├── 9219b8ee51230fa859824dd9a514cc0a6590de9f.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── a3cfa7a48b2d0af452eb50fc83ffc7221d687092.nq.gz
│   ├── ab4288bd1c937d4d0cd11d2236ebb2d5100d6e52.nq.gz
│   ├── ac529958e8aa50dd0fa51b67fb8bc426e46001c9.nq.gz
│   ├── ae7825fe1b43956c506b57973a1d82f8f4b803e2.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── b6f001705c193d25c79c2bc90b0c5d88ab6fc61e.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── ded69748c9670ef7883a8f3caf63953c86340407.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 23df0b9487b354fdb7866e476cf43f71e1db480a.nq.gz
├── filetree
│   └── 23df0b9487b354fdb7866e476cf43f71e1db480a.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 37 files
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

[asimov-modules/asimov-x-module](https://github.com/asimov-modules/asimov-x-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
