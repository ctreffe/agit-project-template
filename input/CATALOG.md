# External File and Source Catalog

Record unchanged external files and sources, including sources that remain
outside the repository. Put only metadata suitable for Git here; keep sensitive
details in ignored `CATALOG.local.md` and device-specific resolutions in
ignored `PATHS.local.md`.

| ID | Description | Kind | Content location | Assistant access | Git content | External sharing | Source version or retrieval state | Integrity | Last verified | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `<source-id>` | `<safe description>` | `<file | dataset | service | URL | other>` | `<intake | restricted | local | versioned | stable URL or logical external location>` | `<not approved | approved scope>` | `<no | yes | not applicable>` | `<not approved | approved scope>` | `<version, timestamp or mutability note>` | `<checksum, validation or not applicable>` | `<date>` | `<provenance or handling notes>` |

Use stable public URLs directly. Use logical locations for device-specific or
private locations and resolve them through `PATHS.local.md`, copied from
`PATHS.local.example.md`. Never record credentials or private share tokens.
A catalog entry records decisions but grants no additional permission.
