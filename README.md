# FTDI245R Signal Acquisition Architecture

Project file namespace: `fsa`. The architecture starts at `fsaManual.tex`.
This project copy changes the template project name and namespace only;
remaining template placeholders and examples are not approved project facts.
Unresolved project decisions remain assigned to the project requester.

## Sources

- `fsa*.tex`: manual, front matter, chapters, appendices, and glossary.
- `TikZ/`: separate editable diagram sources, grouped by including chapter.
- `fsaReferences.bib` and `IEEEtran.bst`: bibliography and citation style.
- `cornell.cls`: the manual's local document class.
- `AGENTS.md`, `CLAUDE.md`, and `SKILL.md`: bootstrap pointers to the authoritative LaTeX guidance.
- `fsaMakefilePowerShell.ps1` and `fsaMakefileMacLinux`: build configuration.

Read `fsaDocumentGuide.tex` for authoring and toolchain details. This README
and `.gitignore` use standard repository filenames.

## Build

Required tools: `pdflatex`, `bibtex`, `makeglossaries`, and `makeindex`, with
the LaTeX packages used by the manual. `latexmk` is needed by the clean target.

From this directory on Windows PowerShell:

```powershell
.\fsaMakefilePowerShell.ps1 -Action pdf
```

On macOS or Linux:

```sh
make -f fsaMakefileMacLinux pdf
```

The output is `fsaManual.pdf`. PDFs and intermediate build outputs are ignored
and are not included in the staged source package. A documented build command
is not evidence of a successful build.

Template teaching slides, legacy diagrams/images, the sample Visio file, and
unused legacy bibliography/class/style files remain local and are excluded
from this project's source package.
