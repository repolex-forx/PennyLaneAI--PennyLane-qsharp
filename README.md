# Repolex Knowledge Graph of PennyLaneAI/PennyLane-qsharp

RDF knowledge graph data for [PennyLaneAI/PennyLane-qsharp](https://github.com/PennyLaneAI/PennyLane-qsharp), parsed by [repolex](https://repolex.ai).

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
rlex download PennyLaneAI/PennyLane-qsharp
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cdbf79a94611bcf96bc3cd31858e3714e9836cca
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cdbf79a94611bcf96bc3cd31858e3714e9836cca
│           └── chunk-001.nq.gz
├── blob
│   ├── 04c287f93d014f9e1e7f17d752b19828c1eb92b8.nq.gz
│   ├── 10bd335a4522daf891e05f12f05910ad58a69d91.nq.gz
│   ├── 122bfe917aadcb389b6e47553cc4048951ecb809.nq.gz
│   ├── 1f45a51f640f0d0dc04c0311021c6c62d6f85ae7.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2ad508a2b3acb619d064608d6fee05eb9ff1ce18.nq.gz
│   ├── 4ce934a31f18c0df7776ff34c29851daaffce49f.nq.gz
│   ├── 5f67c1d451f9ced120d30df868ce81d18e642bc8.nq.gz
│   ├── 68623d4982181e1f939dcf3b3b222a958c0fc32a.nq.gz
│   ├── 6f9e005b8c172b734d433f5eb753ec45a8206de5.nq.gz
│   ├── 6fa46878030cbe6bee8bf2f8b841d34c4b614287.nq.gz
│   ├── 734dc40efffbdeae9dd2e9f1856ec4d32812535f.nq.gz
│   ├── 7350d308c59c612465577b53980afb32dd726528.nq.gz
│   ├── 7579e1355f73ad6bf2f53b87cdad02619ddfa72a.nq.gz
│   ├── 7960a1ebe0ff7edfd31ef2f7a985baf4f7ca62fd.nq.gz
│   ├── 7cd1aefa2984726053a2319ca0510fc8c65beb69.nq.gz
│   ├── 822e990f3ac7b06431667507439abddb057a0756.nq.gz
│   ├── 82f595134297601e6f177554be7f7c960338589e.nq.gz
│   ├── 867fbe96dabf1967f60987c6fea720ec348c0d76.nq.gz
│   ├── acf263d5b38e58dc04e0f125d804254e2c28ceb3.nq.gz
│   ├── c1abf5ce880a2cf740a44abc033326098d8524f3.nq.gz
│   ├── cd104183d5cd5fd4d46ae0d2e6995c523098a4fe.nq.gz
│   ├── cf510d1b3ccda19d64692a87b998b1b0b134747a.nq.gz
│   ├── d9a259015802350bb2e9b9ea963b8b95cc1d61f8.nq.gz
│   ├── db298a2f67a9a66dd9095bdeee9cb79cc8291da8.nq.gz
│   ├── e3d7c0626fd60ecd707cdcde31fa233d132cc7c4.nq.gz
│   ├── e564134c214e9ad3be4b580cf0e1b6a2a1cb2849.nq.gz
│   ├── ea1393fb05192ffc286fec05a4caf07a5c0636d5.nq.gz
│   └── f67bec815653a41d9d6bb7cda75b00f728640fe0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cdbf79a94611bcf96bc3cd31858e3714e9836cca.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[PennyLaneAI/PennyLane-qsharp](https://github.com/PennyLaneAI/PennyLane-qsharp)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
