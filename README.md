# Repolex Knowledge Graph of agronholm/exceptiongroup

RDF knowledge graph data for [agronholm/exceptiongroup](https://github.com/agronholm/exceptiongroup), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download agronholm/exceptiongroup
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ddddb6fdf8582c4ae5187dc1bd258115974229fe
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── ddddb6fdf8582c4ae5187dc1bd258115974229fe.nq.gz
│   └── repolex
│       └── ddddb6fdf8582c4ae5187dc1bd258115974229fe
│           └── chunk-001.nq.gz
├── blob
│   ├── 0246568bd05013ed797e0514181aa43bdc59c63e.nq.gz
│   ├── 11467eeda9b317cbf5d378beea30e31a51d35d1c.nq.gz
│   ├── 1da749e23c6ed9b75f6f1e2c2fb27ac1f3048207.nq.gz
│   ├── 1e4a8f30deeac30ae534247ce59dfa6a4ee6c5fa.nq.gz
│   ├── 289bb33c0e67fb99b149a306c9e32db8455cbb52.nq.gz
│   ├── 2f12ac32a28361a36d7e8c1312e3b0fccb6ce494.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 45a2f73673edab66a13ab5de206142341e996f10.nq.gz
│   ├── 490e2e0cafcd5ed4f6c53da5dbd5b517e10a7baa.nq.gz
│   ├── 50d4fa5e68439ce837f6eef437b299c0dd7c8594.nq.gz
│   ├── 5e512137aac725981f643b0c8dcac198f48a84a9.nq.gz
│   ├── 6263930ca5698c9eb8e983c5f9075ac9c0c37e67.nq.gz
│   ├── 82b7e56adbb68d64dc7893fdc973ed09c71f4883.nq.gz
│   ├── 84e558ab4ded32bb2a2e6b6560dd1db761790090.nq.gz
│   ├── 8712927206c43527ba7f39835dc8d9abfcc4072b.nq.gz
│   ├── aeca72d3b5e6f178a10d7913fb593b45b92fd342.nq.gz
│   ├── c5c30bc6b668565fc8d799fcde739d499677515a.nq.gz
│   ├── d34937d576e47d9eb6a446b45a6e98bc2c239c38.nq.gz
│   ├── d50afee14b797cfebc7bd33527dd3fd9d210ec7c.nq.gz
│   ├── d59f2f7e64450d0518f576d5e51ff5a1f0fa529c.nq.gz
│   ├── d8e36b2e65d11e7f3b2c540c1b292a39a6cc219d.nq.gz
│   ├── e2bc81a2069a4bdfd29aae1a705bb1552712cb10.nq.gz
│   ├── e67e636323eb5bafd67139a656bb3ed9bb4ae0a2.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7f43c5970a9e3ae1d5f1f5dbe28e9cfe5085f81.nq.gz
│   ├── f42c1ad3628d927776f82dbd180cd499f26cd34d.nq.gz
│   └── ff0c71e4d45d52217e32f8ac145c83cc623c58e1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── ddddb6fdf8582c4ae5187dc1bd258115974229fe.nq.gz
├── filetree
│   └── ddddb6fdf8582c4ae5187dc1bd258115974229fe.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 37 files
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

## Source repository

[agronholm/exceptiongroup](https://github.com/agronholm/exceptiongroup)

---
*Parsed on 2026-04-14 by [repolex](https://repolex.ai)*
