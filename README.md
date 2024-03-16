# PUTwiki
---

## Initializing locally

1. Clone repository
2. Install Python
   1. Currently used version is `3.12.1`
   2. Create a virtual environment - not necessary, but **recommended**
      1. `python -m venv <virtual_environment_name>`
3. Install MkDocs
   1. `pip install mkdocs-material`
4. Run project with command:
   1. `mkdocs serve`

List of python dependencies is also stored in `py-requirements.txt` file.

## Editing documents

`mkdocs.yml` - main config file containing all necessary settings needed to deploy MkDocs webpage

`docs` - directory containing all wiki files

`docs/assets` - subdirectory containing all assets used in wiki

`docs/style` - subdirectory containing all CSS style files used in wiki

## Sources

| Description        | Link                                                   |
|--------------------|--------------------------------------------------------|
| **_REFERENCES_**   | https://squidfunk.github.io/mkdocs-material/reference/ |
| source project     | https://squidfunk.github.io/mkdocs-material/           |
| plugins            | https://squidfunk.github.io/mkdocs-material/plugins/   |
| documentation      | https://www.mkdocs.org/                                |
| catalog of plugins | https://github.com/mkdocs/catalog                      |
