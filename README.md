# Repolex Knowledge Graph of seanmonstar/httparse

RDF knowledge graph data for [seanmonstar/httparse](https://github.com/seanmonstar/httparse), parsed by [repolex](https://repolex.ai).

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
rlex download seanmonstar/httparse
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9f29e79f9832dbd0ae5220acb17c1866745bdecd
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9f29e79f9832dbd0ae5220acb17c1866745bdecd.nq.gz
│   └── repolex
│       └── 9f29e79f9832dbd0ae5220acb17c1866745bdecd
│           └── chunk-001.nq.gz
├── blob
│   ├── 06bc4df5cc01add94494a6ed5e77ac45b3c4cc6e.nq.gz
│   ├── 0e4493a5c635e17addf26f6e4d5a855cdd062316.nq.gz
│   ├── 0ea7bac075cb08b58b612e86e7d24adde7a5436b.nq.gz
│   ├── 0fabdfeb21efde791e20bb6848d7c718d400e0d4.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 2adf0a28d94f014858f24e62bdc3e036ef4dd937.nq.gz
│   ├── 2e0309daef01d4062972ba0fcf4b7c68c95f0432.nq.gz
│   ├── 37654b9d4df336a5f08be3d3922a1e8bab999ef4.nq.gz
│   ├── 4587f8d68ff64232a5739cb47e62c4d16994b428.nq.gz
│   ├── 4aee710c4c669aa8838af48e957e527322f9d98f.nq.gz
│   ├── 572e03bdf321b6cc3a99488183436905cefd086d.nq.gz
│   ├── 5e854c5fbb45ba8ad407446c71b755b1077270d9.nq.gz
│   ├── 751f60b3f71a3d2e1586e69fc0fabe5a03fe3d25.nq.gz
│   ├── 757723f776fed278604a3b10f9935a9e08f33a5c.nq.gz
│   ├── 7794d31de8c80189968232e50985652b561e7790.nq.gz
│   ├── 7846a3e0976dac7ed3d3aa3899a60af0f460d6cb.nq.gz
│   ├── 83133af66ead8560c89aa9aa9e3f13258f908bf8.nq.gz
│   ├── 98c1d7bc206f382bb47b140be6ba0b41c08bec90.nq.gz
│   ├── a6b3376daef6e0ce45479f26768d6bb60126d15c.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── b059efb2219cc2b41d56d6a72d8b344d3678ae15.nq.gz
│   ├── b543c61bfb7062d0a14fd283e5d4f058df8c732a.nq.gz
│   ├── bffcedb6cc02c5b3b69d65792125532b561c0c7a.nq.gz
│   ├── c523a921dbc80f9ebc91f510faf6fda22e6e2e15.nq.gz
│   ├── ce79aa608877a6f224f79f956e02b0ae0e8276d2.nq.gz
│   ├── ceba2f457abaaa301f9fa135017152af51bac5dd.nq.gz
│   ├── dfa8395f775dfffcfc7a93e58169e5a5c74c75fc.nq.gz
│   ├── e0ceab47786af7cc8cac1647858bc8d2e4564071.nq.gz
│   ├── e1028d0531862a5724ec6ad6a7d923615245b96f.nq.gz
│   └── f221e5297c7659379ed408fec46865e8429d7366.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9f29e79f9832dbd0ae5220acb17c1866745bdecd.nq.gz
├── filetree
│   └── 9f29e79f9832dbd0ae5220acb17c1866745bdecd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 40 files
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

[seanmonstar/httparse](https://github.com/seanmonstar/httparse)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
