# Compilation Instructions for EAP Document

This document contains instructions for compiling the Maestro Early Access Program (EAP) LaTeX document to PDF.

## Prerequisites

You need to have a LaTeX distribution installed. On Fedora systems, install the required packages:

```bash
sudo dnf install -y texlive-scheme-basic texlive-latex texlive-xetex texlive-collection-fontsrecommended
```

## Compilation Steps

1. Navigate to the `eap_document` directory:
   ```bash
   cd eap_document
   ```

2. Compile the LaTeX document to PDF using pdflatex:
   ```bash
   pdflatex eap_document.tex
   ```

3. Run the command again to ensure proper hyperlinks and outlines:
   ```bash
   pdflatex eap_document.tex
   ```

## Output

The compilation will generate several files:
- `eap_document.pdf` - The final PDF document
- `eap_document.log` - LaTeX compilation log
- `eap_document.aux` - Auxiliary file for cross-references
- `eap_document.out` - Hyperref outline file

## Notes

- The document includes the `input_box.png` image which must be in the same directory
- The document uses standard LaTeX packages: geometry, xcolor, hyperref, and graphicx
- The PDF will be approximately 3 pages with the Maestro interface screenshot included

## Troubleshooting

If you encounter errors:
1. Ensure all required LaTeX packages are installed
2. Verify that `input_box.png` is in the same directory as the .tex file
3. Check the `eap_document.log` file for specific error messages