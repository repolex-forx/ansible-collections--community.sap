# Repolex Knowledge Graph of ansible-collections/community.sap

RDF knowledge graph data for [ansible-collections/community.sap](https://github.com/ansible-collections/community.sap), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-collections/community.sap
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9f06d3358ffa63af13209fd043e730ba39f22a1a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9f06d3358ffa63af13209fd043e730ba39f22a1a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0164155b81025416095f31a4732098ec238e6476.nq.gz
│   ├── 08de7a62ea272134222954dfa78e8ed27d157929.nq.gz
│   ├── 0972cd2e8e58d51f20c6b0d23d8f89154c7ac076.nq.gz
│   ├── 09ee81186902ead1a8b05f9a6a21f249a35ded8c.nq.gz
│   ├── 15cbcba59af9e1f63da4c35eaa2f1007fd4566ae.nq.gz
│   ├── 23490ccdedb213b1dc8e7a857f5ef9c5373dc4c6.nq.gz
│   ├── 2df6b13c9284c610f209084aac65fc39bd9e8eff.nq.gz
│   ├── 39f79a298908adff98db1af988ecc37ec67bae9f.nq.gz
│   ├── 49654b8b54edb4329101e7d859da03c3cac3b79b.nq.gz
│   ├── 50d5c86d3503a3ff2ecee0bf12d204c16c68943a.nq.gz
│   ├── 5389bdcb2fd31b211f4d1563ccde97029cf217cf.nq.gz
│   ├── 5673863e1685240665aacaadb3c11151e4adf0c7.nq.gz
│   ├── 5fe2edd1fd3462b106fca1a576dbba590d678ea3.nq.gz
│   ├── 604cc9ba0f100bb475dd66eb4e6efc5adf926415.nq.gz
│   ├── 6bd2db9c32a4c9d7b326bd972ac2c3ac701389ec.nq.gz
│   ├── 6e30606b6f5e67506dea9e42582e58094dc598c8.nq.gz
│   ├── 714ed15a54c5becf088c2bb92632c11e4157838b.nq.gz
│   ├── 7362c13d8cfb06c8f10a9c900a3cbbf1e7a2f45f.nq.gz
│   ├── 740c8115458b12e3a8f24220e718e0b33ef2e16d.nq.gz
│   ├── 8f20b4575c69bd52f56dff028c18f7f700e208e8.nq.gz
│   ├── 982689f7e6d1cc709e8e6f77e086206d53688f6c.nq.gz
│   ├── 98f08ad6a8474fbcc3e338436bae46663d4aa4ae.nq.gz
│   ├── 9dccf7ef174657345b77b37626c52cdc0390117f.nq.gz
│   ├── 9fad0d343c07aa82e21752481014bb870092c693.nq.gz
│   ├── a646c0241c7e09dd427ef636c613aee0445c1d73.nq.gz
│   ├── b4a17dec0383181a3caed73fc87775df337d0eee.nq.gz
│   ├── b63d90d354b9d294fc93609eb645ca8ba7af7a66.nq.gz
│   ├── b8d61db6218b751f9538537d17a8fb16f54ec9c9.nq.gz
│   ├── c1c075bc02607c01ff0dc6784d12557cac6ef385.nq.gz
│   ├── c29b8123aadf3f68c32bec598d24f2857d2d2d0c.nq.gz
│   ├── db443763c044026c1570460e857d78d36d8cc8dd.nq.gz
│   ├── dd935b2701613d759c1db0247f88514694393f7b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   ├── f60ee6782280b043f8014305cffb9b0d2c4d184d.nq.gz
│   ├── f90bd1ad861af4f092444b8667bbc662d345e7d9.nq.gz
│   └── fb023cf46c400f181211eeaee6be13de7fa1500a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9f06d3358ffa63af13209fd043e730ba39f22a1a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 45 files
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

[ansible-collections/community.sap](https://github.com/ansible-collections/community.sap)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
