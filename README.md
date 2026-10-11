# Repolex Knowledge Graph of pytest-dev/pytest-subtests

RDF knowledge graph data for [pytest-dev/pytest-subtests](https://github.com/pytest-dev/pytest-subtests), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-subtests
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1e5760131dd7cc0376b86f4499aef15d51e28ea6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1e5760131dd7cc0376b86f4499aef15d51e28ea6
│           └── chunk-001.nq.gz
├── blob
│   ├── 1566e3300d99f7f48c92dbb10fdd1b27856e25d0.nq.gz
│   ├── 2ddb0d127530d619cd2a83d58733648880928c30.nq.gz
│   ├── 2f48d8643533ab844b366de81f3b28c8cee10bde.nq.gz
│   ├── 5efbe503d5fb19de995581932dcb9faa1098c591.nq.gz
│   ├── 627ea1b43ba8695160b2b2787c7c31c4be4dd3db.nq.gz
│   ├── 694d7d58d440c236ea8ddcfece9eb605427f7be9.nq.gz
│   ├── 73966619001c79a901d4866a649908bbad529ad1.nq.gz
│   ├── 77c04d8d78bb63f876889312ebceb6cea9eae265.nq.gz
│   ├── 878cdb261c31e7033e8a0680f9573ebe7f5e21d9.nq.gz
│   ├── 8946903254e6544bc31a429359e31b9e819e1bfe.nq.gz
│   ├── 91ec1d67cfae4201ed92a1777ebb5924b2ef3cc2.nq.gz
│   ├── 956939fbb3ffd4042db6e3e03bcef0152b971e1c.nq.gz
│   ├── b023de03b59fb0e389a6b0e6b8639eded7167e17.nq.gz
│   ├── bc6a8496d1fe5cd3f3fc0408fe0cef2e286cc42c.nq.gz
│   ├── d0ffc9501dcc4748985c6773d3092866f6bf6af7.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ed3ef03883d47980acb830f2d877096987f57c61.nq.gz
│   └── ef05f22485a5159538569334edc8df77b49185a5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1e5760131dd7cc0376b86f4499aef15d51e28ea6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[pytest-dev/pytest-subtests](https://github.com/pytest-dev/pytest-subtests)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
