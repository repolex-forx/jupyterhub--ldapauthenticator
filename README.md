# Repolex Knowledge Graph of jupyterhub/ldapauthenticator

RDF knowledge graph data for [jupyterhub/ldapauthenticator](https://github.com/jupyterhub/ldapauthenticator), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/ldapauthenticator
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9d2759a3ca3ab8a311398fbae8f8d4cd114f66b0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9d2759a3ca3ab8a311398fbae8f8d4cd114f66b0
│           └── chunk-001.nq.gz
├── blob
│   ├── 08e2c862d18b0e57e16015943ebe4f4d698168f3.nq.gz
│   ├── 0dc89813dc10ed07777226c26d348a19ce3afb93.nq.gz
│   ├── 154686b80c9c99003a93a039578ed973a6b54476.nq.gz
│   ├── 1aba38f67a2211cf5b09466d7b411206cb7223bf.nq.gz
│   ├── 353731e87a1df8e1599a2db42e583bafdc88c1ca.nq.gz
│   ├── 3850476de6d58d478c9c2edd2354659ef34cf46e.nq.gz
│   ├── 40e4f75e0b11184f6b966270175ce5b00abe40ad.nq.gz
│   ├── 522bb086268ccb32f7b10952749a6f354eb04e9b.nq.gz
│   ├── 676ce8cbb65141a024d4b5b2ef8f9eb92096971c.nq.gz
│   ├── 75077cfc9aaada17f683484adccfb38a5f078b69.nq.gz
│   ├── 758e1a69a4053e1bf7d7f5d2b4d5c37ee10c8376.nq.gz
│   ├── 78dc6281dad7c6993896889f5b766fbd56b4f9c2.nq.gz
│   ├── 8b55fca2bf387823995b2078f01e6d0d2a579c3b.nq.gz
│   ├── 976f96985b038f1685174c805a290ccdc16a1ba3.nq.gz
│   ├── 9b92a33935518015e3c5c8baf21169524083d723.nq.gz
│   ├── c19a5198725404fce4241d64064d0a3c8e860567.nq.gz
│   ├── cf788f110aedf5a1f30e6f9d5e249107c789ae90.nq.gz
│   ├── e1eb364d9e2072bc91242f612a87b377b4c60fcb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fbc9eb5620fbbb6121f7fbc06b7fd9ff7653bf6d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9d2759a3ca3ab8a311398fbae8f8d4cd114f66b0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[jupyterhub/ldapauthenticator](https://github.com/jupyterhub/ldapauthenticator)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
