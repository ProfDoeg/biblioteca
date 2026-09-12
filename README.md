# biblioteca

libros

A general library: books and articles, kept as files, with one catalog.

- `books/`, `articles/`: the items, named `<surname>_<year>_<short_title>.<ext>`.
- `catalog.json`: one record per item (author, title, year, publisher, language, source, note).
- `CATALOG.md`: the human table, generated. Never edit by hand.
- `raw/`: scans and drops not yet cataloged.

To add an item: put the file on its shelf, add a record to `catalog.json`, run
`python3 catalog.py` (it rewrites `CATALOG.md` and fails if a file and the catalog
disagree), commit both.

Nothing here is tied to the atlas; it is Anthony's reading, filed.
