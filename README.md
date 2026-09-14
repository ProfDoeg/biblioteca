# biblioteca

libros

A general library: books and articles, kept as files, with one catalog.

- `books/`, `articles/`: the items, named `<surname>_<year>_<short_title>.<ext>`.
- `catalog.json`: one record per item: the shelf fields (author, title, year, publisher,
  language, source, note) and the BibTeX fields (bibtype, citekey, bibauthor, journal, volume,
  number, pages, booktitle, editor, translator, address, doi, bibnote) plus `annotation`, a
  paragraph on what the item is and why it is here.
- `CATALOG.md`: the human table, generated.
- `references.bib`: the BibTeX file, generated; the `annote` field carries the annotation.
  UTF-8 throughout, so compile with biblatex and biber (or bibtex8).
- `BIBLIOGRAPHY.md`: the annotated bibliography for reading, generated, alphabetical by cite key.
- `raw/`: scans and drops not yet cataloged.

Never edit the generated files by hand. To add an item: put the file on its shelf, add a
record to `catalog.json`, run `python3 catalog.py` (it rewrites the three generated files and
fails if a file and the catalog disagree), commit all four.

Nothing here is tied to the atlas; it is Anthony's reading, filed.
