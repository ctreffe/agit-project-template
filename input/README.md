# External Files and Sources

Use `input/` for files supplied by the maintainer or obtained from external
sources. This includes documents, datasets, screenshots, exports, forms and
other files that enter the project from outside its maintained project files.

New or uncertain files start in `intake/`. Files whose handling is already
clear may be placed directly in the appropriate folder:

- `intake/` contains files that have not yet been classified;
- `restricted/` contains local files whose contents an assistant must not
  inspect;
- `local/` contains local files approved for assistant access but not for Git;
- `versioned/` contains files deliberately approved for Git versioning and
  assistant access.

Record safe source and handling information in `INVENTORY.md`. If filenames,
paths or other details are themselves sensitive, keep them in the ignored
`INVENTORY.local.md` instead.

Assistant access, Git versioning and publication or external sharing are
separate maintainer decisions. Moving a file does not authorize reading,
staging, committing, pushing or sharing it. Files that become maintained
project content may move to a more specific project folder after their origin
and handling have been recorded.
