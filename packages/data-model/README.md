# @iroha2/data-model

Generated SCALE-definitions for Iroha Data Model

## Versioning

| Iroha                                                           | This package |
| --------------------------------------------------------------- | ------------ |
| 2.0.0-pre-rc.6-lts (`75da907f66d5270f407a50e06bc76cec41d3d409`) | `1.4.0`      |
| 2.0.0-pre-rc.5 (`43be45fc7fb7b0bd73f87b4fef167d61680c8e1e`)     | `1.3.0`      |
| 2.0.0-pre-rc.4 (`d00e0a9172d2a887a97f504796db5f2e05939c10`)     | `1.2.0`      |
| 2.0.0-pre-rc.3 (`8d83a3eff33f29b49004a0a5efe643b10f0f256e`)     | `1.1.0`      |
| 2.0.0-pre-rc.2 (`920e4d12754b0f3bf08cbaa5221d91c27863fcdc`)     | `1.0.0`      |
| 2.0.0-pre-rc.1                                                  | `0.5.0`      |

## Installation

Configure your package manager to fetch scoped packages from nexus. Example for `npm`/`pnpm` - file `.npmrc`:

```ini
# .npmrc
@iroha2:registry=https://nexus.iroha.tech/repository/npm-group/
```

Then, install packages:

```bash
npm i @iroha2/data-model
```

## Known issues

### Entries ordering in `BTreeMap` and `BTreeSet`

In Rust, these structs assume that items are `PartialOrd`-ordered while encoding to ensure consistency for signatures creation. This library doesn't provide this feature and you should put entries in the correct order by yourself.