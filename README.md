# శ్రీ వినాయక వ్రతకల్పము

XeLaTeX edition of the Vinayaka Vratha Kalpam booklet (A4, Telugu, 14pt body).

## Requirements

TeX Live (or MiKTeX) with XeLaTeX and latexmk. Fonts are bundled in `fonts/`.

## Build

The `latexmkrc` uses XeLaTeX, keeps auxiliary files in `build/`, and writes
the PDFs to the repository root.

| Mode  | Command                              | Output                             |
|-------|--------------------------------------|------------------------------------|
| Both  | `latexmk`                            | both PDFs below                    |
| PDF   | `latexmk vinayaka-vratha-kalpam`     | `vinayaka-vratha-kalpam.pdf`       |
| Print | `latexmk vinayaka-vratha-kalpam-print` | `vinayaka-vratha-kalpam-print.pdf` |

- **PDF mode** is for reading on screen: the contents follow the cover directly.
- **Print mode** adds a blank page after the cover so the cover prints alone
  on its sheet in double-sided printing and content starts on a right-hand
  page. Page numbers include the blank page.

Clean up with `latexmk -c` (auxiliary files) or `latexmk -C` (also the PDFs).
