# HUL-Schemas

A persistent home for the metadata schemas used by Harvard Library.

## Purpose

This repository gives the XML schemas (and related metadata specifications) that Harvard Library systems depend on a stable, version-controlled location where they can always be found.

## Referencing schemas

**Always reference a schema by its NRS URN, never by its GitHub URL.**

Each schema in this repository is assigned a persistent identifier through Harvard's Name Resolution Service (NRS). The NRS URN resolves to the current location of the file, so references keep working even if the repository is moved, renamed, or restructured.

| Do | Don't |
| --- | --- |
| `https://nrs.harvard.edu/urn-3:...` | `https://github.com/harvard-lts/HUL-Schemas/...` |
| | `https://raw.githubusercontent.com/harvard-lts/HUL-Schemas/...` |

Use the NRS URN in `xsi:schemaLocation` attributes, documentation, and application configuration.

## Layout

Schemas are organized by standard under `schema/`:

```
schema/
  <standard>/
    <schema file>
```

## Available schemas

| Schema | Namespace | File | NRS URN |
| --- | --- | --- | --- |
| METS 2.0 | `http://www.loc.gov/METS/v2` | [`schema/mets/mets2.xsd`](schema/mets/mets2.xsd) | _TBD_ |

## Adding a schema

1. Add the file under `schema/<standard>/`.
2. Request an NRS URN that points to the file.
3. Add a row to the **Available schemas** table above with the URN.
4. Open a pull request against `main`.

Once a schema has been published under an NRS URN, do not move or rename it without updating the NRS mapping.

## License

Each schema retains the license of its original publisher; see the documentation within each schema file. For example, METS 2.0 is released under [CC0 1.0](http://creativecommons.org/publicdomain/zero/1.0/).
