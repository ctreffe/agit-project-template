# Temporary Working Files

`temp/` contains disposable intermediate files used during active project work.
All contents outside `restricted/` are assistant-readable. Everything under
`temp/` is local-only, ignored by Git and must never be versioned.

Use `restricted/` for temporary files that assistants must not enumerate or
read. Temporary files are not cataloged. Move a file to `materials/` and add it
to `materials/CATALOG.md` when it becomes a durable working foundation.
