# fen
another type of wetland

## Now trying (impromptu)

- [markup](markup) directory to test markup languages,
  mainly Markdown, reStructuredText, and AsciiDoc

[Markdown]: markup/md/readme.md
[reStructuredText]: markup/rst/readme.rst
[AsciiDoc]: markup/adoc/readme.adoc

## Test and document

- readme.md has "pretty" markup viewing on the web
- sub/readme.txt with [.md symbolic link](sub/readme.md)
- [relative link](sub) may work with the .md symbolic link
- sub/plain.txt with readme.rst symbolic link may be shown
  "pretty" via [another relative link](sub/try/)

## Test and put aside

- citation file ending with `.cff`, naming as lowercase
  worked fine, despite the Citation File Format (CFF) schema
  requires UPPERCASE naming
- with multiple citation files, the `.cff` file will be
  found first and some options to copy citation will appear
  before "view citation file", under "cite this repository"
- citation file ending with either `.md` or `.bib` will not
  show more options, and will only have "view citation file"
- .github/workflows/basic.yml was created by suggested
  minimum configurations to try GitHub Actions
- [off directory](off) with readme was created as
  dependency to limit workflow without deletion
- renaming from .yml to .txt could disable the workflow,
  and keep the configuration file as plain text document,
  likewise: [basic.txt](.github/workflows/basic.txt)

## Anything else

Basic requirements to work with the contents:

- a web repository
- a web browser
- any markup tool or browser extension (optional)

The "pretty" markup preview is a built-in feature of the
web repository i.e. GitHub. Otherwise, run a self-hosted
repository or use any markup editor to preview contents.

Licensing was never decided for this project, but a
simple attribution would be good enough for personal
and educational use.
